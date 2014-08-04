# Toggle

[![Build Status](https://travis-ci.org/cv-library/Toggle.svg?branch=master)](https://travis-ci.org/cv-library/Toggle)
[![Coverage Status](https://img.shields.io/coveralls/cv-library/Toggle.svg)](https://coveralls.io/r/cv-library/Toggle)

Feature toggles for Perl, stored in Redis (or any other store of your choice).

Based on [James Golick's rollout](http://github.com/jamesgolick/rollout)
library for Ruby.

## How do I use this code?

See [the POD](lib/Toggle.pod) for instructions.

## What are feature toggles?

Feature toggles are known by a huge variety of names: feature switches,
feature flags, feature flippers, or conditional features.

- https://en.wikipedia.org/wiki/Feature_toggle
- http://martinfowler.com/bliki/FeatureToggle.html

They can help you avoid long-lived branches with painful merges, by letting
you hide unfinished features from your users by default.  At runtime, you can
change which users or groups are allowed to see your new feature - to enable
staff testing or beta testing, for example.

Another possibility is an incremental rollout, where you expose a new feature
to a small percentage of users, and then increase that percentage gradually
as you gain more confidence in the code.  You can roll back the feature
very quickly if you discover serious bugs.

All this without needing to redeploy your code.

## What's special about this module?

This module stores the feature flags in a database of your choice - it works
particularly well with Redis, and makes just one key lookup to decide if a
feature is active.

It becomes very easy to write a user interface to control the rollout of
features.

## Copyright

Copyright © 2014 CV-Library Ltd.

Licensed under the same terms as Perl itself.
