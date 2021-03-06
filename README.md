## GitLab CI Multi-purpose Runner

This is GitLab CI Multi-purpose Runner repository an **unofficial GitLab CI runner written in Go**, this application run tests and sends the results to GitLab CI.
[GitLab CI](https://about.gitlab.com/gitlab-ci) is the open-source continuous integration server that coordinates the testing.

This project was made as Go learning opportunity. The initial release was created within two days.

[![Build Status](https://travis-ci.org/ayufan/gitlab-ci-multi-runner.svg?branch=master)](https://travis-ci.org/ayufan/gitlab-ci-multi-runner)

### Requirements

**None. This project is designed for the Linux, OS X and Windows operating systems.**

### Features

* Allows to run:
 - multiple jobs concurrently
 - use multiple tokens with multiple server (even per-project)
 - limit number of concurrent jobs per-token
* Jobs can be run:
 - locally
 - using Docker container
 - using Docker container and executing job over SSH
 - connecting to remote SSH server
* Is written in Go and distributed as single binary without any other requirements
* Supports Bash, Windows Batch and Windows PowerShell
* Works on Ubuntu, Debian, OS X and Windows (and anywhere you can run Docker)
* Allows to customize job running environment
* Automatic configuration reload without restart
* Easy to use setup with support for docker, docker-ssh, parallels or ssh running environments
* Enables caching of Docker containers
* Easy installation as service for Linux, OSX and Windows

### Installation

* [Install using Debian/Ubuntu/CentOS/RedHat package (preferred)](docs/install-on-linux.md)
* [Install on OSX (preffered)](docs/install-on-osx.md)
* [Install on Windows (preffered)](docs/install-on-windows.md)
* [Install as Docker Service](docs/install-on-docker.md)
* [Manuall installation (advanced)](docs/install-manually.md)

### Advanced Configuration

* [See advanced configuration options](docs/advanced-configuration.md)
* [See example configuration file](config.toml.example)

### Example integrations

* [Integrate GitLab CE](docs/example-integration-gitlab.md)
* [Integrate GitLab CI](docs/example-integration-gitlab-ci.md)

### Extra projects?

If you want to add another project, token or image simply RE-RUN SETUP. *You don't have to re-run the runner. He will automatically reload configuration once it changes.*

### FAQ

Have any problems. Please [Go To Issues](https://github.com/ayufan/gitlab-ci-multi-runner/issues).

### Changelog

Visit [Changelog](CHANGELOG.md) to view recent changes.

### Help

```bash
$ gitlab-ci-multi-runner --help
NAME:
   gitlab-ci-multi-runner - a GitLab-CI Multi Runner

USAGE:
   gitlab-ci-multi-runner [global options] command [command options] [arguments...]

VERSION:
   dev

AUTHOR:
  Kamil Trzciński - <ayufan@ayufan.eu>

COMMANDS:
   run, r run multi runner service
   install  install service
   uninstall  uninstall service
   start  start service
   stop   stop service
   restart  restart service
   setup, s setup a new runner
   run-single start single runner
   help, h  Shows a list of commands or help for one command
   
GLOBAL OPTIONS:
   --debug      debug mode [$DEBUG]
   --log-level, -l 'info' Log level (options: debug, info, warn, error, fatal, panic)
   --help, -h     show help
   --version, -v    print the version
```

### Future

* It should be simple to add additional executors: DigitalOcean? Amazon EC2?
* Maybe script annotations?

### Author

[Kamil Trzciński](mailto:ayufan@ayufan.eu), 2015, [Polidea](http://www.polidea.com/)

### License

GPLv3
