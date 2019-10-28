# Pivotal RabbitMQ for Kubernetes docs

## Branches in this Content Repo

The master branch is the tree-trunk, so **always** make changes you want carried forward in this branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

Then, if necessary, immediately cherry-pick/copy any changes that you want to push immediately to production into the appropriate branches listed below:

| Branch Name| Use for… |
|------------| ---------|
| master     | 0.5 (staged here: http://docs-pcf-staging.cfapps.io/rabbitmq-kubernetes/0-n/index.html) |
| 0.4        | 0.4 (live here: http://docs.pivotal.io/rabbitmq-kubernetes/0-4/index.html) | 


[docs-book-rmq-k8s]: https://github.com/pivotal-cf/docs-book-rmq-k8s/blob/master/config.yml


## Book Repo

**docs-book-rmq-k8s** is the book repo:

* **Edge** branch is for the next unreleased version is not yet staged.
But, eventually will be staged at this link:
http://docs-pcf-staging.cfapps.io/rabbitmq-kubernetes/1-n/index.html

* **Master** branch is for the published/live releases listed above.


### Staging Environment

When a commit is made into any of the above branches, the documentation is deployed by
[this concourse build][docs-staging-deploy]. All the supported versions will be accessible on the
[staging website][docs-staging].

[docs-staging]:        http://docs-pcf-staging.cfapps.io/rabbitmq-kubernetes/

### Style Sheet

Use this section to specify spelling of special words for RabbitMQ for Kubernetes:


### Making Your Documentation Changes Live

Click the deploy button in the pipeline! Living the dream :-D

### Contributing Documentation

If there is some documentation to add for an unreleased patch version of RabbitMQ then create a branch off of the **live** branch
you intend to modify and create a pull request against that branch.
After the version that change is targeting is released, the pull request can be merged and will be live
the next time a documentation deployment occurs.

If the documentation is meant to be target several released versions,
then you will need to:
+ create a pull request for each individual minor version
+ or ask the technical writer to cherry-pick to particular branches/versions.

### Partials

Cross-product partials (if any) for **Pivotal RabbitMQ for Kubernetes** are single sourced from the [PCF Docs Partials](https://github.com/pivotal-cf/docs-partials) repository.

### Releasing a New Minor Version

Because **master** is the latest and greatest documentation, the process would be to cut a **x.x-live** branch
for the version that **master** was targeting during that time.
A corresponding section in **config.yml** in the [docs-book-pcfservices][docs-book-pcfservices] repository would also need to be made.

After this point, **master** will then be the target for the next version of the RabbitMQ product.



## Style Guide

This is a word list for terminology and word usage specific to the RabbitMQ for Kubernetes for docs.

| Word | Explanation |
|------|-------------|
| Kuberenetes Operator |This operator refers to an Operator pattern, which is a Kubernetes concept. You can have a container image for the Operator code but it is not an image itself. Always capitalize it to help differentiate the term from the Alana persona operator.|
| service broker |Unless you are specifically refering to the Open Source Service Broker API, do not capitalize service broker.|

