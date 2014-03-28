---
layout: post
title: Running behat on ACE
---

Sometimes you just need to bootstrap Drupal to get all your tests done. It's possible, and it's not pretty. It involves using [Drush](https://github.com/drush-ops/drush) [ssh](http://www.drushcommands.com/drush-6x/ssh/site-ssh) to run tasks on the server. This includes downloading [composer.phar](https://getcomposer.org/), doing its setup, running a subset of [@api](http://docs.behat.org/guides/6.cli.html#gherkin-filters) tagged tests, and finally, rsyncing the results back to the CI server.

See the ant snippet.

{% gist 94f944161a7b97bf1ad2 %}
