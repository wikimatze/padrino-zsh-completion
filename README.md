# Installation

All you need is add the `_padrino` source to your `fpath` and call zsh commands for enabling autocompletion. If you
don't know what I mean please do the following:


```bash
$ mkdir -p ~/.zsh-completions
$ cp _padrino ~/.zsh-completions
$ vim ~/.zshrc
# add the following codes

  fpath=($HOME/.zsh-completions $fpath)
  autoload -U compinit
  compinit
```


Now reload your shell with `exec $SHELL`, install the [padrino gem](http://rubygems.org/gems/padrino) with
`gem install padrino`, and finally start using `$ padrino g` and press tab for complete your command


# Support

Currently all generator like the following are supported


```bash
controller  -- creates a new controller
mailer      -- creates a new mailer
migration   -- creates a new migration
model       -- creates a new model
plugin      -- add plugin to your app
project     -- create a new Padrino app
```


Dep in which context you are, different options are available, for example:


```bash
$padrino g model User -
  -d          -- removes all generated files
  -r          -- specify the root destination path
  -s          -- skip migration generation
```


or


```bash
$padrino g project HelloPadrino -
  -a     -- specify db adapter (options: 'mysql', 'sqlite' , 'postgres')
  -b     -- execute bundler dependencies installation
  -c     -- define stylesheet (options: 'compass', 'less', 'sass', 'scss')
  -d     -- define orm (options: 'mongoid', 'activerecord', 'datamapper', 'couchrest', 'mongomatic', 'ohm', 'ripple', 'seq
  -e     -- define renderer (options: 'erb', 'haml', 'slim', 'liquid')
  -i     -- generate tiny project skeleton without any components
  -m     -- define mock (options: 'mocha', 'rr')
  -n     -- specify app name different from the project name
  -r     -- the root destination path for the project
  -s     -- define script (options: 'prototype' 'rightjs' 'jquery' 'mootools' 'extcore' 'dojo')
  -t     -- define test (options: 'bacon', 'shoulda', 'cucumber', 'testspec', 'riot', 'rspec', 'minitest')
```


# License

This software is licensed under the [MIT license](http://en.wikipedia.org/wiki/MIT_License).

© Matthias Günther <matthias.guenther@wikimatze.de>

