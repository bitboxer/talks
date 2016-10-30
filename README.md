# My Talks

In this repo I store all the talks I did. You can also 
see them on my [speakerdeck](https://speakerdeck.com/bitboxer).

## Tickety Tick

**rubyconf.pt 2016**

A small lightning talk I gave about a [browser
extension](http://github.com/bitcrowd/tickety-tick) we wrote at [bitcrowd](http://bitcrowd.net)
to unify names of branches and commits inside of our teams.

[Slides](https://speakerdeck.com/bitboxer/tickety-tick)

## InfluxDB

**Ruby Usergroup Berlin 03/2016**

[InfluxDB](https://www.influxdata.com/) is an interesting database. It focuses on time
series data and has an awesome toolchain for handling
those kind of datasets. In this talk I introduce a bit
of the toolchain around it.

[Slides](https://speakerdeck.com/bitboxer/influxdb)

## Ruby > Web

**Ruby Usergroup Berlin 11/2015**

This is a small lightning talk highlighting several non web things that use ruby.

[Slides](https://speakerdeck.com/bitboxer/ruby-web)

## Statemachines

**Ruby Usergroup Berlin 01/2015**

Rails has this nice little feature called Enums. The [introduction
example](http://edgeapi.rubyonrails.org/classes/ActiveRecord/Enum.html) is
something like this:

```
class Conversation < ActiveRecord::Base
enum status: [ :active, :archived ]
end
```

And I think this is dangerous. States should be dealed with in a state machine. Why you ask? Because state changes usually have conditions attached to them. Only archive if ... . If you want to model something like that with enums, you end up with a horrible version of a state machine.

[Slides](https://speakerdeck.com/bitboxer/introduction-to-statemachines)

## beanstalkd

**Ruby Usergroup Berlin 06/2014**

A revolutionary idea: why not use a job queue system for your job queue?

Most people use delayed job aka a database or resque/sidekiq for queuing. But
why hack your way around a database or a "smarter memcache" to do a simple
queue when there are other solutions that were build for this?

Beanstalkd is one of them. It's small. It's fast. It's awesome. And I show you
why.

[Slides](https://speakerdeck.com/bitboxer/beanstalkd)

## WECK DEN GEEK IN DIR

**Froscon/RedFrogConf 2013**

Was ist ein Geek? Oder Nerd? Und wo trifft man mehr davon? Warum sollte man die
überhaupt treffen wollen? Reicht es nicht, wenn man schon tagsüber im Büro mit
denen zu tun hat? Hilfe ich bin das erste mal hier auf einer Konferenz… und nu?
Und wieso sind hier so viele Fragen? Hoffentlich beantwortet die da mal jemand
in dem Talk!!1! Kann nicht jemand mal an die Nerds denken hier?!

[Video](http://media.ccc.de/browse/conferences/froscon/2013/hs6_-_2013-08-24_10:30_-_weck_den_geek_in_dir_-_bodo_tasche_-_1261.html)  
[Slides](https://speakerdeck.com/bitboxer/weck-den-geek-in-dir)

## Endless fun with Arduino and Eventmachine

**Euruko 2011**

After seven years of working as a java developer, Bodo fall in love with ruby
and moved to cologne to work as a full time ruby developer. He started
tinkering with hardware as a teenager with his C-64, his dad created the robots
and he wrote the software that made them move. Besides coding Bodo loves
diving, traveling and biking.

In his talk he will show how to connect an arduino with ruby using
eventmachine. He will also show potential use cases and projects that can be
created using this technique. Most of the projects can be finished on one
weekend.

[Slides](https://speakerdeck.com/bitboxer/endless-fun-with-arduino-and-eventmachine)
