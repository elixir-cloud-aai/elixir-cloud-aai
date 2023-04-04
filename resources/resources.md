# ELIXIR-Cloud & AAI services & applications

[&#8629; Welcome page][welcome-page]

## Guidelines

- [Authentication & Authorization Infrastructure (AAI)][guidelines-aai] [![release_tag][badges-aai-guidelines-release]][guidelines-aai-releases]

## Core services

The following services collectively constitute the core efforts of our team:

| Name | Description | Server-side APIs | Client-side APIs | Status |
| --- | --- | --- | --- | --- |
| [CWLab][apps-cwlab] | Web portal | Custom | [GA4GH WES][specs-ga4gh-wes] | [![release_tag][badges-cwlab-release]][apps-cwlab-releases] |
| [Cloud Registry][apps-cloud-registry] | Service registry | [GA4GH Service Registry][specs-ga4gh-service-registry] | N/A | ![under development][badges-under-development] |
| [TRS-Filer][apps-trs-filer] | Tool registry | [GA4GH TRS][specs-ga4gh-trs] | N/A | ![under development][badges-under-development] |
| [proWES][apps-pro-wes] | Gateway for workflows | [GA4GH WES][specs-ga4gh-wes] | [GA4GH WES][specs-ga4gh-wes] | ![under development][badges-under-development] |
| [cwl-WES][apps-cwl-wes] | Run [CWL][res-cwl] workflows | [GA4GH WES][specs-ga4gh-wes] | [GA4GH TES][specs-ga4gh-tes] | ![under development][badges-under-development] |
| [DRS-Filer][apps-drs-filer] | Data object indexer | [GA4GH DRS][specs-ga4gh-drs] | N/A | ![under development][badges-under-development] |
| [proTES][apps-pro-tes] | Gateway for tasks | [GA4GH WES][specs-ga4gh-tes] | [GA4GH TES][specs-ga4gh-tes] | ![under development][badges-under-development] |
| [TEStribute][apps-testribute] | Task distribution middleware | [Custom][specs-testribute] | [GA4GH TES][specs-ga4gh-wes] | [![release_tag][badges-testribute-release]][apps-testribute-releases] |
| [TESK][apps-tesk] | Execute tasks on [Kubernetes][res-kubernetes] | [GA4GH TES][specs-ga4gh-tes] | N/A | [![release_tag][badges-tesk-release]][apps-tesk-releases] |

## Utilities

In addition to the core services, we are also developing the following
utilities, which currently include clients and mockup services mainly for
testing purposes:

### Clients

| Name | Description | Target API | Status |
| --- | --- | --- | --- |
| [DRS-cli][clients-drs-cli] | DRS client | [GA4GH DRS][specs-ga4gh-drs] | [![release_tag][badges-drs-cli-release]][clients-drs-cli-releases] |
| [TES-cli][clients-tes-cli] | Mock TES client used in [TEStribute][apps-testribute] | [Extended GA4GH TES][specs-mock-tes] | [![release_tag][badges-tes-cli-release]][clients-tes-cli-releases] |
| [TRS-cli][clients-trs-cli] | TRS client | [GA4GH TRS][specs-ga4gh-trs] | [![release_tag][badges-trs-cli-release]][clients-trs-cli-releases] |
| [WES-cli][clients-wes-cli] | WES client | [GA4GH WES][specs-ga4gh-wes] | ![under development][badges-under-development] |

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

### CWLab

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [DKFZ][loc-dkfz], Germany | Master | Yes | Yes | [UI][depl-ui-cwlab-dkfz-master] | [![Status][badges-health-cwlab-master]][depl-ui-cwlab-dkfz-master] |
| [DKFZ][loc-dkfz], Germany | Development | Yes | Yes | [UI][depl-ui-cwlab-dkfz-dev] | [![Status][badges-health-cwlab-dev]][depl-ui-cwlab-dkfz-dev] |
| [DKFZ][loc-dkfz], Germany | Testing | Yes | Yes | [UI][depl-ui-cwlab-dkfz-test] | [![Status][badges-health-cwlab-test]][depl-ui-cwlab-dkfz-test] |

### Cloud Registry

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-cloud-registry-csc-openshift] / [Swagger UI][depl-ui-cloud-registry-csc-openshift] | [![Status][badges-health-cloud-registry-csc-openshift]][depl-ui-cloud-registry-csc-openshift] |

