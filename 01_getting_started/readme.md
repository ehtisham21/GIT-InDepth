**What is Git? 🤔**

Git is a version control system that helps you track changes in your codebase over time. It allows you to collaborate with others, experiment with new features, and maintain a history of your project's development.

**Git Configuration Levels 🔧**

Git has three main configuration levels:

1. **System Level** (also known as Global Level for the system): Applies to all users on the system.
2. **Global Level** (also known as User Level): Applies to the current user.
3. **Local Level** (also known as Repository Level): Applies to the current repository.

**Settings for the Global Level 🌐**

The Global Level settings apply to the current user and are stored in the `~/.gitconfig` file. Here are the settings you can configure at the Global Level:

###1. Set Your Username 👤

`git config --global user.name "Your Name"`

* Set your Git username to identify yourself as the author of commits.

**Example:**

Let's say your name is John Doe. You can set your username using the following command:

```bash
git config --global user.name "John Doe"
```

This will update your `~/.gitconfig` file with the following content:

```ini
[user]
 name = John Doe
```

###2. Set Your Email 📧

`git config --global user.email "your.email@example.com"`

* Set your email address associated with your Git commits.

**Example:**

Let's say your email address is johndoe@example.com. You can set your email using the following command:

```bash
git config --global user.email "johndoe@example.com"
```

This will update your `~/.gitconfig` file with the following content:

```ini
[user]
 name = John Doe
 email = johndoe@example.com
```

###3. Set Your Default Editor 📝

`git config --global core.editor "your_editor"`

* Choose your preferred text editor for Git operations, such as `nano`, `vim`, or `emacs`.

**Example:**

Let's say you prefer to use `nano` as your default editor. You can set it using the following command:

```bash
git config --global core.editor "nano"
```

This will update your `~/.gitconfig` file with the following content:

```ini
[user]
 name = John Doe
 email = johndoe@example.com
[core]
 editor = nano
```

###4. View Your Global Settings 👀

`git config --global --list`

* Display all your Global Level configurations.

**Example:**

You can view your Global Level settings using the following command:

```bash
git config --global --list
```

This will output:

```ini
user.name=John Doe
user.email=johndoe@example.com
core.editor=nano
```