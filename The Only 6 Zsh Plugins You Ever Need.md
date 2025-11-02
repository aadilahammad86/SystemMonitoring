
# ⚡ The Only 6 Zsh Plugins You’ll Ever Need

Zsh plugins allow you to customize and supercharge your terminal experience — improving both **appearance** and **functionality**.

However, with thousands of Zsh plugins out there, it’s easy to get lost.  
So here are **the only 6 Zsh plugins you actually need** to become faster and more efficient with the command line.

> 💡 I use these with the [Oh My Zsh](https://ohmyz.sh) framework.  
> If you’re on macOS, check out [iTerm2 + Oh My Zsh](https://catalins.tech/iterm2-oh-my-zsh-supercharge-your-mac-terminal) to take your terminal to the next level.

---

## 🥇 1. Git Plugin

The **Git plugin** comes **pre-installed** with Oh My Zsh and provides dozens of helpful aliases and functions.

Instead of typing:
```bash
git push --set-upstream origin <branch>
````

you can simply type:

```bash
gpsup
```

### 💻 Commonly Used Aliases

| Alias        | Command                                                |
| ------------ | ------------------------------------------------------ |
| `ga`, `gaa`  | `git add`, `git add --all`                             |
| `gco`, `gcb` | `git checkout`, `git checkout -b`                      |
| `gcmsg`      | `git commit --message`                                 |
| `gd`         | `git diff`                                             |
| `gl`         | `git pull`                                             |
| `gp`         | `git push`                                             |
| `gpsup`      | `git push --set-upstream origin $(git_current_branch)` |
| `gst`        | `git status`                                           |

To view all available aliases, check the [Oh My Zsh Git plugin documentation](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git).

You can also add your **own custom aliases** in `~/.zshrc`.

---

## ⚙️ 2. Zsh-Autosuggestions Plugin

The **zsh-autosuggestions** plugin provides intelligent command **autocompletion** based on your command history.

As you type, suggestions appear in a lighter color — simply press → (right arrow) to accept.

### 🔧 Installation

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions \
${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Then edit your `~/.zshrc`:

```bash
plugins=(git zsh-autosuggestions)
```

Apply the changes:

```bash
source ~/.zshrc
```

> 💡 Now, your terminal will remember what you typed and help you repeat commands faster.

---

## 🌈 3. Zsh-Syntax-Highlighting Plugin

This plugin adds **syntax highlighting** to your commands — helping you spot typos before pressing Enter.

Commands turn green when valid and red when invalid, giving instant feedback.

### 🔧 Installation

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git \
${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Update your `~/.zshrc`:

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

Reload:

```bash
source ~/.zshrc
```

> 🎨 Your terminal now looks better and helps you avoid mistakes.

---

## 🧠 4. You-Should-Use Plugin

Can’t remember your aliases?
The **you-should-use** plugin gently reminds you whenever you use a command that has a shortcut available.

For example:

```
You typed: git status
Alias suggestion: gst
```

### 🔧 Installation

```bash
git clone https://github.com/MichaelAquilina/zsh-you-should-use.git \
$ZSH_CUSTOM/plugins/you-should-use
```

Update your `~/.zshrc`:

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting you-should-use)
```

Reload:

```bash
source ~/.zshrc
```

> 🧩 This plugin is a subtle but effective productivity booster.

---

## 🐈 5. Zsh-Bat Plugin

The **zsh-bat** plugin replaces the boring `cat` command with `bat`, which adds **syntax highlighting**, **line numbers**, and **Git integration**.

> ⚠️ Requires the `bat` utility to be installed.

### 🔧 Installation

```bash
git clone https://github.com/fdellwing/zsh-bat.git \
$ZSH_CUSTOM/plugins/zsh-bat
```

Update your `~/.zshrc`:

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting you-should-use zsh-bat)
```

Reload:

```bash
source ~/.zshrc
```

> 🖋️ Output looks beautiful and far more readable than `cat`.

---

## 🧩 6. Node Version Manager (NVM)

The **nvm** plugin integrates [Node Version Manager](https://github.com/nvm-sh/nvm) into your Zsh environment.

It allows you to **easily switch between Node.js versions** right from your terminal.

Once installed, simply add it to your plugins:

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting you-should-use zsh-bat nvm)
```

Reload your shell to activate it:

```bash
source ~/.zshrc
```

> 💡 Perfect for developers juggling multiple Node.js projects.

---

## 🧾 Summary

Here’s a quick overview of the 6 must-have Zsh plugins:

| # | Plugin                      | Purpose                                               |
| - | --------------------------- | ----------------------------------------------------- |
| 1 | **git**                     | Shortcuts and aliases for Git commands                |
| 2 | **zsh-autosuggestions**     | Auto-complete commands based on history               |
| 3 | **zsh-syntax-highlighting** | Syntax highlighting for better readability            |
| 4 | **you-should-use**          | Reminds you of command aliases                        |
| 5 | **zsh-bat**                 | Replaces `cat` with pretty, syntax-highlighted output |
| 6 | **nvm**                     | Manage multiple Node.js versions easily               |

---

## 🧠 Bonus — Common Git Aliases (Oh My Zsh)

| Alias   | Command                                                |
| ------- | ------------------------------------------------------ |
| `gst`   | `git status`                                           |
| `gcmsg` | `git commit -m`                                        |
| `gco`   | `git checkout`                                         |
| `gcb`   | `git checkout -b`                                      |
| `gl`    | `git pull`                                             |
| `gp`    | `git push`                                             |
| `gpsup` | `git push --set-upstream origin $(git_current_branch)` |
| `gcam`  | `git commit -am`                                       |
| `grh`   | `git reset --hard`                                     |
| `gbd`   | `git branch -d`                                        |
| `grv`   | `git remote -v`                                        |
| `gpoat` | `git push origin --all && git push origin --tags`      |

For the full list, see the [Oh My Zsh Git plugin documentation](https://github.com/ohmyzsh/ohmyzsh/blob/master/plugins/git/git.plugin.zsh).

---

## 🧰 Example Plugin Section in `.zshrc`

Here’s what your plugin line might look like after installing everything:

```bash
plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
  you-should-use
  zsh-bat
  nvm
)
```

Reload Zsh to activate all plugins:

```bash
source ~/.zshrc
```

---

## 🖤 Credits

* [Oh My Zsh](https://ohmyz.sh/)
* [zsh-users/zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
* [zsh-users/zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)
* [MichaelAquilina/zsh-you-should-use](https://github.com/MichaelAquilina/zsh-you-should-use)
* [fdellwing/zsh-bat](https://github.com/fdellwing/zsh-bat)
* [NVM Plugin Docs](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/nvm)
* Original Article by [Catalin Pit](https://catalins.tech)

---

## 🎉 Final Thoughts

These 6 plugins will **completely transform your Zsh experience** — making it faster, smarter, and way more enjoyable to use.

> ⚡ Minimal setup, maximum productivity.
> Keep this list handy — you’ll thank yourself later.

```

---

Would you like me to **add emoji section headers**, **GitHub badges** (like “Built with ❤️ using Oh My Zsh”), and **preview image placeholders** (for plugin demos)? It’ll make it look like a polished open-source project README.

