# Customizing and Modifying Terminal

### Oh-My-Zsh

[ Oh My Zsh ](https://ohmyz.sh/) is a delightful, open source, community-driven framework for managing your Zsh configuration. --Oh My Zsh docs

The Z shell (also known as zsh) is a Unix shell that is built on top of bash with additional features. It's recommended to use zsh over bash. It's also highly recommended to install a framework with zsh as it makes dealing with configuration, plugins and themes a lot nicer. Functionality can be added through a brew command

Starting with macOS Catalina, Macs will now use zsh as the default login shell and interactive shell across the operating system. All newly created user accounts in macOS Catalina will use zsh by default.

To install Z shell:  
`$ brew install zsh`

To install Oh My Zsh:  
`$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

Oh My Zsh allows for non-case sensitive autocompletion of file and file paths by default.

### .zshrc
A Z shell run command file lives in the root directory of your computer. To see the file navigate to the root directory:  
`$ cd ~`

And open the .zshrc file:  
`$ atom .zshrc`

This file can be modified to update the look and functionality of the Z shell.

**Change Themes**  
[ Oh My Zsh Themes ](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) can be changed by updating the variable ZSH_THEME.

`ZSH_THEME="robbyrussell"`

The default theme is "robbyrussell" but Oh My Zsh offers hundreds of other themes. Some themes require additional plugins that can be found on the theme documentation.

**Add Plugins**
Oh My Zsh offers many [ plugins ](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) to add functionality to the terminal. The plugins can slow start up time, so only add what you will use. Many plugins offer keyboard shortcuts for often used commands.

By default, Oh My Zsh offers a git plugin to display branch names. Plugins can be added to the list by space separation, no commas.

Many plugins require additional libraries that can be installed via homebrew.

Example: Chuck Norris plugin

`plugins=(git chucknorris)`

Print a Chuck Norris quote in your terminal. Requires fortune and cowsay for additional functionality.

`$ brew install fortune`
`$ brew install cowsay`
Exit and reopen terminal

`$ chuck`
`$ chuck_cow`

**End of Line Indicator**  
Add the following variable to the `.zshrc` file to change the end of line indicator in terminal. The default is `%` but can be updated with other symbols or emojis.

`PROMPT_EOL_MARK="❤️"`


### Customizing Terminal
Open terminal >> preferences >> click to the `Profiles` tab

Create and name a new profile.

Text:
- font style
- font size
- background color
- highlight color

Window:
- height and width of terminal window

Set the new profile to be the default on open under the `General` tab.
