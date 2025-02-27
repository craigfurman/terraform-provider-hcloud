Terraform Provider for the Hetzner Cloud
==================
[![GitHub release](https://img.shields.io/github/tag/terraform-providers/terraform-provider-hcloud.svg?label=release)](https://github.com/terraform-providers/terraform-provider-hcloud/releases/latest) [![Build Status](https://travis-ci.org/terraform-providers/terraform-provider-hcloud.svg?branch=master)](https://travis-ci.org/terraform-providers/terraform-provider-hcloud)

- Website: https://www.terraform.io
- Documentation: https://www.terraform.io/docs/providers/hcloud/index.html

<img src="https://cdn.rawgit.com/hashicorp/terraform-website/master/content/source/assets/images/logo-hashicorp.svg" width="600px">

Requirements
------------

-	[Terraform](https://www.terraform.io/downloads.html) 0.11.x
-	[Go](https://golang.org/doc/install) 1.11 (to build the provider plugin)

Building the provider
---------------------

Clone repository to: `$GOPATH/src/github.com/terraform-providers/terraform-provider-hcloud`

```sh
$ mkdir -p $GOPATH/src/github.com/terraform-providers; cd $GOPATH/src/github.com/terraform-providers
$ git clone https://github.com/terraform-providers/terraform-provider-hcloud.git
```

Enter the provider directory and build the provider

```sh
$ cd $GOPATH/src/github.com/terraform-providers/terraform-provider-hcloud
$ make build
```

Using the provider
----------------------

if you are building the provider, follow the instructions to [install it as a plugin](https://www.terraform.io/docs/plugins/basics.html#installing-a-plugin). After placing it into your plugins directory, run `terraform init` to initialize it.

Developing the provider
---------------------------

If you wish to work on the provider, you'll first need [Go](http://www.golang.org) installed on your machine (version 1.11+ is *required*). You'll also need to correctly setup a [GOPATH](http://golang.org/doc/code.html#GOPATH), as well as adding `$GOPATH/bin` to your `$PATH`.

To compile the provider, run `make build`. This will build the provider and put the provider binary in the `$GOPATH/bin` directory.

```sh
$ make build
...
$ ./bin/terraform-provider-hcloud
...
```

In order to test the provider, you can simply run `make test`.

```sh
$ make test
```

In order to run the full suite of Acceptance tests run `make testacc`.

*Note:* Acceptance tests create real resources, and often cost money to run.

```
$ make testacc
```
