# Deploy the BOSH release

Try this:

```
bosh create-release --force
bosh upload-release
bosh upload-stemcell https://the-ubuntu-bionic-stemcell.tgz # eg. https://storage.googleapis.com/bosh-core-stemcells/1.41/bosh-stemcell-1.41-aws-xen-hvm-ubuntu-bionic-go_agent.tgz
bosh -d hello-world-deployment deploy deployment-manifest.yml
bosh -d hello-world-deployment errands
bosh -d hello-world-deployment run-errand hello-world
```

The last command should output `Hello World`.
