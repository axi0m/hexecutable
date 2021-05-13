---
title: "Rich"
date: 2021-05-13T06:40:46-05:00
draft: false
---

If you find yourself constantly creating command-line interfaces and have not heard of [rich](https://github.com/willmcgugan/rich), take a few hours next week and play with it!

Historically I've used `termcolor` and `colorama` to handle the pretty terminal colors in Python programs I write but now that I've discovered `rich` I'm not sure I'll ever go back. The project is well-maintained, feature rich and Will the author seems to have put a lot of effort into it.

## Install

I prefer to use `pipenv` but you can use normal `pip` or `poetry` too of course.

```python
pip install rich
pipenv install rich
```

## Usage

This is mentioned in detail on the README for Rich but this was the most immediately useful example I took away for my CLI programs.

```python
from rich.console import Console

console = Console()

console.print(f'[+] Building the mechtronics matrix splicer...', style="bold green")
```

In addition there is a wonderful `track()` function you can use to wrap around an iterator and have rich progress bars in your console. I have used this in some non-public programs but have yet to add it to anything that's on my GitHub repos or Gists.

## Replacing Tabulate

I [blogged](https://kevindienst.blog/posts/tabulate/) about using the package `tabulate` previously when I developed a small API client to interact with AWS EC2 resources using `boto3` but after finding the `rich` package I think I'm goint to explore using its table rendering features instead.

## References

- [Rich](https://github.com/willmcgugan/rich)
- [RealPython](https://realpython.com/command-line-interfaces-python-argparse/)
- [Termcolor](https://termcolor.readthedocs.io/)
- [Colorama](https://github.com/tartley/colorama)
