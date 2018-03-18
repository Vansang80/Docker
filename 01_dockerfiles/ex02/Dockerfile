FROM				ruby:latest

RUN					apt-get update -y && apt-get upgrade -y && \
					apt-get install -qy wget tar bzip2 sudo && \
					apt-get install -y nodejs && \
					apt-get install sqlite3 -y && \
					gem update --system && \
					gem install bundler && \
					gem install rails

ONBUILD COPY		. /opt/app

ONBUILD WORKDIR		/opt/app

ONBUILD RUN			bundle install && \
					rake db:migrate && \
					rake db:seed
