BSON [![Build Status](https://secure.travis-ci.org/mongodb/bson-ruby.png?branch=master&.png)](http://travis-ci.org/mongodb/bson-ruby) [![Code Climate](https://codeclimate.com/github/mongodb/bson-ruby.png)](https://codeclimate.com/github/mongodb/bson-ruby)
====

An implementation of the BSON specification in Ruby.

Compatibility
-------------

BSON is tested against MRI (1.8.7+), JRuby (1.5.0+), and REE.

Documentation
-------------

Please see the [BSON specification](http://bsonspec.org) and the [API Documentation](http://rdoc.info/github/mongodb/bson-ruby/master/frames).

TODO: Review
------------

- note threading concerns
- no safety limit needed for non-pathological use (review this)
- symbol ~ gain: 0.25 (36 --> 27) Xeon, gain: 0.34 (41 --> 27) Core 2
- string ~ gain: 0.15 (33 --> 28) Xeon, gain: 0.24 (39 --> 29) Core 2
- with safety limit, mutex overhead eats up the benefit on Xeon
- symbol ~ gain: 0.15 (41 --> 35) Core 2
- string ~ gain: 0.05 (39 --> 37) Core 2

Notes
-----

- Ruby prof for encoding of twitter data looks good
- modules and classes have some overhead that can be significant
- optimization in Ruby seems to have more effect for Core 2 and less for Xeon

License
-------

Copyright (C) 2013 10gen Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
