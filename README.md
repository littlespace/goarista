# Arista Go library [![Build Status](https://travis-ci.org/aristanetworks/goarista.svg?branch=master)](https://travis-ci.org/aristanetworks/goarista) [![codecov.io](http://codecov.io/github/aristanetworks/goarista/coverage.svg?branch=master)](http://codecov.io/github/aristanetworks/goarista?branch=master) [![GoDoc](https://godoc.org/github.com/aristanetworks/goarista?status.png)](https://godoc.org/github.com/aristanetworks/goarista) [![Go Report Card](https://goreportcard.com/badge/github.com/aristanetworks/goarista)](https://goreportcard.com/report/github.com/aristanetworks/goarista)

## areflect

Helper functions to work with the `reflect` package.  Contains
`ForceExport()`, which bypasses the check in `reflect.Value` that
prevents accessing unexported attributes.

## cmd/occlient

Client for the gRPC OpenConfig service for getting and setting the configuration and
state of a network device.

## dscp

Provides `ListenTCPWithTOS()`, which is a replacement for `net.ListenTCP()`
that allows specifying the ToS (Type of Service), to specify DSCP / ECN /
class of service flags to use for incoming connections.

## key

Provides a common type used across various Arista projects, named `key.Key`,
which is used to work around the fact that Go can't let one
use a non-hashable type as a key to a `map`, and we sometimes need to use
a `map[string]interface{}` (or something containing one) as a key to maps.
As a result, we frequently use `map[key.Key]interface{}` instead of just
`map[interface{}]interface{}` when we need a generic key-value collection.

## monitor

A library to help expose monitoring metrics on top of the
[`expvar`](https://golang.org/pkg/expvar/) infrastructure.

## netns

`netns.Do(namespace, cb)` provides a handy mechanism to execute the given
callback `cb` in the given [network namespace](https://lwn.net/Articles/580893/).

## test

This is a [Go](http://golang.org/) library to help in writing unit tests.

## Examples

TBD
