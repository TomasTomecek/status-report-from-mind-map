# status-report-from-mind-map

## Maps syntax

Create a dedicated sheet for these reports. It needs to have a special structure:

 1. root nodes are years
 2. children of year nodes are weeks

E.g.

```
* Root node
 * 2015
  * 30
   * ...
  * 31
   * ...
 * 2016
  * 1
   * I fixed this bug
   * implemented that feature
    * link
   * ...
```

And then report for week 1 of 2016 will look like this:

```
* I fixed this bug
* implemented that feature
 * link
* ...
```


## Setup

The script has only a single external dependency:

```
$ pip install mekk.xmind
```


## Usage

Create a file with configuration:

```
$ cat config.json
{
  "from": "me@company.io",
  "to": "boss@company.io",
  "cc": ["optional-address@company.io", "mailing-list@company.io"],
  "map": "/path/to/my/map.xmind",
  "sheet_name": "sheet-name"
}
```

and then just run the script:

```
$ ./generate-status-report
```

By default it expects the configuration file to be available at
`./config.json`, this can be changed easily with option `--config`.

