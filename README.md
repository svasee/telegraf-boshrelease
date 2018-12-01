# Telegraf BOSH Release

A [BOSH](https://bosh.io) release for deploying [Telegraf](https://github.com/influxdata/telegraf).

## Usage

See [the `telegraf` job spec](jobs/telegraf/spec).

Commands to compile:

 * Git clone this repo
 * Change directory to this repo
 * Make a changes to /jobs/telegraf/spec and /jobs/telegraf/template/telegraf.conf.erb
 * Commit the changes
 * Create a release
   bosh create-release --tarball /tmp/my-telegraf.tgz
   bosh create-release --final

* Upload the /tmp/my-telegraf.tgz to bosh