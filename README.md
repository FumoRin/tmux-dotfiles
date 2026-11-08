# tmux-dotfiles

Personal [tmux](https://github.com/tmux/tmux) configuration based on [Oh my tmux!](https://github.com/gpakosz/.tmux).

## Features & Customizations

- Self-contained configuration based on `gpakosz/.tmux`
- Customized in `tmux.conf.local`:
  - Prefix set to `C-a`
  - Vi mode enabled for status and mode keys (`v`, `y` copy-selection)
  - Mouse mode enabled
  - True color (24-bit) & terminal overrides
  - Synchronized pane toggle (`prefix + S`)
  - Integration with TPM (Tmux Plugin Manager):
    - `tmux-plugins/tmux-copycat`
    - `tmux-plugins/tmux-resurrect`
    - `tmux-plugins/tmux-continuum` (auto-restore enabled)

## Requirements

- `tmux >= 2.6`
- `awk`, `perl`, `sed`, `git`

## Installation / Import

To import this configuration onto a new machine:

### Option 1: XDG Config Directory (`~/.config/tmux`)

```bash
git clone https://github.com/FumoRin/tmux-dotfiles.git ~/.config/tmux
```

### Option 2: Home Directory (`~/.tmux.conf`)

```bash
git clone https://github.com/FumoRin/tmux-dotfiles.git ~/.tmux
ln -s -f ~/.tmux/tmux.conf ~/.tmux.conf
ln -s -f ~/.tmux/tmux.conf.local ~/.tmux.conf.local
```

### Starting Tmux

Start tmux:

```bash
tmux
```

On first launch, Oh my tmux! will automatically bootstrap TPM and install all configured plugins.
