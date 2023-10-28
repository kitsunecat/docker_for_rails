FROM ruby:3.2.2

ENV ROOT="/app"
ENV LANG=C.UTF-8
ENV TZ=Asia/Tokyo

WORKDIR ${ROOT}

COPY ./web/Gemfile ./web/Gemfile.lock ${ROOT}

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs

RUN gem install bundler
RUN bundle install

COPY ./docker/ruby/entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["/usr/bin/entrypoint.sh"]

EXPOSE 3000
CMD ["bundle", "exec", "rails", "server", "-b", "0.0.0.0"]
