# Elasticsearch Box

Packer templates to build a Vagrant Elasticsearch box.

## Synopsis

This script will create a Vagrant box with Elasticsearch installed and with all
of the required libraries.

## Getting Started

There are a couple of things needed for the templates to work.

### Prerequisites

Packer tools need to be installed on your local computer.

#### Packer

Packer installation instructions can be found [here](https://www.packer.io/docs/installation.html).

#### Vagrant

Vagrant installation instructions can be found [here](https://www.vagrantup.com/docs/installation/).

#### Virtualbox

Virtualbox installation instructions can be found [here](https://www.virtualbox.org/wiki/Downloads).

### Installation

Nothing special to be done. Just download the template that you wish to use.

### Usage

In order to create the box using this packer script you need to provide a
few options.

```
Usage:
  packer build [-var 'option=value'] elasticsearch.json
```

#### Script Options
- `app_name` - The application name (default value: "elasticsearch").
- `app_name_ext` - Extra name for the application (default value: "").
- `elasticsearch_version` - Elasticsearch version (default value: "3.9").
- `headless` - Show the console of the machine being built (default value: "true").
- `java_build_number` - Java build number (default value: "11").
- `java_major_version` - Java major version (default value: "8").
- `java_token` - Java link token (default version: "d54c1d3a095b4ff2b6607d096fa80163").
- `java_update_version` - Java update version (default value: "131").
- `system_disk_size` - Size of the disk in MB (default value: "12288").
- `system_domain` - Domain name (default value: "marsh").
- `system_hostname` - Host name (default value: "elasticsearch").
- `system_locale` - Locale for the system (default value: "en_US").
- `system_pwd` - Password for the root and system users (default value: "elasticsearch").
- `system_timezone` - Time zone for the system (default value: "Europe/Lisbon").
- `system_user` - Username of the system user (default value: "pollywog").

## Services

This box will have the following services running.

| Service                                 | Port   | Protocol |
|-----------------------------------------|:------:|:--------:|
| SSH                                     | 22     |    TCP   |
| Elasticsearch RESTful API               | 9200   |    TCP   |
| Elasticsearch Native Transport Protocol | 9300   |    TCP   |

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Versioning

This project uses [SemVer](http://semver.org/) for versioning. For the versions
available, see the [tags on this repository](https://github.com/fscm/packer-vagrant-elasticsearch/tags).

## Authors

* **Frederico Martins** - [fscm](https://github.com/fscm)

See also the list of [contributors](https://github.com/fscm/packer-vagrant-elasticsearch/contributors)
who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE)
file for details
