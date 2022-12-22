# Contributing

## Local installation
To run the website locally, make sure you have installed the `jekyll` and `bundle` gems:
```
gem install jekyll bundler
```
To prepare the build environment, run:
```
bundle install
```
To build the site and make it available on a local server, change directory to the root of the repository and run:
```
bundle exec jekyll serve
```
Then, point your browser to [http://localhost:4000](http://localhost:4000).
For more information about Jekyll, visit [https://jekyllrb.com/docs/](https://jekyllrb.com/docs/).

## Adding a post
You can add a post by creating a file in the `_posts` directory.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for>

Once you've created the file, go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web ser>

Make sure the file has a proper header of the following form:
```
---
layout: post
title:  "<TITLE>"
date:   <YYYY-MM-DD hh:mm:ss> -0800
categories: <SPACE-SEPARATED KEYWORDS>
---
```
The `-0800` timezone parameter denotes PST.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
