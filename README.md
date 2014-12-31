# Littlstar API Documentation

This repo is a fork of the [Slate](https://github.com/tripit/slate) API Documentation Generator. It uses markdown to generate a single static page of docs.

## Clone/Initialize

This project is built on top of [Middleman](http://middlemanapp.com/), so a current version of Ruby and the Bundler gem are required.

```bash
git clone git@github.com:littlstar/docs.git
cd docs
bundle
```

The site can be compiled and served locally by running:

```bash
middleman s
```

## Configuration

Global site configuration is stored in the `config.rb` file.

## Development and Deploy

Local development is done either directly in the master branch, or in a topic/working branch which is then merged into master. When you're ready to deploy/publish, run the following rake command from the master branch:

```bash
rake publish
```

This command will build the site and push it to the gh-pages branch on Github.

## Further Reading

The original [Slate wiki](https://github.com/tripit/slate/wiki) has excellent documentation explaining more advanced usage and configuration.
