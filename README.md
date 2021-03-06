# Culture Amp web team dotfiles

## Requirements

Install [Homebrew](https://brew.sh) on your Mac.

## Installation

### One-step<sup>*</sup> setup

If you’re installing our [shared development environment][shared]:

```sh
brew tap cultureamp/web-team-devtools
brew bootstrap-developer-system
```

*Two-step

[shared]: https://github.com/cultureamp/homebrew-web-team-devtools#bootstrap-developer-system

### Manual setup

Clone the dotfiles repo:

```sh
git clone https://github.com/cultureamp/web-team-dotfiles.git ~/.dotfiles-web-team
```

Install the dotfiles:

```sh
~/.dotfiles-web-team/script/setup
```

## Pulling updates

From time to time, pull down any updates to these dotfiles:

```sh
cd ~/.dotfiles-web-team
git pull
```

Then apply them:

```sh
rcup
```

## Making your own customizations

Put your customizations in dotfiles ending with `.local`:

- `~/.aliases.local`
- `~/.gitconfig.local`
- `~/.zshenv.local`
- `~/.zshrc.local`

For example, your `~/.aliases.local` might look like this:

```
# Personal git shortcuts
alias gs='git status'
alias gd='git diff'
```

Your `~/.gitconfig.local` might look like this:

```
[user]
  name = Tim Riley
  email = your-name@example.com
```

Your `~/.zshenv.local` might look like this:

```
# Use Visual Studio Code as default editor
export VISUAL=code
export EDITOR=$VISUAL
```

### Customizing zsh

You can put additional zsh configuration in the `~/.zsh/configs` directory. This
includes two special subdirectories: `pre`, for files that must be loaded first,
and `post`, for files that must be loaded last.

The `~/.zshrc.local` file is loaded after `~/.zsh/configs`.

## Combine with your personal dotfiles

The `rcrc` configuration in these dotfiles also looks for a separate
`~/.dotfiles` directory. If you create this directory, fill it with your own
dotfiles, then run `rcup`, those dotfiles will be used in combination with (and
in preference to) these ones. See [Tim’s dotfiles][tims-dotfiles] as an example.

[tims-dotfiles]: https://github.com/timriley/dotfiles

## Credits

Thanks to Thoughtbot for [rcm](https://github.com/thoughtbot/rcm) and [their own
dotfiles](https://github.com/thoughtbot/dotfiles), which formed the basis for
this collection.

Thanks to [Icelab](https://icelab.com.au/) for all the the good times we had
while using these dotfiles.

These dotfiles are maintained by the [Culture Amp](https://www.cultureamp.com)
web team.
