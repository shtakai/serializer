# serializer

[![Build Status](https://travis-ci.org/charlieegan3/serializer.svg?branch=master)](https://travis-ci.org/charlieegan3/serializer)
[![Code Climate](https://codeclimate.com/github/charlieegan3/serializer/badges/gpa.svg)](https://codeclimate.com/github/charlieegan3/serializer)
[![Test Coverage](https://codeclimate.com/github/charlieegan3/serializer/badges/coverage.svg)](https://codeclimate.com/github/charlieegan3/serializer/coverage) [![GuardRails badge](https://badges.production.guardrails.io/shtakai/serializer.svg)](https://www.guardrails.io)

serializer collects links from Hacker news, Reddit & Product Hunt and lists them in **sequential** order, some might even say it *serializes* them. It also collects a few other sources, not all of which are voting based, e.g. Ars Technica.

I deploy the app to [serializer.io](http://www.serializer.io) when there are changes to deploy. It's currently configured to work with [dokku-alt](https://github.com/dokku-alt/dokku-alt). [rufus-scheduler](https://github.com/jmettraux/rufus-scheduler) is used to run the collection tasks.

## Features
* Read-to-Here Marker
* **Loginless** sessions for cross-device syncing
* Customizable source feeds - toggle sources in 'menu'
* Reading time estimates (based on 300wpm and a simple content extractor)
* Tweet counts that are updated for recently added items
* Basic duplicate link removal
* Tab title unread marker & background refresh

## Feedback & Contributing
I'm keen to accept changes that make serializer work better for you, pull requests welcome. If something's not right [open an issue](https://github.com/charlieegan3/serializer/issues/new). There's an anonymous feedback form [here](https://charlie43.typeform.com/to/tZWtCn).

#### Notes
* `rake collect_active` & `rake collect_feeds` can be used to populate items, collection doesn't run automatically in development.
* Images and icons are hosted on [Cloudinary](https://cloudinary.com/users/register/free).
* If the app runs into issues it sends notifications via Airbrake.

#### ENV Variables
To have everything up and running you'll need most of these set.

* `CLOUD_NAME`
* `CLOUDINARY_SECRET`
* `CLOUDINARY_KEY`
* `AIRBRAKE_KEY`
* `SECRET_KEY_BASE`
* `SECRET_TOKEN`
* `CODECLIMATE_REPO_TOKEN`
* `TRELLO_KEY`
