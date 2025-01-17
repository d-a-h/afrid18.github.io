---
title: "GSoC: Week3"
date: 2023-06-21T17:59:05+05:30
Description: "My third week at Google Summer of Code 2023 at OpenSUSE"
thumbnail: "images/post5/week3.png"
Tags: ["OpenSUSE", "Open Source", "Google", "Summer of Code"]
Categories: ["Open source", "Programming"]
Series:
  - "gsoc-weekly-report"
DisableComments: false
---

Hello I am back again with my another GSoC weekly report and in this blog post I will share what I worked on the previous week, which is 3rd week of Google Summer of Code!

As discussed in the previous [previous post], my mentor and I have decided to go with extending implementation of `FakePkg` class, just to keep everything simple. Whereas with mocking, it would be hard to mock every inner piece of functions and other required binary operations. Which eventually consume more design to `Pkg` class itself and this approach will also take more time. However, there a big scope to the project and hence there might be improvements in future.

[previous post]: /post/week2-at-gsoc/

> If you haven't been following or confused, here is the reference to the overview of the project I am working on: [project overview]

[project overview]: https://github.com/openSUSE/mentoring/issues/189

This week, I have made decent progress, also I was able to eliminate 5 following binary rpm packages

1. `rpmlint/test/binary/pythoncheck-python-doc-in-package-0-0.x86_64.rpm`
2. `rpmlint/test/binary/pythoncheck-python-doc-module-in-package-0-0.x86_64.rpm`
3. `rpmlint/test/binary/pythoncheck-python-doc-in-site-packages-0-0.x86_64.rpm`
4. `rpmlint/test/binary/pythoncheck-python-src-in-site-packages-0-0.x86_64.rpm`
5. `rpmlint/test/binary/pythoncheck-python-tests-in-site-packages-0-0.x86_64.rpm`

{{% notice info %}}

> These binary packages are basically built to have source directory, test directory and docs directories in them so that to test for python packages that have src, test and docs directories. And now, these were eliminated with mocking strategy.

{{% /notice %}}

Here is the commit **[db63a42](https://github.com/afrid18/rpmlint/commit/db63a4226b2fc50e169dca348fb5aa9a256fccc9)** if you are interested.

Looking ahead to the coming week, my plan is to focus on developing more complex tests and, hopefully, work alongside my mentor to create some well-designed and effective mocked tests.

<h1 align="center"> Thank you </h1>

links:
- [previous post]
- [project overview]

---
