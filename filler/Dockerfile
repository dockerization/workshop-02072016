# Configure HEAD
FROM ruby:2.3.0
ENV PORT 4568
ENV LOGIC_PORT 4567

# BODY
ADD . /app/
RUN cd /app && bundle install

# Add some security
RUN useradd -ms /bin/bash usafe
RUN chown -R usafe:usafe /app

WORKDIR /app
USER usafe

EXPOSE $PORT
CMD ["ruby", "app.rb"]
