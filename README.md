A simple labeling utility in one file that only depends on the standard library.

It's not pretty but it should work. Work is still in progress it is not well tested.

I want to support video labeling in the future.

## Install

Just copy [label](/label?raw=true) to where you need it.

## Important notes

Please keep in mind files are moved while labeling. You probably want to keep a backups.

To give a unique filename to all the unlabeled files run:

```
label --rename data
```

## Usage

The directory structure for your data should look like this:

```
data/
  _unlabeled/ -- unlabeled things in here (leading '_' means unlabeled)
  _also_unlabeled -- there can be as many unlabeled directories as you want
  yes/ -- directory for things labeled 'yes'
  no/ -- directory for things labeled 'no'
```

To begin label run:

```
label data
```

A UI should appear and you can begin labeling.

The labeled image is copied to the directory matching its label.

If you only want to label unlabeled things:

```
label --unlabeled data
```

For convenience, you can pack up the labeled data by running:

```
label data --pack dataset.tar.gz
```
