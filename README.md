# CLI URL-Encoder
This URL Encoder is a script meant to be used by penetration testers to perform filter evasion directly from CLI, quickly and without any overhead.

The reason why I built this tool is that most URL encoders online simply encode backslashes and spaces, leaving out other non alphanumeric characters such as the dot.
Furthermore, having a quick, simple cli function makes everything more convinient, so I thought I might as well share it for fellow pentesters to use.

## Installation
Installation is fairly straightforward. This script is currently available for both `zsh` and `bash`. Just download the file corresponding to your preferred shell (find out either with `echo $SHELL` if set or with a simple `ps`) and put it into your `*.d` folder.
For example, for `zsh`, the folder is located at `$HOME/.zsh.d`.

Although generally considered bad practice (because it can become messy in the long term), you can as well simply copy the function from GitHub directly into the `.bashrc` or `.zshrc` files and it would still work the same.

## Usage
Here are some usage examples:
```bash
$ urlencode "Hello.World!"
Hello%2EWorld%21

$ urlencode "a_b-c~d"
a%5Fb%2Dc%7Ed

$ echo "foo.bar/baz?" | urlencode
foo%2Ebar%2Fbaz%3F

```
