# Advanced Git

To create a git repository via CLI, initialize a `git repository` using a following command

```bash
  git init
```

The above command will help to create or initialize a git repository

- When you use the following command `ls -ltra` you will see a `.git` folder created here.
- `.git` repository is responsible for tracking and ensuring there are no secrets.

To track the file using `git`

```bash
  git add [file_name]
```

To see what changes are made, the command is :

```bash
  git diff [file_name]
```

After `git add` to commit your changes, you write following command:

```bash
  git commit -m [message]
```

To generate a list of all the commits:

```bash
  git log
```

To push the changes:

```bash
  git push
```

Using `git push`, we can push the entire code to git repository.

The `git push` will initially not work as git repository is created through the CLI and there is no remote reference to this repository as this is the repository that is created through the CLI.

To add remote reference to a git repository:

```bash
  git remote add origin https://github.com/kaustubhchile/git_advance.git
```

Now to push your changes to the `git` repository:

```bash
  git push -u origin master
```
