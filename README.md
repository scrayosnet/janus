![The official Logo of Janus](.github/images/logo.png "Janus")

![A visual badge for the latest release](https://img.shields.io/github/v/release/scrayosnet/janus "Latest Release")
![A visual badge for the version](https://img.shields.io/github/go-mod/go-version/scrayosnet/janus "Go Version")
![A visual badge for the code quality](https://img.shields.io/scrutinizer/quality/g/scrayosnet/janus "Code Quality")
![A visual badge for the coverage](https://img.shields.io/scrutinizer/coverage/g/scrayosnet/janus "Coverage")
![A visual badge for the license](https://img.shields.io/github/license/scrayosnet/janus "License")

Janus is a Minecraft SHARD[^1] world updater and migration tool that can be used to convert files in the SHARD (Shard
Highly Augmented Region Data) format between different [Minecraft versions][minecraft-versions] and can be run as a job
within [Kubernetes][kubernetes].

*The name "Janus" is derived from the Roman god of beginnings, gates, transitions, time, duality, doorways, passages,
frames and endings ([source][name-source]). That alludes to the idea of Janus looking into the future and past and this
software being able to migrate from past versions to future versions.*

## Motivation

The SHARD format was developed to allow for blazing-fast loading and easy modifications of Minecraft worlds. It was
designed to act as both world and schematic without any modifications and therefore has unique characteristics. To
further speed up loading of worlds, no migration is performed ad-hoc.

Janus is the responsible software for migrating SHARD files across different Minecraft and SHARD schema versions. It is
built with scaling and clusters in mind and can be used as a command line tool for easy conversions. Having a separate
software for the migration simplifies the implementation on the runtime platforms. Updates can be properly logged and
are therefore reproducible. This is especially convenient, as the SHARD format is read-only and conversion would
otherwise happen each time, the instance is restarted.

## Major Features

* Migrate SHARD files from one Minecraft version to another by modifying as little as possible.
* Save time on ad-hoc conversions by updating all SHARDs in advance.
* Perform dry-runs to see which changes are required between versions.
* Run Janus as a job within [Kubernetes][kubernetes] to update the files automatically.
* Hook up different data sources for retrieval and storage of SHARD files.

## Getting started

Once this project is ready, information about how to run Janus will be published here. Stay tuned!

## Reporting Security Issues

To report a security issue for this project, please note our [Security Policy][security-policy].

## Code of Conduct

Participation in this project comes under the [Contributor Covenant Code of Conduct][code-of-conduct].

## How to contribute

Thanks for considering contributing to this project! In order to submit a Pull Request, please read
our [contributing][contributing-guide] guide. This project is in active development, and we're always happy to receive
new contributions!

## License

This project is developed and distributed under the MIT License. See [this explanation][mit-license-doc] for a rundown
on what that means.

[minecraft-versions]: https://minecraft.fandom.com/wiki/Version_history

[kubernetes]: https://kubernetes.io/

[name-source]: https://en.wikipedia.org/wiki/Janus

[minetools-docs]: https://api.minetools.eu/

[grpc-docs]: https://grpc.io/

[rest-docs]: https://en.wikipedia.org/wiki/Representational_state_transfer

[security-policy]: SECURITY.md

[code-of-conduct]: CODE_OF_CONDUCT.md

[contributing-guide]: CONTRIBUTING.md

[mit-license-doc]: https://choosealicense.com/licenses/mit/

[^1]: The SHARD format was developed by ScrayosNET and will be released at a later point in time. It was inspired by
the SLIME format of Hypixel and the Sponge Schematic format.