### TRS-Filer

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-trs-filer-csc-openshift] / [Swagger UI][depl-ui-trs-filer-csc-openshift] | [![Status][badges-health-trs-filer-csc-openshift]][depl-ui-trs-filer-csc-openshift] |

### proWES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-pro-wes-csc-openshift] / [Swagger UI][depl-ui-pro-wes-csc-openshift] | [![Status][badges-health-pro-wes-csc-openshift]][depl-ui-pro-wes-csc-openshift] |

### cwl-WES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CERIT-SC][loc-cerit], CZ | [Kubernetes][res-kubernetes] | Yes | Yes | [API][depl-api-cwl-wes-cerit] / [Swagger UI][depl-ui-cwl-wes-cerit] | [![Status][badges-health-cwl-wes-cerit-kubernetes]][depl-ui-cwl-wes-cerit] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-cwl-wes-csc-openshift] / [Swagger UI][depl-ui-cwl-wes-csc-openshift] | [![Status][badges-health-cwl-wes-csc-openshift]][depl-ui-cwl-wes-csc-openshift] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | Yes | [API][depl-api-cwl-wes-csc-rahti] / [Swagger UI][depl-ui-cwl-wes-csc-rahti] | [![Status][badges-health-cwl-wes-csc-rahti]][depl-ui-cwl-wes-csc-rahti] |
| [GRNET][loc-grnet] & [ARC][loc-athrc], Greece | [Kubernetes][res-kubernetes] | Yes | Yes | [API][depl-api-cwl-wes-athrc] / [Swagger UI][depl-ui-cwl-wes-athrc] | [![Status][badges-health-cwl-wes-athrc]][depl-ui-cwl-wes-athrc] |

### DRS-Filer

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-drs-filer-csc-openshift] / [Swagger UI][depl-ui-drs-filer-csc-openshift] | [![Status][badges-health-drs-filer-csc-openshift]][depl-ui-drs-filer-csc-openshift] |

### proTES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-pro-tes-csc-openshift] / [Swagger UI][depl-ui-pro-tes-csc-openshift] | [![Status][badges-health-pro-tes-csc-openshift]][depl-ui-pro-tes-csc-openshift] |

### TEStribute

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | No | No | [API][depl-api-testribute-csc-openshift] / [Swagger UI][depl-ui-testribute-csc-openshift] | [![Status][badges-health-testribute-csc-openshift]][depl-ui-testribute-csc-openshift] |

### TESK

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [CERIT-SC][loc-cerit], CZ | [Kubernetes][res-kubernetes] | Yes | Yes | [API][depl-api-tesk-cerit-kubernetes] / [Swagger UI][depl-ui-tesk-cerit-kubernetes] | [![Status][badges-health-tesk-cerit-kubernetes]][depl-ui-tesk-cerit-kubernetes] |
| [CSC][loc-csc], Finland | [OpenShift][res-openshift] | Yes | No | [API][depl-api-tesk-csc-openshift-2] / [Swagger UI][depl-ui-tesk-csc-openshift-2] | [![Status][badges-health-tesk-csc-openshift-2]][depl-ui-tesk-csc-openshift-2] |
| [EMBL-EBI][loc-ebi], UK | [Kubernetes][res-kubernetes] | Yes | No | [API][depl-api-tesk-ebi-kubernetes] / [Swagger UI][depl-ui-tesk-ebi-kubernetes] | [![Status][badges-health-tesk-ebi-kubernetes]][depl-ui-tesk-ebi-kubernetes] |
| [GRNET][loc-grnet] & [ARC][loc-athrc], Greece | [Kubernetes][res-kubernetes] | Yes | Yes | [API][depl-api-tesk-athrc-kubernetes] / [Swagger UI][depl-api-tesk-athrc-kubernetes] | [![Status][badges-health-tesk-athrc]][depl-api-tesk-athrc-kubernetes] |

### mock-DRS

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [sciCORE][loc-bz], Switzerland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-mock-drs-bz-compose] / [Swagger UI][depl-ui-mock-drs-bz-compose] | [![Status][badges-health-mock-drs-bz-compose]][depl-ui-mock-drs-bz-compose] |

### mock-TES

