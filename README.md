# remic
Vulnerability Scanner for Detecting Publicly Disclosed Vulnerabilities in Application Dependencies

# Usage

```
$ remic -h
NAME:
  remic - A simple and fast tool for detecting vulnerabilities in application dependencies
USAGE:
  remic [options] file
VERSION:
  0.0.2
OPTIONS:
  --format value, -f value    format (table, json) (default: "table")
  --severity value, -s value  severity of vulnerabilities to be displayed (default: "UNKNOWN,LOW,MEDIUM,HIGH,CRITICAL")
  --output value, -o value    output file name
  --exit-code value           Exit code when vulnerabilities were found (default: 0)
  --skip-update               skip db update
  --ignore-unfixed            display only fixed vulnerabilities
  --debug, -d                 debug mode
  --help, -h                  show help
  --version, -v               print the version
```

# Vulnerability Detection
## Application Dependencies

`Remic` automatically detects the following files in the container and scans vulnerabilities in the application dependencies.

- Gemfile.lock
- Pipfile.lock
- composer.lock
- package-lock.json
- yarn.lock
- Cargo.lock

The path of these files does not matter.

Example: https://npm.pkg.github.com/knqyf263/trivy-ci-test/blob/master/Dockerfile