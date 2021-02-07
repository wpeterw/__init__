+++
title = "Poetry and Azure DevOps"
date = 2021-02-07T14:45:10+01:00
draft = false
tags = ["Python", "Azure DevOps"]
categories = []
+++

categories:
- Python
- Azure Devops
date: "2021-02-07"
description: How to use Poetry with Azure DevOps
slug: python_poetry_with_azure_devops
tags:
- python
- poetry
- azure devops
title: Poetry and Azure DevOps private package repository

Recently I have switched from Pip to Poetry. I use Poetry for both dependency-management and packaging.

How to setup Poetry with a private Azure repository ?

Microsoft instructions to connect to a private package feed:
{{< highlight bash >}}
python -m pip install --upgrade pip

pip install keyring artifacts-keyring
{{< /highlight >}}