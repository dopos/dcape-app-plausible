# dcape-app-plausible

[![GitHub Release][1]][2] [![GitHub code size in bytes][3]]() [![GitHub license][4]][5]

[1]: https://img.shields.io/github/release/dopos/dcape-app-plausible.svg
[2]: https://github.com/dopos/dcape-app-plausible/releases
[3]: https://img.shields.io/github/languages/code-size/dopos/dcape-app-plausible.svg
[4]: https://img.shields.io/github/license/dopos/dcape-app-plausible.svg
[5]: LICENSE

[plausible](https://plausible.io/) application package for [dcape](https://github.com/dopos/dcape).

## Docker image used

* [plausible/analytics](https://hub.docker.com/r/plausible/analytics)

## Requirements

* linux 64bit (git, make, wget, gawk, openssl)
* [docker](http://docker.io)
* [dcape](https://github.com/dopos/dcape)
* Git service ([github](https://github.com), [gitea](https://gitea.io) or [gogs](https://gogs.io))

## Usage

* Fork this repo in your Git service
* Setup deploy hook
* Run "Test delivery" (config sample will be created in dcape)
* Edit and save config (enable deploy etc)
* Run "Test delivery" again (app will be installed and started on webhook host)

See also: [Deploy setup](https://github.com/dopos/dcape/blob/master/DEPLOY.md) (in Russian)

## License

The MIT License (MIT), see [LICENSE](LICENSE).

Copyright (c) 2023 Aleksei Kovrizhkin <lekovr+dopos@gmail.com>
