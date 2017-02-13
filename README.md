# DBPL 2017

Website for the The 16th International Symposium on Database Programming Languages

The website can be accessed via [http://dbpl2017.org](http://dbpl2017.org).

## Design

We use [a cutstomized Foundation download](http://foundation.zurb.com/develop/download.html#customizeFoundation) based on [this Paletton palette](http://paletton.com/#uid=64j0X0kofuw02yjaLCaEcpE++jr). The colors are mapped as follows:

* Paletton primary color (0) ↦ Foundation primary color
* Paletton secondary color #1 (0) ↦ Foundation alert color
* Paletton secondary color #2 (0) ↦ Foundation secondary color 
* Paletton secondary color #2 (0) ↦ Foundation success color
* Paletton complement color (0) ↦ Foundation warning color

## Development & Local Preview

See [the GitHub Jekyll documentation](https://help.github.com/articles/using-jekyll-with-pages/) for instructions how to run and preview the website locally. 

### Fun with Linux

You'll need Ruby 2.0+ (bin + dev packages) as well as the `bundler` package in order to run as the GitHub documentation suggests. If you are running Ubuntu 14.04 LTS, you will find out that merely executing

```bash
sudo apt-get install ruby2.0 ruby2.0-dev bundler
``` 

doesn't really help due to [a bug in the `ruby2.0` packaging](https://bugs.launchpad.net/ubuntu/+source/ruby2.0/+bug/1310292). To solve the problem [do as suggested by agent-8131](https://bugs.launchpad.net/ubuntu/+source/ruby2.0/+bug/1310292/comments/20) after that.

You might also be asked to require a JavaScript runtime [from this list](https://github.com/rails/execjs#execjs), e.g. with

```bash
sudo apt-get install nodejs
```

Upon that, you should be able to install the required Ruby packages for local preview by running

```bash
bundle install
```

You also need to install some gems:

```bash
gem install jekyll-redirect-from
```

from the `gh-pages` root folder.

Keep your gems up to date with

```bash
bundle update
```

as discussed in the ["Keeping Jekyll up to date" section of the GitHub Jekyll documentation](https://help.github.com/articles/using-jekyll-with-pages/#keeping-jekyll-up-to-date).

### Local Preview

Once you've managed to install the required Ruby bundles, you can preview the website locally with

```bash
bundle exec jekyll serve
```