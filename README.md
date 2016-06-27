# status-report-from-mind-map

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

