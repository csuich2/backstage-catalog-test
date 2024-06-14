# backstage-catalog-test

This repo contains example catalog-info.yaml files which demonstrate a bug when the path to a catalog-info.yaml file contains the word `blob`.

To reproduce:

* Stand up a Backstage instance with @backstage/create-app
* Open localhost:3000
* Attempt to import the following catalog-info.yaml files and they succeed:
  * [https://github.com/csuich2/backstage-catalog-test/blob/main/catalog-info.good.yaml](https://github.com/csuich2/backstage-catalog-test/blob/main/catalog-info.good.yaml)
  * [https://github.com/csuich2/backstage-catalog-test/blob/main/pkg/foo/catalog-info.yaml](https://github.com/csuich2/backstage-catalog-test/blob/main/pkg/foo/catalog-info.yaml)
* Attempt to import the following catalog-info.yaml files and they fail:
  * [https://github.com/csuich2/backstage-catalog-test/blob/main/catalog-info.bad.yaml](https://github.com/csuich2/backstage-catalog-test/blob/main/catalog-info.bad.yaml)
  * [https://github.com/csuich2/backstage-catalog-test/blob/main/pkg/blob/catalog-info.yaml](https://github.com/csuich2/backstage-catalog-test/blob/main/pkg/blob/catalog-info.yaml)
