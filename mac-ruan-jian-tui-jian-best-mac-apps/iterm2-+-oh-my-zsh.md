# iTerm2 + Oh My Zsh

![](../.gitbook/assets/iterm-ohmyzsh.png)

In this tutorial, I'm going to show you how I used the "iTerm2 + Oh My Zsh" combined with macos features \(iCloud, Keychain Access\) to make sure we can have a handy/updated/secure command line tool across all my macos devices \(I have a macbook pro in office, macmini in my home\).

## Steps

### iTerm2 + Oh My Zsh overview & installation \[ONLY FOR THE FIRST TIME\]

Please follow this gist [https://gist.github.com/kevin-smets/8568070](https://gist.github.com/kevin-smets/8568070) to have an overview on iTerm2 & Oh My Zsh, and then install the iTerm2 & Oh My Zsh on your macos ONLY FOR THE FIRST TIME.

### Make the configuration iCloud-syncable

* Setup iTerm2 to use the preferences from iCloud storage
* Reorg `~/.profile` and `~/.zshrc` 

### Security Security Security

Always consider to have a more secure way to set your sensitive environment in your command line.

* Keychain Access
* `security` command
* TouchID
* [https://apple.stackexchange.com/questions/311334/replace-password-prompt-with-touch-id-to-read-keychain-password](https://apple.stackexchange.com/questions/311334/replace-password-prompt-with-touch-id-to-read-keychain-password)

### Notification with iTerm "triggers"

![My Triggers settings](../.gitbook/assets/image.png)

It looks like this

![We can identify the &quot;keywords&quot; from the trigger settings.](../.gitbook/assets/image%20%282%29.png)



