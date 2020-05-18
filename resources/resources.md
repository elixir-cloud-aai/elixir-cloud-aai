# ELIXIR-Cloud & AAI services & applications

[&#8629; Welcome page][welcome-page]

## Guidelines

- [Authentication & Authorization Infrastructure (AAI)][guidelines-aai] [![release_tag][badges-aai-guidelines-release]][guidelines-aai-releases]

## Core services

The following services collectively constitute the core efforts of our team:

| Name | Description | Server-side APIs | Client-side APIs | Status |
| --- | --- | --- | --- | --- |
| [proWES][apps-pro-wes] | Gateway for workflows | [GA4GH WES][specs-ga4gh-wes] | [GA4GH WES][specs-ga4gh-wes] | ![under development][badges-under-development] |
| [cwl-WES][apps-cwl-wes] | Run [CWL][res-cwl] workflows | [GA4GH WES][specs-ga4gh-wes] | [GA4GH TES][specs-ga4gh-tes] | ![under development][badges-under-development] |
| [proTES][apps-pro-tes] | Gateway for tasks | [GA4GH WES][specs-ga4gh-tes] | [GA4GH TES][specs-ga4gh-tes] | ![under development][badges-under-development] |
| [TEStribute][apps-testribute] | Task distribution middleware | [Custom][specs-testribute] | [GA4GH TES][specs-ga4gh-wes] | [![release_tag][badges-testribute-release]][apps-testribute-releases] |
| [TESK][apps-tesk] | Execute tasks on [Kubernetes][res-kubernetes] | [GA4GH TES][specs-ga4gh-tes] | N/A | ![under development][badges-under-development] |

## Utilities

In addition to the core services, we are also developing the following
utilities, which currently include clients and mockup services mainly for
testing purposes:

### Clients

| Name | Description | Target API | Status |
| --- | --- | --- | --- |
| [DRS-cli][clients-drs-cli] | Mock client used in [TEStribute][apps-testribute] | [GA4GH DRS][specs-ga4gh-drs] | [![release_tag][badges-drs-cli-release]][clients-drs-cli-releases] |
| [TES-cli][clients-tes-cli] | Mock client used in [TEStribute][apps-testribute] | [Extended GA4GH TES][specs-mock-tes] | [![release_tag][badges-tes-cli-release]][clients-tes-cli-releases] |
| [WES-cli][clients-wes-cli] | Send workflow run requests | [GA4GH WES][specs-ga4gh-wes] | ![under development][badges-under-development] |

### Services

| Name | Description | API | Status |
| --- | --- | --- | --- |
| [mock-DRS][mock-apps-drs] | Mock service used for [TEStribute][apps-testribute] | [GA4GH DRS][specs-ga4gh-drs] (partially implemented) | ![under development][badges-under-development] |
| [mock-TES][mock-apps-tes] | Mock service used for [TEStribute][apps-testribute] | [Extended GA4GH TES][specs-mock-tes] | ![under development][badges-under-development] |

## Deployments

Below are lists of currently deployed instances of our core and utility
services. You can explore their APIs via [Swagger][res-swagger]-based user
interfaces and even run tests. No guarantees for functionality are made at this
point, and abusers will be blocked.

> **Note:** All of our services support authentication/authorization via
> [ELIXIR AAI][elixir-aai]-based tokens. For testing purposes these are mostly
> disabled. However, this may change at any point, without notice and
> regardless of the value set in field "Auth" in the lists below.

### proWES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-pro-wes-csc-openshift] / [Swagger UI][depl-ui-pro-wes-csc-openshift] | [![Status][badges-health-pro-wes-csc-openshift]][depl-ui-pro-wes-csc-openshift] |

### cwl-WES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-cwl-wes-csc-compose] / [Swagger UI][depl-ui-cwl-wes-csc-compose] | [![Status][badges-health-cwl-wes-csc-compose]][depl-ui-cwl-wes-csc-compose] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-cwl-wes-csc-openshift] / [Swagger UI][depl-ui-cwl-wes-csc-openshift] | [![Status][badges-health-cwl-wes-csc-openshift]][depl-ui-cwl-wes-csc-openshift] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | Yes | [API][depl-api-cwl-wes-csc-rahti] / [Swagger UI][depl-ui-cwl-wes-csc-rahti] | [![Status][badges-health-cwl-wes-csc-rahti]][depl-ui-cwl-wes-csc-rahti] |


### proTES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-pro-tes-csc-compose] / [Swagger UI][depl-ui-pro-tes-csc-compose] | [![Status][badges-health-pro-tes-csc-compose]][depl-ui-pro-tes-csc-compose] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-pro-tes-csc-openshift] / [Swagger UI][depl-ui-pro-tes-csc-openshift] | [![Status][badges-health-pro-tes-csc-openshift]][depl-ui-pro-tes-csc-openshift] |

### TEStribute

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-testribute-csc-compose] / [Swagger UI][depl-ui-testribute-csc-compose] | [![Status][badges-health-testribute-csc-compose]][depl-ui-testribute-csc-compose] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | No | No | [API][depl-api-testribute-csc-openshift] / [Swagger UI][depl-ui-testribute-csc-openshift] | [![Status][badges-health-testribute-csc-openshift]][depl-ui-testribute-csc-openshift] |

