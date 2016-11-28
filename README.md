Redis Deployment Template
======================================

This repository acts as an upstream repository of YAML templates for use
in deploying one or more [Redis](https://github.com/cloudfoundry-community/redis-boshrelease)
clusters, via the [Gensis][1] utility.

Redis is a Syslog aggregator, designed to stream all of your BOSH job logs through it
and out via an http/websocket stream.

Creating a new Redis Deployment
======================================

To create a new [Genesis][1]-based deployment of Redis, run

    genesis new deployment --template redis

This will create a new repo called `redis-deployments` for you, and
pull in the `github.com/starkandwayne/redis-deployment` repo as the
`upstream` remote, copying the contents of `global/*` into the new
`redis-deployments` repository.

This allows you to easily diverge from the upstream templates to suit your
environment, yet still be able to pull in changes from upstream down
the road. For example, Redis on AWS.

Amazon EC2 (AWS) Sites
======================================

The `aws` template will set you up with a structure suitable for
deploying Redis to Amazon Web Service's EC2/VPC
infrastructure.

    genesis new site --template aws <name>



Notes
======================================

For more information, check out the [Genesis][1] repo, or `genesis help`.
You can download the Genesis program from [Github][1]



[1]: https://github.com/starkandwayne/genesis
