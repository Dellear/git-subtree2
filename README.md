# git-subtree2

Git-subtree help you working with subtree commands. 

This is a copy of [git-subtree](https://github.com/plitex/git-subtree), because the original repository has not been updated for a long time.

This repository just for fix bugs.

Using a subtrees config file, you can clone a project and create all subtree remotes with one command. It also helps working with push/pull commands, adding prefix and branch from config.

## Requeriments

- [NodeJS](https://nodejs.org)
- [Git subtree](https://github.com/git/git/blob/master/contrib/subtree/git-subtree.txt)

## Install

```bash
$ npm install -g git-subtree2
```

## Configuration file

The git-subtree configuration must be stored in subtrees.json file in the project root.

```json
{ 
	"mysubtree" : {
		"localFolder": "subtrees/mysubtree",
		"repository": "https://github.com/username/myrepo.git",
		"branch": "master"
	}
}
```

## Use

```bash
$ gitsbt2 <command>
```

### Init

```bash
$ gitsbt2 init [username]
```

This command creates all remotes from subtrees config and if it's a new project, where subtrees folders are still not created, will fetch from subtree remote and add the subtree.

### Add

```bash
$ gitsbt2 add <subtree> [username]
```

Adds git remote, fetch it and creates the local folder with subtree content.

### Pull

```bash
$ gitsbt2 pull <subtree>
```

Pulls subtree changes from subtree remote. 

### Push

```bash
$ gitsbt2 push <subtree>
```

Pushes subtree changes. 

### Commit

```bash
$ gitsbt2 commit <subtree> <message>
```

Commits subtree pending changes. 