### TESK

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-tesk-csc-openshift-2] / [Swagger UI][depl-ui-tesk-csc-openshift-2] | [![Status][badges-health-tesk-csc-openshift-2]][depl-ui-tesk-csc-openshift-2] |
| [EMBL-EBI][loc-ebi], UK | [Kubernetes][res-kubernetes] | Yes | No | [API][depl-api-tesk-ebi-kubernetes] / [Swagger UI][depl-ui-tesk-ebi-kubernetes] | [![Status][badges-health-tesk-ebi-kubernetes]][depl-ui-tesk-ebi-kubernetes] |
| [CERIT-SC][cerit-sc], CZ | [Kubernetes][res-kubernetes] | Yes | Yes | [API][depl-api-tesk-cerit-kubernetes] / [Swagger UI][depl-ui-tesk-cerit-kubernetes] | [![Status][badges-health-test-cerit-kubernetes]][depl-ui-tesk-cerit-kubernetes] |

### mock-DRS

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-mock-drs-csc-compose] / [Swagger UI][depl-ui-mock-drs-csc-compose] | [![Status][badges-health-mock-drs-csc-compose]][depl-ui-mock-drs-csc-compose] |
| [sciCORE][loc-bz], Switzerland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-mock-drs-bz-compose] / [Swagger UI][depl-ui-mock-drs-bz-compose] | [![Status][badges-health-mock-drs-bz-compose]][depl-ui-mock-drs-bz-compose] |

### mock-TES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-mock-tes-csc-compose] / [Swagger UI][depl-ui-mock-tes-csc-compose] | [![Status][badges-health-mock-tes-csc-compose]][depl-ui-mock-tes-csc-compose] |
| [EMBL-EBI][loc-ebi], UK | [Kubernetes][res-kubernetes] | Yes | No | [API][depl-api-mock-tes-ebi-kubernetes] / [Swagger UI][depl-ui-mock-tes-ebi-kubernetes] | [![Status][badges-health-mock-tes-ebi-kubernetes]][depl-ui-mock-tes-ebi-kubernetes] |
| [sciCORE][loc-bz], Switzerland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-mock-tes-bz-compose] / [Swagger UI][depl-ui-mock-tes-bz-compose] | [![Status][badges-health-mock-tes-bz-compose]][depl-ui-mock-tes-bz-compose] |

