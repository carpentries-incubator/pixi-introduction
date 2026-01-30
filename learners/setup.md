---
title: Setup
---

## Data Sets

All data used in this lesson will either be downloaded from a long term archive as part of the lesson, or will be provided by the learners.

## GitHub Repository Setup

At the end of this lesson you will have created a personal GitHub repository that contains the information that you've learned.
This gives you version controlled examples that you can take forward with you as references for your own projects.

1. Create a [GitHub account](https://github.com/) if you don't have one yet.
1. Navigate to your GitHub profile (https://github.com/<username>) and click the "+" icon in the upper right hand side to [create a new repository](https://github.com/new).
1. Name the new repository named `introduction-to-pixi`, make it public, and give it a README and an [open source license](https://docs.github.com/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository) (e.g. MIT License).
1. As GitHub requires two-factor authentication, it is highly recommended that you [generate an SSH key pair](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) specifically for GitHub, [add the generated SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account), and then use your SSH keys to connect with GitHub.

::: caution

# What do I do if I don't have Git installed on my machine?

Jump to the next section ("Software Setup") and install Pixi.
Then, run this command (which we'll cover in the lesson) in your terminal

```bash
pixi global install git
```

and you'll have Git installed. :+1:

You can of course install Git in other ways depending on your operating system, but this is straightforward and will work for everyone.

:::

## Software Setup

This lesson will focus on using technology that allows for fully reproducible multi-platform software environments.
[Pixi](https://pixi.sh/latest/), the technology that enables this, is the only tool that needs to be installed in advance of the lesson.

To install Pixi, follow the one-line [installation instructions on the documentation website](https://pixi.sh/latest/#installation) and then [install the shell autocompletions](https://pixi.sh/latest/advanced/installation/#autocompletion) for your respective terminal shell.
See the options below for Linux, macOS, and Windows to get the operating system level commands that are provided in the installation docs.

If you already have Pixi installed, update it to the latest version with

```shell
pixi self-update
```

::: spoiler

### Unix machines (Linux and macOS)

```bash
curl -fsSL https://pixi.sh/install.sh | sh
```

or

```bash
wget -qO- https://pixi.sh/install.sh | sh
```

#### Autocompletions

##### Bash

Add the following to the end of `~/.bashrc`:

```bash
eval "$(pixi completion --shell bash)"
```

##### Zsh

Add the following to the end of `~/.zshrc`:

```zsh
autoload -Uz compinit && compinit  # redundant with Oh My Zsh
eval "$(pixi completion --shell zsh)"
```

##### Fish

Add the following to the end of `~/.config/fish/config.fish`:

```fish
pixi completion --shell fish | source
```

:::

::: spoiler

### Windows

```powershell
powershell -ExecutionPolicy ByPass -c "irm -useb https://pixi.sh/install.ps1 | iex"
```

#### Autocompletions

##### Bash (available through Windows Terminal)

Add the following to the end of `~/.bashrc`:

```bash
eval "$(pixi completion --shell bash)"
```

##### PowerShell

Add the following to the end of `Microsoft.PowerShell_profile.ps1`.
You can check the location of this file by querying the `$PROFILE` variable in PowerShell.
Typically the path is `~\Documents\PowerShell\Microsoft.PowerShell_profile.ps1`.

```powershell
(& pixi completion --shell powershell) | Out-String | Invoke-Expression
```

:::

::: caution

# Optionally disable Apple SIP for your terminal emulator

If you are on macOS, [Apple System Integrity Protection (SIP)](https://en.wikipedia.org/wiki/System_Integrity_Protection) will security scan everything executed in your terminal emulator (and the rest of the computer) the first time you ever use it.
This can add _significant_ runtime overhead for the first time you ever execute any code a bespoke computing environment (e.g. a Pixi environment).
If this overhead becomes problematic, you can disable it for your terminal emulator program by selecting "Settings" → "Privacy & Security" → "Developer Tools" and adding your terminal emulator program of choice.

:::
