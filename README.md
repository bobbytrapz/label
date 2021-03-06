A simple labeling utility in one file that only depends on the standard library.

**Work is still in progress and it is not well tested.**

It's not pretty either.

I want to support video labeling in the future.

## Install

Just save [label](/label?raw=true) to where you need it.

## Important notes

Please keep in mind files are moved while labeling. You probably want to keep a backup of your data before labeling.

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

The labeled image is moved to the directory matching its label.

If you only want to label unlabeled things:

```
label --unlabeled data
```

For convenience, you can pack up the labeled data by running:

```
label data --pack dataset.tar.gz
```
