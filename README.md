# 🔌 TCPeasy - Connecting sockets

`TCPeasy` provides you with a TCP server socket and a TCP client socket to
jump-start your TCP projects. It comes with a TCP message parser that extracts
messages from your TCP data stream.

`TCPeasy.Cli` is a dotnet console application that can run in server mode or
client mode and is using the TCP message parser to allow you to send UTF8
messages from a server to multiple clients or from a client to a server.

[![CI](https://github.com/sschmid/TCPeasy/actions/workflows/ci.yml/badge.svg)](https://github.com/sschmid/TCPeasy/actions/workflows/ci.yml)
[![Coverage Status](https://coveralls.io/repos/github/sschmid/TCPeasy/badge.svg)](https://coveralls.io/github/sschmid/TCPeasy)
[![NuGet](https://img.shields.io/nuget/dt/TCPeasy)](https://www.nuget.org/packages?q=TCPeasy)
[![License: MIT](https://img.shields.io/github/license/sschmid/TCPeasy)](https://github.com/sschmid/TCPeasy/blob/main/LICENSE.md)
[![Twitter](https://img.shields.io/twitter/follow/s_schmid)][twitter-sschmid]

# Install

|             | NuGet                                                                                              | Unity Packages on [OpenUPM](https://openupm.com)                                                                                                                                    |
|:------------|:---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TCPeasy     | [![NuGet](https://img.shields.io/nuget/v/TCPeasy)](https://www.nuget.org/packages/TCPeasy)         | [![openupm](https://img.shields.io/npm/v/com.sschmid.tcpeasy?label=com.sschmid.tcpeasy&registry_uri=https://package.openupm.com)](https://openupm.com/packages/com.sschmid.tcpeasy) |
| TCPeasy.Cli | [![NuGet](https://img.shields.io/nuget/v/TCPeasy.Cli)](https://www.nuget.org/packages/TCPeasy.Cli) |                                                                                                                                                                                     |

Automated Unity Package Releases: https://github.com/sschmid/com.sschmid.tcpeasy

# Quick Start

Check out the `TCPeasy.Cli` project which contains the `ListenCommand` and
the `ConnectCommand` which starts the console app in either server or client mode.

### See [TCPeasy.Cli](https://github.com/sschmid/TCPeasy/tree/main/src/TCPeasy.Cli)

# Demo

Run `TCPeasy.Cli` and give it a try!

Start the server by listening on a port, e.g. `12345`

```
dotnet run --project src/TCPeasy.Cli/TCPeasy.Cli.csproj listen 12345
```

Connect clients to an IP address on a specific port, e.g. `localhost` on port `12345`

```
dotnet run --project src/TCPeasy.Cli/TCPeasy.Cli.csproj connect localhost 12345
```

![TCPeasy-Server-Clients](https://github.com/sschmid/TCPeasy/raw/main/readme/TCPeasy-Server-Clients.png)

Use the `-v` option for verbose output

```
dotnet run --project src/TCPeasy.Cli/TCPeasy.Cli.csproj -- listen -v 12345
```

```
dotnet run --project src/TCPeasy.Cli/TCPeasy.Cli.csproj -- connect -v localhost 12345
```

# Maintainer(s)
[@sschmid on GitHub][github-sschmid] - [@s_schmid on Twitter][twitter-sschmid]

[github-sschmid]: https://github.com/sschmid "@sschmid"
[twitter-sschmid]: https://twitter.com/intent/follow?original_referer=https%3A%2F%2Fgithub.com%2Fsschmid%2FTCPeasy&screen_name=s_schmid&tw_p=followbutton "s_schmid on Twitter"
