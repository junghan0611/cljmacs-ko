# Command Line Shell with Spacemacs

A simple shell can be run with the `shell` function.  This `shell` function opens a new buffer with a shell prompt and displays that buffer, replacing the currently highlighted buffer.

`SPC '` to popup a shell buffer in the root of the user account. Consecutive presses toggle the shell popup buffer for quick access.

`SPC p '` displays a popup buffer in the project directory.

Use the `exit` command to close the shell.


## Adding the shell layer

Add the **shell** layer to `dotspacemacs-configuration-layers` section of `~/.spacemacs`. Or `SPC SPC eshell` will prompt to install the shell package if its not currently added.

The shell popup is configured in the `dotspacemacs-configure-layers` section of the `~/.spacemacs` file.

```
(shell :variables
       shell-default-height 30
       shell-default-position 'bottom)
```

`shell-default-position` can be top, bottom, left or right.

`shell-default-height` defines the percentage of the Spacemacs frame to use.


## Customising eshell prompt

Practicalli created a custom Eshell prompt.  The code can be found in the [practicalli/spacemacs.d](https://github.com/practicalli/spacemacs.d/blob/master/init.el#L872-L994) configuration, the [Eshell custom code in `dotspacemacs/user-config` section](https://github.com/practicalli/spacemacs.d/blob/live/init.el#L1110-L1206).

![Spacemacs Eshell custom prompt](https://raw.githubusercontent.com/practicalli/graphic-design/live/spacemacs/screenshots/spacemacs-shell-poppup.png)


## Configure shell to use multi-term

multi-term uses the default shell from the operating system.

Set the `shell-default-shell` variable to `'multi-term` in the shell layer in the `~/.spacemacs` file.

Here is an example with the multi-term shell set, along with popup size and location

```
     (shell :variables
            shell-default-shell 'multi-term
            shell-default-height 30
            shell-default-position 'bottom)
```

`M-m '` now opens a shell buffer as a popup with the default shell of your operating system terminal.


# Configure multi-term to use zsh

I have [zsh configured for my terminal window](http://jr0cket.co.uk/2013/09/hey-prezto-zsh-for-command-line-heaven.html) which uses [prezto](https://github.com/sorin-ionescu/prezto) to provide extra shell features.

Add the following to `dotspacemacs/user-config` in your `~/.spacemacs` file

```
(setq multi-term-program "/usr/bin/zsh")
```

`SPC f s` to save the `~/.spacemacs` file.

`SPC f e R` to reload the configuration, or `SPC q r` to restart Spacemacs.

![Spacemacs Shell - Multi-term zsh](/image/spacemacs-shell-popup-multi-term-zsh.png)