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

# Branching

To create a branch from the `main` branch :

```bash
  git checkout -b [branch_name]
```

To check in which branch you are currently on :

```bash
  git branch
```

Then do the necessary changes by editing the file and then `staging` and `commiting` it.

```bash
  vim calculator.sh
  git add calculator.sh
  git commit -m [message]
```

To switch back to the main branch, command is:

```bash
  git checkout main
```

Basically branching is used to separate the branches from `development` branch

## Using `git merge`

Now create a `branch`. Make some changes in the `calculator.sh` and then run the following command.

```bash
  vim calculator.sh
  git add calculator.sh
  git commit -m [message]
```

Then to merge the changes go to the main branch and write the following command ( but before that just go once to the main branch and do some changes to `calculator.sh` ).

The `git log` of the `master` branch is:

![Screenshot 2024-05-12 165805](https://github.com/kaustubhchile/git_practice_test/assets/72078555/761af8ac-d41a-4849-828b-7001d56588c3)

and the `git log` of `subtraction` branch is

![Screenshot 2024-05-12 165918](https://github.com/kaustubhchile/git_practice_test/assets/72078555/8e87658c-b76a-4661-b75b-4754cd9f98f5)

Now to merge the 2 branches:

```bash
  git merge [branch_name]
```

After merging you may again need to `stage and commit` in your `master branch` .

![Screenshot 2024-05-12 170724](https://github.com/kaustubhchile/git_practice_test/assets/72078555/759e028d-2e6e-4b21-9d7a-ff6725872d76)
![Screenshot 2024-05-12 170836](https://github.com/kaustubhchile/git_practice_test/assets/72078555/fb7bbad5-f9be-4ae9-a8be-0599efecf4d3)

## Using `git rebase`

`git log` for `master` branch

![Screenshot 2024-05-12 171814](https://github.com/kaustubhchile/git_practice_test/assets/72078555/0bbed728-fccc-4ba1-82c9-e4d286c8d7ff)
![Screenshot 2024-05-12 171902](https://github.com/kaustubhchile/git_practice_test/assets/72078555/4f7659df-cefc-41e7-89de-8eaa290c2a55)

`git log` for `multiplication` branch:

![Screenshot 2024-05-12 172014](https://github.com/kaustubhchile/git_practice_test/assets/72078555/cb5d6b4d-1310-481a-b3cf-f5f350d8a1d1)

```bash
  git rebase [branch_name]
```

![Screenshot 2024-05-12 172701](https://github.com/kaustubhchile/git_practice_test/assets/72078555/d76bfa27-6391-4b8e-9b5f-3653e2a09ebc)
