# Jekyll::Paginate - Categories

Customized pagination generator for Jekyll.
Include features to paginate posts based on categories.

[![Build Status](https://secure.travis-ci.org/jekyll/jekyll-paginate.svg?branch=master)](https://travis-ci.org/jekyll/jekyll-paginate)

## Installation

As the original jekyll-paginate plugin is no longer maintained, I will not send a PR but instead host this plugin on this branch.

Add this line to your application's Gemfile:

    gem 'jekyll-paginate', :git => 'git://github.com/pyliaorachel/jekyll-paginate.git', :branch => 'paginate_categories'

And then execute:

    $ bundle

Or install it yourself following the steps below:

    $ git clone -b paginate_categories https://github.com/pyliaorachel/jekyll-paginate
    $ gem build jekyll-pagiinate.gemspec
    $ sudo gem install jekyll-paginate-1.1.0.gem

## Usage

Once the gem is installed on your system, Jekyll will auto-require it. Just set the following configuration in `_config.yml`:

```yml
paginate: [how-many-posts-per-page]
paginate_categories: [true | false] # there shouldn't be a reason to choose false... you can just follow the original jekyll-paginate configurations
paginate_paths: 
  [category 1]: [paginate_path 1]
  [category 2]: [paginate_path 2]
  ...
```

### Example

```yml
paginate: 10
paginate_categories: true
paginate_paths: 
  Blog: "/blog/page:num/"
  Tutorial: "/tutorial/page:num/"
```

Also, in your posts' front matters, include:

```yml
---
categories: Blog [other category] [other category] ...
---
```

This post appears in path `/blog/page:num/` of your site, e.g. https://pyliaorachel.github.io/blog/page2/

```yml
---
categories: Tutorial [other category] [other category] ...
---
```

This post appears in path `/tutorial/page:num/` of your site, e.g. https://pyliaorachel.github.io/tutorial/page2/

## Demo

[MyCoon](https://github.com/pyliaorachel/pyliaorachel.github.io/tree/source)
