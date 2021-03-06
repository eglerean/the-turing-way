# Code Quality

| Prerequisite                                                                                  | Importance |
| --------------------------------------------------------------------------------------------- | ---------- |
| [Experience with the command line](https://programminghistorian.org/en/lessons/intro-to-bash) | Helpful    |

## Table of contents

1.  [Summary](#summary)
2.  [Static code analysis](#static-code-analysis)
3.  [Code style](#code-style)
    1.  [Automatic code formatters](#automatic-code-formatters)
4.  [Online services providing software quality checks](#online-services-providing-software-quality-checks)

## Summary

There are several ways to improve software quality that require relatively little effort.
By following a coding style, code will be easier for yourself and others to understand and therefore it will contain fewer bugs.
Tools for static code analysis can report bugs as well as style issues without even running the code.

## Static code analysis

Static code analysis tools, also known as linters, can analyze source code and find bugs before your code is executed.
In addition to finding bugs, many of these tools can also help maintain a consistent coding style.
Examples of linter tools include [prospector](https://prospector.readthedocs.io) for Python, [lintr](https://github.com/jimhester/lintr) for R, or [shellcheck](https://www.shellcheck.net) for shell scripts.

## Code style

A coding style is a set of conventions on how to format code.
For instance, what do you call your variables? Do you use spaces or tabs for indentation? Where do you put comments?
Consistently using the same style throughout your code, makes it easier to read.
Code that is easy to read, is easier to understand for yourself as well as potential collaborators.
Therefore adhering to a coding style reduces the risk of mistakes and makes it easier to work together on software.
[Improving software quality, why Coding Style Matters](http://coding.smashingmagazine.com/2012/10/25/why-coding-style-matters/) is a nice article on why coding styles matter and how they increase software quality.

For example, [PEP8](https://www.python.org/dev/peps/pep-0008/) is the most widely used Python coding style.

For commonly used style guides for various programming languages see the [Language Guides](https://guide.esciencecenter.nl/best_practices/language_guides/languages_overview.html).
Google also has a style guide for many languages [google style guide page](https://code.google.com/p/google-styleguide/) that are used in open source projects originating out of Google.

### Automatic formatting

Numerous tools exists to automatically format code such that it follows a certain style.
Using these is highly recommended, as it can save you a lot of time.

[EditorConfig](https://editorconfig.org) is a language independent tool that helps maintain consistent whitespace styles for multiple people working on the same project across various editors.
Most editors support EditorConfig either natively or through a plugin.

In addition to that, there are many language specific tools for automatically formatting code according to a particular style.
For example, [Black](https://black.readthedocs.io) and [yapf](https://pypi.org/project/yapf/) are tools for automatically formatting Python code.
Note that editors often support using these tools directly from the editor.

## Online services providing software quality checks

There are several web services that analyze code and make the quality of the code visible.
Usually these services run one or more static code analysis tools that can also be used from the command line or integrated into your editor on your own computer.
Using a code quality service that integrates with a GitHub/GitLab repository is highly recommended, as it will make it spot and communicate about quality issues in pull requests.

Code quality analysis services are websites that often offer the following features:

- Automaticly analyse your code after pushing it to GitHub/GitLab
- Usually free for open source projects
- Support multiple programming languages, but not every language will have the same level of features
- Grade or score for the quality of all of the code in the repository
- List of issues with the code, grouped by severity
- Drill down to location of issue
- Default list of checks which the service provider finds the best practice
- Can be configured to make the list of checks more strict or relaxed
- Can be configured to ignore files or extensions
- Can read a configuration file from repository
- Track issues over time and send alerts when quality deteriorates
- Optionally reports on code coverage generated by a CI build

For a list of choices see [shields.io](https://shields.io/category/analysis) or [this list of services that are free for open source projects](https://github.com/ripienaar/free-for-dev#code-quality).
