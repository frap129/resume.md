# resume.md

![Resume](resume.png)

Write your resume in
[Markdown](https://raw.githubusercontent.com/mikepqr/resume.md/main/resume.md),
style it with [CSS](resume.css), output to [HTML](resume.html) and
[PDF](resume.pdf).

## Prerequisites

 - Python ≥ 3.6
 - python-venv
 - [python-markdown](https://python-markdown.github.io/)
 - [weasyprint](https://doc.courtbouillon.org/weasyprint/stable/#)

## Usage

 1. Clone this repository
 2. Create a venv with necessary dependencies
     1. `python -m venv .venv`
     2. `source .venv/bin/activate`
     3. `pip install -r requirements.txt`
 2. Edit [resume.md](resume.md) (the placeholder text is taken with thanks from
    the [JSON Resume Project](https://jsonresume.org/themes/))

 3. Run `python3 resume.py` to build resume.html and resume.pdf.

     - Use `--no-html` or `--no-pdf` to disable HTML or PDF output.

## Customization

Edit [resume.css](resume.css) to change the appearance of your resume. The
default style is extremely generic, which is perhaps what you want in a resume,
but CSS gives you a lot of flexibility. See, e.g. [The Tech Resume
Inside-Out](https://www.thetechinterview.com/) for good advice about what a
resume should look like (and what it should say).

Change the appearance of the PDF version (without affecting the HTML version) by
adding rules under the `@media print` CSS selector.

Change the margins and paper size of the PDF version by editing the [`@page` CSS
rule](https://developer.mozilla.org/en-US/docs/Web/CSS/%40page/size).

[python-markdown](https://python-markdown.github.io/) is by default a very basic
markdown compiler, but it has a number of optional extensions that you may want
to enable (by adding to [the list of extensions
here](https://github.com/mikepqr/resume.md/blob/f1b0699a9b66833cb67bb59111f45a09ed3c0f7e/resume.py#L112)).
<code><a
href="https://python-markdown.github.io/extensions/attr_list/">attr_list</a></code>
in particular may by useful if you are editing the CSS.
[abbreviations](https://python-markdown.github.io/extensions/abbreviations/)
extension is already enabled.
