# hexo-series

A hexo plugin for writing article series. 

## Features

* Article series management
* Article series index page
* Navigation widgets

## Install

Run:

```shell
$ npm install hexo-series --save
```

## Usage

### Interactive console

You can enter hexo-series interactive console by:

```
$ hexo series
```

Notice that the prompt has become:

```
series>
```

Exit:
```
series> exit
```

### Create a new series

Say that you want to write a article series on subject **foo**.

```
series> create foo "An Introduction to Foo"
``` 

There are two arguments for `create` command (left to right order):

Argument | Description | Example
-------- | ----------- | -------
Alias    | Short and memorable name for a series. Used to identify a series in all commands | foo
Main title | The main title of this series surrounded with `"` | "An Introduction to Foo" 

### List all series

Run:

```
series> list
```

You will get a list of all series and their progress.

### Work on a series

To work on a series, you will first enter its workspace by:

```
series> begin foo
```

The prompt will become:

```
series[foo]>
```

There is one argument for `begin` command:

Argument | Description | Example
-------- | ----------- | -------
Alias | Short and memorable name for a series. Used to identify a series in all commands | foo

You can complete serveral tasks in this workspace (see following sections). When you are done, exit this workspace by:

```
series[foo]> end
```

### Make plans

(TBD)

### Start Writing

(TBD)

### Navigation Widget and Index Page

The naviagtion widget provides a menu of artiles in one sereies and is displayed in each articles. 

It can be automatically inserted at the start or at the end of one article. You can configure this behaviour by:

```
TBD
TBD
```

Or you can manually insert tag ```{% series_nav %}``` anywhere inside the article.

A index page of all article series will be genereated at URL `/series.html`. The generator first searches for `series.ejs` in your current theme's `layout` folder as the template. If the file does not exist, it fall back to `archieve.ejs`. 

## API For Theme Developer

(TBD)
