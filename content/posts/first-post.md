---
title: "Poetry and Azure DevOps private package repository"
description: "How to use Poetry with Azure DevOps"
date: "2021-02-07"
categories:
tags:
  - "python"
  - "poetry"
  - "azure devops"
---

Recently I have switched from Pip to Poetry. I use Poetry for both dependency-management and packaging.

How to setup Poetry with a private Azure repository ?

Microsoft instructions to connect to a private package feed (using pip):
{{< highlight bash >}}
python -m pip install --upgrade pip

pip install keyring artifacts-keyring
{{< /highlight >}}

Configure the repository in pip.ini:
{{< highlight bash >}}
[global]
extra-index-url=https://pkgs.dev.azure.com/your_organisation_name/_packaging/Python/pypi/simple/
{{< /highlight >}}

Now when you do a pip install for a package in your local repository you will be presented with an authentication url where you enter the authentication-code.
Now Microsoft's artifacts-keyring is used to find the credentials.


