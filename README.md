# bestcohort blog

This blog is built with [Middleman](https://middlemanapp.com/basics/install/).
When the time comes, we will deploy it using [Divshot](https://divshot.com/).
Markup in HAML, styles in SCSS, content in Markdown, syntax highlighting with [highlight.js](https://highlightjs.org/).

## Environment setup and running the server
+ Dependencies: `bundle install`
+ Run the server: `bundle exec middleman`
+ Navigate to `localhost:4567`
+ As it says in the CLI, inspect configs at `localhost:4567/__middleman`.
This can be ridiculously helpful.
+ Build: `bundle exec middleman build` (add `--verbose`) for error logging

## Contributing

If you've added a post you feel good about, just push to master.
If you would like some technical review, or you're altering someone else's code or
making a change that affects multiple pages, send a pull request.

### Writing a post

`middleman article <TITLE>`

Your new post will be generated under `source/`. The filename determines the post's URL,
and the title in the YAML at the top of the file is a piece of metadata that can be used
in layouts. More docs [here](https://middlemanapp.com/basics/blogging/).

To add a code block in Markdown, use three tildes `~~~` at the beginning and end.
For some reason, it doesn't seem to indent correctly unless you have a blank line as the first line, like so:

    ~~~

    def hi
      puts "hi"
    end
    ~~~

For a code span, use single backticks around the span: `` `this is code` ``


### Modifying layouts and other meta things

There are zillions of options that can be set in `config.rb`.
You can also add gems.

Layouts with extension `.html.haml` are meant to be standalone pages;
layouts with extension `.haml` are meant to wrap other pages.

Syntax highlighting theme is determined by the name of the CSS file (currently `sunburst.min.css`).
Supported languages are determined by `highlight.pack.js`, which contains a custom set downloaded
from the [highlight.js website](https://highlightjs.org/), and can be replaced if your language of choice isn't being detected.
Refer to the highlight.js website to see all the options for color themes and languages.
