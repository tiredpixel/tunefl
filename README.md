# tunefl

![](https://raw.github.com/tiredpixel/tunefl/master/app/assets/images/logo.png)

tunefl is a musical application which runs [LilyPond](http://lilypond.org) as a service.
The live tunefl service is provided by [tunefl.com](http://www.tunefl.com) ([@tunefl](https://twitter.com/tunefl)).

More sleep lost by [tiredpixel](http://www.tiredpixel.com).

[![Build Status](https://travis-ci.org/tiredpixel/tunefl.png?branch=master,stable)](https://travis-ci.org/tiredpixel/tunefl)


## Externals

- [PostgreSQL](http://www.postgresql.org/)

- [Redis](http://redis.io/)

- [LilyPond](http://lilypond.org)
  
  Ensure in `PATH` by running `lilypond` on the command-line.


## Installation

- Config
  
  Copy and edit as appropriate:
  
  - `.env.example` => `.env`

- Libraries
  
  Using [Bundler](http://gembundler.com/), `bundle install`.

- Database
  
  Migrate using `rake db:migrate` (`rake db:schema:load` won't work properly).

The default Ruby version supported is defined in `.ruby-version`.
Any other versions supported are defined in `.travis.yml`.


## Run-time

- Services are defined in `Procfile`.

- Using [Foreman](http://ddollar.github.io/foreman/), `foreman start`.

- To monitor the queue using [sidekiq-spy](https://github.com/tiredpixel/sidekiq-spy):

        sidekiq-spy -n resque

  ensuring `-u` matches `WORKER_REDIS_URL` and `-n` matches `WORKER_REDIS_NS`.


## Stay Tuned

We have a [Librelist](http://librelist.com) mailing list!
To subscribe, send an email to <tunefl@librelist.com>.
To unsubscribe, send an email to <tunefl-unsubscribe@librelist.com>.
There be [archives](http://librelist.com/browser/tunefl/).
That was easy.


## Testing

- Using [Foreman](http://ddollar.github.io/foreman/), `foreman run rspec`.


## Contributions

Contributions are embraced with much love and affection.
Please fork the repository and wizard your magic, ensuring that any tests are not broken by the changes.
Then send a pull request. Simples!
If you'd like to discuss what you're doing or planning to do, or if you get stuck on something, then just wave. :)

Do whatever makes you happy. We'll probably still like you. :)


## Blessing

May you find peace, and help others to do likewise.


## License

© [tunefl.com](http://www.tunefl.com) & [tiredpixel](http://www.tiredpixel.com) 2013.
It is free software, released under the MIT License, and may be redistributed under the terms specified in `LICENSE`.