[badges-aai-guidelines-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/elixir-aai-guidelines?color=C39BD3>
[badges-drs-cli-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/DRS-cli?color=C39BD3>
[badges-health-cwl-wes-csc-compose]: <https://img.shields.io/website?url=http%3A%2F%2F193.167.189.73%3A7777%2Fga4gh%2Fwes%2Fv1%2Fui>
[badges-health-cwl-wes-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fwes.c03.k8s-popup.csc.fi%2Fga4gh%2Fwes%2Fv1%2Fui>
[badges-health-cwl-wes-csc-rahti]: <https://img.shields.io/website?url=https%3A%2F%2Fcsc-wes.rahtiapp.fi%2Fga4gh%2Fwes%2Fv1%2Fui%2F>
[badges-health-mock-drs-bz-compose]: <https://img.shields.io/website?url=http%3A%2F%2F131.152.229.71%2Fga4gh%2Fdrs%2Fv1%2Fui>
[badges-health-mock-drs-csc-compose]: <https://img.shields.io/website?url=http%3A%2F%2F193.166.24.114%2Fga4gh%2Fdrs%2Fv1%2Fui>
[badges-health-mock-tes-bz-compose]: <https://img.shields.io/website?url=http%3A%2F%2F131.152.229.70%2Fga4gh%2Ftes%2Fv1%2Fui>
[badges-health-mock-tes-csc-compose]: <https://img.shields.io/website?url=http%3A%2F%2F193.166.24.111%2Fga4gh%2Ftes%2Fv1%2Fui>
[badges-health-mock-tes-ebi-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Ftes1.tsi.ebi.ac.uk%2Fmock%2Fga4gh%2Ftes%2Fv1%2Fui%2F>
[badges-health-pro-tes-csc-compose]: <https://img.shields.io/website?url=http%3A%2F%2F86.50.252.55:7878%2Fga4gh%2Ftes%2Fv1%2Fui>
[badges-health-pro-tes-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fprotes.c03.k8s-popup.csc.fi%2Fga4gh%2Ftes%2Fv1%2Fui>
[badges-health-pro-wes-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fprowes.c03.k8s-popup.csc.fi%2Fga4gh%2Fwes%2Fv1%2Fui>
[badges-health-test-cerit-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Felixir-tesk2.cerit-sc.cz%2F>
[badges-health-tesk-csc-openshift-2]: <https://img.shields.io/website?url=https%3A%2F%2Fcsc-tesk.c03.k8s-popup.csc.fi%2F>
[badges-health-tesk-ebi-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Ftes1.tsi.ebi.ac.uk%2Ftes>
[badges-health-testribute-csc-compose]: <https://img.shields.io/website?url=http%3A%2F%2Fvm2051.kaj.pouta.csc.fi:7979%2Fui>
[badges-health-testribute-csc-openshift]: <https://img.shields.io/website?url=http%3A%2F%2Ftestribute.c03.k8s-popup.csc.fi%2Fui>
[badges-tes-cli-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/TES-cli?color=C39BD3>
[badges-testribute-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/TEStribute?color=C39BD3>
[badges-under-development]: <https://img.shields.io/static/v1?label=development&message=active&color=yellowgreen>
[cerit-sc]: <https://www.cerit-sc.cz/>
[clients-drs-cli]: <https://github.com/elixir-cloud-aai/DRS-cli>
[clients-drs-cli-releases]: <https://github.com/elixir-cloud-aai/DRS-cli/releases>
[clients-tes-cli]: <https://github.com/elixir-cloud-aai/TES-cli>
[clients-tes-cli-releases]: <https://github.com/elixir-cloud-aai/TES-cli/releases>
[clients-wes-cli]: <https://github.com/elixir-cloud-aai/WES-cli>
[elixir-aai]: <https://elixir-europe.org/services/compute/aai>
[apps-cwl-wes]: <https://github.com/elixir-cloud-aai/cwl-WES>
[apps-pro-tes]: <https://github.com/elixir-cloud-aai/proTES>
[apps-pro-wes]: <https://github.com/elixir-cloud-aai/proWES>
[apps-tesk]: <https://github.com/EMBL-EBI-TSI/TESK>
[apps-testribute]: <https://github.com/elixir-cloud-aai/TEStribute>
[apps-testribute-releases]: <https://github.com/elixir-cloud-aai/TEStribute/releases>
[depl-api-cwl-wes-csc-compose]: <http://193.167.189.73:7777/ga4gh/wes/v1/>
[depl-api-cwl-wes-csc-openshift]: <https://wes.c03.k8s-popup.csc.fi/ga4gh/wes/v1/>
[depl-api-cwl-wes-csc-rahti]: <https://csc-wes.rahtiapp.fi/ga4gh/wes/v1/>
[depl-api-mock-drs-bz-compose]: <http://131.152.229.71/ga4gh/drs/v1/>
[depl-api-mock-drs-csc-compose]: <http://193.166.24.114/ga4gh/drs/v1/>
[depl-api-mock-tes-bz-compose]: <http://131.152.229.70/ga4gh/tes/v1/>
[depl-api-mock-tes-csc-compose]: <http://193.166.24.111/ga4gh/tes/v1/>
[depl-api-mock-tes-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/mock/ga4gh/tes/v1/>
[depl-api-pro-tes-csc-compose]: <http://86.50.252.55:7878/ga4gh/tes/v1/>
[depl-api-pro-tes-csc-openshift]: <https://protes.c03.k8s-popup.csc.fi/ga4gh/tes/v1/>
[depl-api-pro-wes-csc-openshift]: <https://prowes.c03.k8s-popup.csc.fi/ga4gh/wes/v1/>
[depl-api-tesk-cerit-kubernetes]: <https://elixir-tesk2.cerit-sc.cz/>
[depl-api-tesk-csc-openshift-2]: <https://csc-tesk.c03.k8s-popup.csc.fi/>
[depl-api-tesk-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/tes>
[depl-api-testribute-csc-compose]: <http://vm2051.kaj.pouta.csc.fi:7979/>
[depl-api-testribute-csc-openshift]: <http://testribute.c03.k8s-popup.csc.fi/>
[depl-ui-cwl-wes-csc-compose]: <http://193.167.189.73:7777/ga4gh/wes/v1/ui/>
[depl-ui-cwl-wes-csc-openshift]: <https://wes.c03.k8s-popup.csc.fi/ga4gh/wes/v1/ui/>
[depl-ui-cwl-wes-csc-rahti]: <https://csc-wes.rahtiapp.fi/ga4gh/wes/v1/ui/>
[depl-ui-mock-drs-bz-compose]: <http://131.152.229.71/ga4gh/drs/v1/ui/>
[depl-ui-mock-drs-csc-compose]: <http://193.166.24.114/ga4gh/drs/v1/ui/>
[depl-ui-mock-tes-bz-compose]: <http://131.152.229.70/ga4gh/tes/v1/ui/>
[depl-ui-mock-tes-csc-compose]: <http://193.166.24.111/ga4gh/tes/v1/ui/>
[depl-ui-mock-tes-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/mock/ga4gh/tes/v1/ui/>
[depl-ui-pro-tes-csc-compose]: <http://86.50.252.55:7878/ga4gh/tes/v1/ui/>
[depl-ui-pro-tes-csc-openshift]: <https://protes.c03.k8s-popup.csc.fi/ga4gh/tes/v1/ui/>
[depl-ui-pro-wes-csc-openshift]: <https://prowes.c03.k8s-popup.csc.fi/ga4gh/wes/v1/ui/>
[depl-ui-tesk-cerit-kubernetes]: <https://elixir-tesk2.cerit-sc.cz/>
[depl-ui-tesk-csc-openshift-2]: <https://csc-tesk.c03.k8s-popup.csc.fi/>
[depl-ui-tesk-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/tes>
[depl-ui-testribute-csc-compose]: <http://vm2051.kaj.pouta.csc.fi:7979/ui/>
[depl-ui-testribute-csc-openshift]: <http://testribute.c03.k8s-popup.csc.fi/ui/>
[guidelines-aai]: <https://github.com/elixir-cloud-aai/elixir-aai-guidelines>
[guidelines-aai-releases]: <https://github.com/elixir-cloud-aai/elixir-aai-guidelines/releases>
[loc-bz]: <https://scicore.unibas.ch/>
[loc-csc]: <https://www.csc.fi/>
[loc-ebi]: <https://www.ebi.ac.uk/>
[mock-apps-drs]: <https://github.com/elixir-cloud-aai/mock-DRS>
[mock-apps-tes]: <https://github.com/elixir-cloud-aai/mock-TES>
[res-cwl]: <https://www.commonwl.org/>
[res-docker-compose]: <https://docs.docker.com/compose/>
[res-kubernetes]: <https://kubernetes.io/>
[res-openshift]: <https://www.openshift.com/>
[res-swagger]: <https://swagger.io/>
[specs-ga4gh-drs]: <https://github.com/ga4gh/data-repository-service-schemas>
[specs-ga4gh-tes]: <https://github.com/ga4gh/task-execution-schemas>
[specs-ga4gh-wes]: <https://github.com/ga4gh/workflow-execution-service-schemas>
[specs-mock-tes]: <https://github.com/elixir-cloud-aai/mock-TES/blob/dev/mock_tes/specs/schema.task_execution_service.d55bf88.openapi.modified.yaml>
[specs-testribute]: <https://github.com/elixir-cloud-aai/TEStribute/blob/dev/TEStribute/specs/schema.TEStribute.openapi.yaml>
[welcome-page]: ../README.md
