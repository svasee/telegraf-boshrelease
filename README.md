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

Verify the tar file by extracting it and make sure it have the modified changes.

   bosh create-release --version 5.3 --final

   git add releases/telegraf/telegraf-5.3.yml
   git commit -a -m "Creating a final release 5.3"
   bosh create-release releases/telegraf/telegraf-5.3.yml --tarball my-telegraf.tgz

* Upload the /tmp/my-telegraf.tgz to bosh