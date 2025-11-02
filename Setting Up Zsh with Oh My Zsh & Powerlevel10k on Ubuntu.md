
# ⚡ Setting Up Zsh with Oh My Zsh & Powerlevel10k on Ubuntu

Zsh (Z Shell) is a powerful and customizable shell that enhances your command-line experience with better autocompletion, syntax highlighting, and themes.  
This guide walks you through installing **Zsh**, setting up **Oh My Zsh**, and customizing it with the beautiful **Powerlevel10k** theme.

---

## 🧩 Step 1 — Install Zsh

Use the `apt` package manager to install Zsh:

```bash
sudo apt install zsh -y
````

After installation, verify the version:

```bash
zsh --version
```

**Expected output:**

```
zsh 5.8 (x86_64-ubuntu-linux-gnu)
```

---

## 🧾 Step 2 — Verify Zsh Installation

Check if Zsh is available in the list of valid login shells:

```bash
cat /etc/shells
```

If you see `/usr/bin/zsh` in the list, the shell is properly installed.

---

## ⚙️ Step 3 — Set Zsh as Default Shell

Run the following command to make Zsh your default shell:

```bash
chsh -s /usr/bin/zsh
```

Now, **log out and log back in**, or restart your terminal.

Confirm Zsh is set as default:

```bash
echo $SHELL
```

**Expected output:**

```
/usr/bin/zsh
```

---

## 💎 Step 4 — Install Oh My Zsh

Oh My Zsh is an open-source, community-driven framework for managing your Zsh configuration.

Install it using **curl**:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

> 💡 This will install Oh My Zsh in the `~/.oh-my-zsh` directory and create a default `~/.zshrc` configuration file.

---

## 🎨 Step 5 — Change the Zsh Theme to Agnoster

Edit your Zsh configuration file:

```bash
nano ~/.zshrc
```

Find this line:

```bash
ZSH_THEME="robbyrussell"
```

Replace it with:

```bash
ZSH_THEME="agnoster"
```

Save and exit (`Ctrl + O`, `Enter`, `Ctrl + X`).

Open a new terminal to see your updated prompt.

---

## 🔠 Step 6 — Fix Broken Powerline Fonts

If your prompt looks **misaligned or broken**, it’s due to missing fonts.
Install the **Powerline fonts** package:

```bash
sudo apt-get install fonts-powerline -y
```

Now open a new terminal — the prompt should look much cleaner.

> 🖋️ Tip: For the best experience, use a Powerline-compatible font in your terminal preferences (like *Fira Code*, *MesloLGS NF*, or *Hack*).

---

## 🚀 Step 7 — Install Powerlevel10k Theme

Powerlevel10k is a fast, highly customizable theme for Zsh and Oh My Zsh.

Clone the theme into your custom themes folder:

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git \
${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Next, open your `~/.zshrc` and update the theme line:

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Save the file and restart your terminal.

If the **Powerlevel10k configuration wizard** doesn’t start automatically, launch it manually:

```bash
p10k configure
```

Follow the interactive setup to personalize your prompt style, icons, colors, and layout.

---

## ✅ Final Check

Once everything’s configured, open a new terminal.
You should now see a stunning, modern Zsh prompt powered by **Oh My Zsh + Powerlevel10k** 😎

---

## 📸 Example Preview

| Theme             | Description                                          |
| ----------------- | ---------------------------------------------------- |
| **Agnoster**      | Minimal, powerline-style theme                       |
| **Powerlevel10k** | Advanced, ultra-fast, and highly customizable prompt |

> Example (Powerlevel10k):
>
> ```
> <username> <directory> <git branch> → ✨
> ```

---

## 🧠 Bonus Tips

* To list all available Oh My Zsh themes:

  ```bash
  ls ~/.oh-my-zsh/themes
  ```
* To reload configuration without restarting terminal:

  ```bash
  source ~/.zshrc
  ```
* To customize plugins (like git, docker, kubectl), edit `~/.zshrc` and modify:

  ```bash
  plugins=(git docker kubectl)
  ```

---

## 🖤 Credits

* [Zsh Official](https://www.zsh.org/)
* [Oh My Zsh](https://ohmyz.sh/)
* [Powerlevel10k](https://github.com/romkatv/powerlevel10k)
* [Fonts Powerline](https://github.com/powerline/fonts)

---

### 🎉 You’re all set!

Enjoy your sleek, lightning-fast terminal experience with Zsh, Oh My Zsh, and Powerlevel10k!


---

Would you like me to add **screenshots placeholders** (like `![screenshot](assets/terminal.png)`) and format it with emoji headers and badges (e.g. “💻 Works on Ubuntu 20.04+”) to make it **GitHub-portfolio ready**?
```
