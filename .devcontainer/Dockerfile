FROM ruby:3.2-slim-bullseye
ENV LANG C.UTF-8

RUN apt-get update -qq && apt-get install -y curl \
                                             gnupg \
                                             gosu \
                                             git \
                                             imagemagick \
                                             ghostscript \
                                             postgresql-client \
                                             build-essential \
                                             libpq-dev
WORKDIR /workspaces
COPY entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/entrypoint.sh
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
