# rubygems-mirror

This gem can help you to full mirror of [rubygems.org](http://rubygems.org),
it is an update to the old `gem mirror` command. It uses `net/http/persistent`
and threads to grab the mirror set a little faster than the original.
Eventually it will replace `gem mirror` completely. Right now the API is not
completely stable (it will change several times before release), however, I
will maintain stability in master.

## FEATURES/PROBLEMS:

* Fast mirroring
* Limited tests - just functional

## REQUIREMENTS:

* rubygems
* net/http/persistent

## USAGE

In a file at `~/.gem/.mirrorrc` add a config that looks like the following:

    ---
    - from:
        provider: http
        url: http://rubygems.org
      to:
        provider: local
        path: /data/rubygems
      parallelism: 10

Either install the gem:

    $ gem install rubygems-mirror
    $ gem mirror

Or clone the source code and use rake command:

    $ bundle install
    $ rake mirror:update


## RESOURCES

* [WebSite](http://rubygems.org/)
* [Documentation](http://rubygems.rubyforge.org/rubygems-mirror/README_rdoc.html)
* [Wiki](http://wiki.github.com/rubygems/rubygems-mirror/)
* [Source Code](http://github.com/rubygems/rubygems-mirror/)
* [Issues](http://github.com/rubygems/rubygems-mirror/issues)

## LICENSE:

    (The MIT License)

    Copyright (c) 2010 James Tucker, The RubyGems Team

    Permission is hereby granted, free of charge, to any person obtaining
    a copy of this software and associated documentation files (the
    'Software'), to deal in the Software without restriction, including
    without limitation the rights to use, copy, modify, merge, publish,
    distribute, sublicense, and/or sell copies of the Software, and to
    permit persons to whom the Software is furnished to do so, subject to
    the following conditions:

    The above copyright notice and this permission notice shall be
    included in all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
    EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
    MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT.
    IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
    CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
    TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
    SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.