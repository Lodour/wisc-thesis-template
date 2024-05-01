# wisc-thesis-template
A Minimum Working Example of the Dissertation Template for UW-Madison.

## What's New

* Easy to use, customize, and debug (there is only one style file)
* You can define and change everything as you like
* Minimal dependency and minimal working example

## Usage

See example PDF at [github](./example.pdf) or [download](https://raw.githubusercontent.com/Lodour/wisc-thesis-template/main/example.pdf).

```latex
\documentclass[12pt,oneside,letterpaper]{memoir}
\usepackage{thesis}

% Use any text & math fonts you like
\usepackage{lmodern}
\usepackage{tgpagella}

% Use any bib style you like
\usepackage{natbib}
\setcitestyle{sort,compress,numbers,square,comma}

% Define thesis information
\title{A Minimum Working Example of the Dissertation Template for UW-Madison}
\author{Student Name}
\department{Computer Sciences}
\deposityear{YYYY}
\defensedate{MM/DD/YYYY}

% Define committee members, you can add more.
\committeemember{Faculty Name, Professor, Computer Sciences}
\committeemember{Faculty Name, Professor, Computer Sciences}
\committeemember{Faculty Name, Associate Professor, Computer Sciences}
\committeemember{Faculty Name, Assistant Professor, Computer Sciences}

% Define frontmatters (comment out if you don't want it)
\dedication{...}

\acknowledgements{
	...
}

\abstract{
  ...
}

\begin{document}

% Make everything before the main thesis
\maketitle
\makefrontmatter

% Your thesis
...

% Use any bib style you like
\bibliographystyle{abbrvnat}
\bibliography{...}

\end{document}
```


## What's Not Working with Previous Templates

Currently, there are three templates available online:
* [GitHub: WI-thesis UW-Madison Dissertation Template](https://github.com/willb/wi-thesis-template)
* [Overleaf: UW-Madison Dissertation Template](https://www.overleaf.com/latex/templates/university-of-wisconsin-madison-dissertation-template/mcvftvhkknkz)
* [Memorial Library Template](https://uwmadison.box.com/s/euyh4u8ffk3evfs30643)

For some unknown reason, all of these packages have several issues:

**1. They hardcoded many formats NOT required by UW-Madison**

As per UW-Maidison's requirement at [web](https://grad.wisc.edu/current-students/doctoral-guide/) or [pdf](https://grad.wisc.edu/wp-content/uploads/sites/329/2023/04/Formatting-Requirements-for-your-Doctoral-Dissertation.pdf), there is no requirement for:
* Putting chapter titles in the header
* Font (the official [sample title page](https://grad.wisc.edu/wp-content/uploads/sites/329/2023/04/Sample-PhD-title-page-2024.pdf) uses Times New Roman)
* A large margin (only required a minimum of 1 inch)
* Reference format
* ...

**2. They used 1.5 spacing, but UW-Madison requires double spacing**

Yet, many deposited dissertations in the past few years passed the formatting check with 1.5 spacing.

I don't know why, but it is better to follow the requirements.

**3. Hard to customize**

* They defined many math and proof environments, which conflict with mine and are hard to dig out
* They defined the math font, which is not friendly for a math-heavy thesis and hard to change
* Too many unnecessary definitions compared with the official requirement
* Too many nested files, which costs me several days to debug


## Acknowledgements

Although previous templates are not working perfectly after these many years, this template referenced a lot of ideas from them:
* https://github.com/willb/wi-thesis-template
* https://uwmadison.box.com/s/euyh4u8ffk3evfs30643
