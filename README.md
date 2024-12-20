<h1 align="center">
  hls-m3u8 - HLS m3u8 playlist library
</h1>

![Test](https://github.com/Eyevinn/hls-m3u8/workflows/Go/badge.svg)
![golangci-lint](https://github.com/Eyevinn/mp4ff/workflows/golangci-lint/badge.svg?branch=master)
[![Go Report Card](https://goreportcard.com/badge/github.com/Eyevinn/hls-m3u8)](https://goreportcard.com/report/github.com/Eyevinn/hls-m3u8)
[![license](https://img.shields.io/github/license/Eyevinn/hls-m3u8.svg)](https://github.com/Eyevinn/hls-m3u8/blob/master/LICENSE)

Module hls-m3u8 implements parsing and generation of HLS m3u8 playlists.
HLS is an evolving protocol with multiple versions.
Versions 1-7 are described in [IETF RFC8216][rfc8216], but it has continued
to evolve with new features and versions in Internet Drafts [rfc8216bis][rfc8216bis].

One of the major libraries in Go for parsing and generating HLS playlist,
aka m3u8 files, has been the Github project [grafov/m3u8][grafov].
However, the majority of that code was written up to version 7,and
the library has not been updated in a long time. It was finally
archived in Dec. 2024.

The goal of this library is to provide an up-to-date alternative
to the [m3u8][grafov] library. The aim is to follow the specification
as it involves and add all new elements and do other updates so that
all m3u8 documents from version 3 and forward can be parsed and generated.

During this evolution, the top-level multi-variant playlist changed
name to `Multivariant Playlist` from `Master Playlist` in [rfc8216bis-10][rfc8216bis-10] in 2021. The new name is also what
is used in this library.

Another big change is the introduction of partial segments in
[rfc8216bis-7][rfc8216bis-7] in 2020.


## Installation / Usage

<!--Add clear instructions on how to use the project here -->

## Development

### pre-commit checks

To run checks before any commit is accepted, install [pre-commit][pre-commit] and the run

```sh
> pre-commit install --hook-type commit-msg
```

to set up the automatic tests.



<!--Add clear instructions on how to start development of the project here -->

## Compatibility with grafov/m3u8

This project tries to align to the archived library [grafov/m3u8][grafov] to make the transition
from that library relatively simple. In case there are new tags, attributes, or use cases
like LL-HLS, the same API may not apply. Following more recent versions of the specification
the top-level playlist is now called `MultiVariantPlaylist` instead of `MasterPlaylist`.

## Contributing

See [CONTRIBUTING](CONTRIBUTING.md)

## License

This project is licensed under the MIT License, see [LICENSE](LICENSE).

# Support

Join our [community on Slack](http://slack.streamingtech.se) where you can post any questions regarding any of our open source projects. Eyevinn's consulting business can also offer you:

- Further development of this component
- Customization and integration of this component into your platform
- Support and maintenance agreement

Contact [sales@eyevinn.se](mailto:sales@eyevinn.se) if you are interested.

# About Eyevinn Technology

[Eyevinn Technology](https://www.eyevinntechnology.se) is an independent consultant firm specialized in video and streaming. Independent in a way that we are not commercially tied to any platform or technology vendor. As our way to innovate and push the industry forward we develop proof-of-concepts and tools. The things we learn and the code we write we share with the industry in [blogs](https://dev.to/video) and by open sourcing the code we have written.

Want to know more about Eyevinn and how it is to work here. Contact us at work@eyevinn.se!

[rfc8216]: https://datatracker.ietf.org/doc/html/rfc8216
[rfc8216bis]: https://datatracker.ietf.org/doc/draft-pantos-hls-rfc8216bis/
[rfc8216bis-07]: https://datatracker.ietf.org/doc/html/draft-pantos-hls-rfc8216bis-07
[rfc8216bis-10]: https://datatracker.ietf.org/doc/html/draft-pantos-hls-rfc8216bis-10
[grafov]: https://github.com/grafov/m3u8