# Hashsum

[![Build](https://img.shields.io/appveyor/ci/Tyrrrz/Hashsum/master.svg)](https://ci.appveyor.com/project/Tyrrrz/Hashsum)
[![Tests](https://img.shields.io/appveyor/tests/Tyrrrz/Hashsum/master.svg)](https://ci.appveyor.com/project/Tyrrrz/Hashsum)
[![NuGet](https://img.shields.io/nuget/v/Hashsum.svg)](https://nuget.org/packages/Hashsum)
[![NuGet](https://img.shields.io/nuget/dt/Hashsum.svg)](https://nuget.org/packages/Hashsum)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FTyrrrz%2FHashsum.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FTyrrrz%2FHashsum?ref=badge_shield)

Hashsum is a library for generating checksums based on arbitrary sets of values. It works by invariantly formatting values into a string buffer and calculating hash based on resulting string.

## Download

- Using NuGet: `Install-Package Hashsum`
- [Continuous integration](https://ci.appveyor.com/project/Tyrrrz/Hashsum)

## Features

- Convenient fluent interface
- Culture and format invariant
- Pluggable hashing algorithm
- Targets .NET Framework 4.5+ and .NET Standard 1.3+
- No external dependencies

## Usage

```c#
var checksum = new ChecksumBuilder()
    .Mutate("hello world")
    .Mutate(12345678)
    .Mutate(10e-5)
    .Mutate(DateTime.Now)
    .Calculate()
    .ToString(); // 4vKHCvfiiF/RLEfiqMnCkzQ8IYGu4K8erlWyzdsvqrU=
```

## Libraries used

- [NUnit](https://github.com/nunit/nunit)

## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FTyrrrz%2FHashsum.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FTyrrrz%2FHashsum?ref=badge_large)