| Location | Type | TLS | Auth | URL | Health |
| --- | --- | --- | --- | --- | --- |
| [EMBL-EBI][loc-ebi], UK | [Kubernetes][res-kubernetes] | Yes | No | [API][depl-api-mock-tes-ebi-kubernetes] / [Swagger UI][depl-ui-mock-tes-ebi-kubernetes] | [![Status][badges-health-mock-tes-ebi-kubernetes]][depl-ui-mock-tes-ebi-kubernetes] |
| [sciCORE][loc-bz], Switzerland | [Docker Compose][res-docker-compose] | No | No | [API][depl-api-mock-tes-bz-compose] / [Swagger UI][depl-ui-mock-tes-bz-compose] | [![Status][badges-health-mock-tes-bz-compose]][depl-ui-mock-tes-bz-compose] |

[apps-cloud-registry]: <https://github.com/elixir-cloud-aai/cloud-registry>
[apps-cwlab]: <https://github.com/CompEpigen/CWLab>
[apps-cwlab-releases]: <https://github.com/CompEpigen/CWLab/releases>
[apps-cwl-wes]: <https://github.com/elixir-cloud-aai/cwl-WES>
[apps-drs-filer]: <https://github.com/elixir-cloud-aai/drs-filer>
[apps-pro-tes]: <https://github.com/elixir-cloud-aai/proTES>
[apps-pro-wes]: <https://github.com/elixir-cloud-aai/proWES>
[apps-tesk]: <https://github.com/EMBL-EBI-TSI/TESK>
[apps-tesk-releases]: <https://github.com/EMBL-EBI-TSI/tesk-api/releases>
[apps-testribute]: <https://github.com/elixir-cloud-aai/TEStribute>
[apps-testribute-releases]: <https://github.com/elixir-cloud-aai/TEStribute/releases>
[apps-trs-filer]: <https://github.com/elixir-cloud-aai/trs-filer>
[badges-aai-guidelines-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/elixir-aai-guidelines?color=C39BD3>
[badges-cwlab-release]: <https://img.shields.io/github/v/tag/CompEpigen/CWLab?color=C39BD3>
[badges-drs-cli-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/DRS-cli?color=C39BD3>
[badges-tesk-release]: <https://img.shields.io/github/v/tag/EMBL-EBI-TSI/tesk-api?color=C39BD3>
[badges-health-cloud-registry-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fcloud-registry.rahtiapp.fi%2Fga4gh%2Fregistry%2Fv1%2Fui%2F>
[badges-health-cwl-wes-athrc]: <https://img.shields.io/website?url=https%3A%2F%2Fwes-eu.hypatia-comp.athenarc.gr%2Fga4gh%2Fwes%2Fv1%2Fui%2F>
[badges-health-cwl-wes-cerit-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Fwes-prod.cerit-sc.cz%2Fga4gh%2Fwes%2Fv1%2Fui%2F>
[badges-health-cwl-wes-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fwes.rahtiapp.fi%2Fga4gh%2Fwes%2Fv1%2Fui>
[badges-health-cwl-wes-csc-rahti]: <https://img.shields.io/website?url=https%3A%2F%2Fcsc-wes.rahtiapp.fi%2Fga4gh%2Fwes%2Fv1%2Fui%2F>
[badges-health-cwlab-dev]: <https://img.shields.io/website?url=https%3A%2F%2Fcwlab.dev.krini.ingress.rancher.computational.bio%2F>
[badges-health-cwlab-master]: <https://img.shields.io/website?url=https%3A%2F%2Fcwlab.krini.ingress.rancher.computational.bio%2F>
[badges-health-cwlab-test]: <https://img.shields.io/website?url=https%3A%2F%2Fcwlab.testing.krini.ingress.rancher.computational.bio%2F>
[badges-health-drs-filer-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fdrs-filer-test.rahtiapp.fi%2Fga4gh%2Fdrs%2Fv1%2Fui>
[badges-health-mock-drs-bz-compose]: <https://img.shields.io/website?url=http%3A%2F%2F131.152.229.71%2Fga4gh%2Fdrs%2Fv1%2Fui>
[badges-health-mock-tes-bz-compose]: <https://img.shields.io/website?url=http%3A%2F%2F131.152.229.70%2Fga4gh%2Ftes%2Fv1%2Fui>
[badges-health-mock-tes-ebi-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Ftes1.tsi.ebi.ac.uk%2Fmock%2Fga4gh%2Ftes%2Fv1%2Fui%2F>
[badges-health-pro-wes-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fprowes.rahtiapp.fi%2Fga4gh%2Fwes%2Fv1%2Fui>
[badges-health-pro-tes-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Fprotes.rahtiapp.fi%2Fga4gh%2Ftes%2Fv1%2Fui>
[badges-health-tesk-athrc]: <https://img.shields.io/website?url=https%3A%2F%2Ftesk-eu.hypatia-comp.athenarc.gr%2F>
[badges-health-tesk-cerit-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Ftesk-prod.cerit-sc.cz%2F>
[badges-health-tesk-csc-openshift-2]: <https://img.shields.io/website?url=https%3A%2F%2Fcsc-tesk.rahtiapp.fi%2F>
[badges-health-tesk-ebi-kubernetes]: <https://img.shields.io/website?url=https%3A%2F%2Ftes1.tsi.ebi.ac.uk%2Ftes%2Fv1%2Ftasks%2Fservice-info>
[badges-health-testribute-csc-openshift]: <https://img.shields.io/website?url=http%3A%2F%2Ftestribute.rahtiapp.fi%2Fui>
[badges-health-trs-filer-csc-openshift]: <https://img.shields.io/website?url=https%3A%2F%2Ftrs-filer-test.rahtiapp.fi%2Fga4gh%2Ftrs%2Fv2%2Fui>
[badges-tes-cli-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/TES-cli?color=C39BD3>
[badges-testribute-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/TEStribute?color=C39BD3>
[badges-trs-cli-release]: <https://img.shields.io/github/v/tag/elixir-cloud-aai/TRS-cli?color=C39BD3>
[badges-under-development]: <https://img.shields.io/static/v1?label=development&message=active&color=yellowgreen>
[clients-drs-cli]: <https://github.com/elixir-cloud-aai/DRS-cli>
[clients-drs-cli-releases]: <https://github.com/elixir-cloud-aai/DRS-cli/releases>
[clients-tes-cli]: <https://github.com/elixir-cloud-aai/TES-cli>
[clients-tes-cli-releases]: <https://github.com/elixir-cloud-aai/TES-cli/releases>
[clients-trs-cli]: <https://github.com/elixir-cloud-aai/TRS-cli>
[clients-trs-cli-releases]: <https://github.com/elixir-cloud-aai/TRS-cli/releases>
[clients-wes-cli]: <https://github.com/elixir-cloud-aai/WES-cli>
[depl-api-cloud-registry-csc-openshift]: <https://cloud-registry.rahtiapp.fi/ga4gh/registry/v1/>
[depl-api-cwl-wes-athrc]: <https://wes-eu.hypatia-comp.athenarc.gr/ga4gh/wes/v1/>
[depl-api-cwl-wes-cerit]: <https://wes-prod.cerit-sc.cz/ga4gh/wes/v1/>
[depl-api-cwl-wes-csc-openshift]: <https://wes.rahtiapp.fi/ga4gh/wes/v1/>
[depl-api-cwl-wes-csc-rahti]: <https://csc-wes.rahtiapp.fi/ga4gh/wes/v1/>
[depl-api-drs-filer-csc-openshift]: <https://drs-filer-test.rahtiapp.fi/ga4gh/drs/v1/>
[depl-api-mock-drs-bz-compose]: <http://131.152.229.71/ga4gh/drs/v1/>
[depl-api-mock-tes-bz-compose]: <http://131.152.229.70/ga4gh/tes/v1/>
[depl-api-mock-tes-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/mock/ga4gh/tes/v1/>
[depl-api-pro-wes-csc-openshift]: <https://prowes.rahtiapp.fi/ga4gh/wes/v1/>
[depl-api-pro-tes-csc-openshift]: <https://protes.rahtiapp.fi/ga4gh/tes/v1/>
[depl-api-tesk-athrc-kubernetes]: <https://tesk-eu.hypatia-comp.athenarc.gr/>
[depl-api-tesk-cerit-kubernetes]: <https://tesk-prod.cerit-sc.cz/>
[depl-api-tesk-csc-openshift-2]: <https://csc-tesk.rahtiapp.fi/>
[depl-api-tesk-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/tes>
[depl-api-testribute-csc-openshift]: <http://testribute.rahtiapp.fi/>
[depl-api-trs-filer-csc-openshift]: <https://trs-filer-test.rahtiapp.fi/ga4gh/trs/v2/>
[depl-ui-cloud-registry-csc-openshift]: <https://cloud-registry.rahtiapp.fi/ga4gh/registry/v1/ui/>
[depl-ui-cwl-wes-athrc]: <https://wes-eu.hypatia-comp.athenarc.gr/ga4gh/wes/v1/ui/>
[depl-ui-cwl-wes-cerit]: <https://wes-prod.cerit-sc.cz/ga4gh/wes/v1/ui/>
[depl-ui-cwl-wes-csc-openshift]: <https://wes.rahtiapp.fi/ga4gh/wes/v1/ui/>
[depl-ui-cwl-wes-csc-rahti]: <https://csc-wes.rahtiapp.fi/ga4gh/wes/v1/ui/>
[depl-ui-cwlab-dkfz-dev]: <https://cwlab.dev.krini.ingress.rancher.computational.bio/>
[depl-ui-cwlab-dkfz-master]: <https://cwlab.krini.ingress.rancher.computational.bio/>
[depl-ui-cwlab-dkfz-test]: <https://cwlab.testing.krini.ingress.rancher.computational.bio/>
[depl-ui-drs-filer-csc-openshift]: <https://drs-filer-test.rahtiapp.fi/ga4gh/drs/v1/ui/>
[depl-ui-mock-drs-bz-compose]: <http://131.152.229.71/ga4gh/drs/v1/ui/>
[depl-ui-mock-tes-bz-compose]: <http://131.152.229.70/ga4gh/tes/v1/ui/>
[depl-ui-mock-tes-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/mock/ga4gh/tes/v1/ui/>
[depl-ui-pro-wes-csc-openshift]: <https://prowes.rahtiapp.fi/ga4gh/wes/v1/ui/>
[depl-ui-pro-tes-csc-openshift]: <https://protes.rahtiapp.fi/ga4gh/tes/v1/ui/>
[depl-ui-tesk-athrc-kubernetes]: <https://tesk-eu.hypatia-comp.athenarc.gr/>
[depl-ui-tesk-cerit-kubernetes]: <https://tesk-prod.cerit-sc.cz/swagger-ui.html>
[depl-ui-tesk-csc-openshift-2]: <https://csc-tesk.rahtiapp.fi/>
[depl-ui-tesk-ebi-kubernetes]: <https://tes1.tsi.ebi.ac.uk/tes>
[depl-ui-testribute-csc-openshift]: <http://testribute.rahtiapp.fi/ui/>
[depl-ui-trs-filer-csc-openshift]: <https://trs-filer-test.rahtiapp.fi/ga4gh/trs/v2/ui/>
[elixir-aai]: <https://elixir-europe.org/services/compute/aai>
[guidelines-aai]: <https://github.com/elixir-cloud-aai/elixir-aai-guidelines>
[guidelines-aai-releases]: <https://github.com/elixir-cloud-aai/elixir-aai-guidelines/releases>
[loc-athrc]: <https://www.athenarc.gr/>
[loc-bz]: <https://scicore.unibas.ch/>
[loc-csc]: <https://www.csc.fi/>
[loc-dkfz]: <https://www.dkfz.de/en/index.html>
[loc-ebi]: <https://www.ebi.ac.uk/>
[loc-cerit]: <https://www.cerit-sc.cz/>
[loc-athrc]: <https://www.athenarc.gr/>
[loc-grnet]: <https://grnet.gr/>
[mock-apps-drs]: <https://github.com/elixir-cloud-aai/mock-DRS>
[mock-apps-tes]: <https://github.com/elixir-cloud-aai/mock-TES>
[res-cwl]: <https://www.commonwl.org/>
[res-docker-compose]: <https://docs.docker.com/compose/>
[res-kubernetes]: <https://kubernetes.io/>
[res-openshift]: <https://www.openshift.com/>
[res-swagger]: <https://swagger.io/>
[specs-ga4gh-drs]: <https://github.com/ga4gh/data-repository-service-schemas>
[specs-ga4gh-service-registry]: <https://github.com/ga4gh-discovery/ga4gh-service-registry>
[specs-ga4gh-tes]: <https://github.com/ga4gh/task-execution-schemas>
[specs-ga4gh-trs]: <https://github.com/ga4gh/tool-registry-service-schemas>
[specs-ga4gh-wes]: <https://github.com/ga4gh/workflow-execution-service-schemas>
[specs-mock-tes]: <https://github.com/elixir-cloud-aai/mock-TES/blob/dev/mock_tes/specs/schema.task_execution_service.d55bf88.openapi.modified.yaml>
[specs-testribute]: <https://github.com/elixir-cloud-aai/TEStribute/blob/dev/TEStribute/specs/schema.TEStribute.openapi.yaml>
[welcome-page]: ../README.md
