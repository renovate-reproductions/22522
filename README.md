# renovate-depName-mismatch-repro

Reproduction repo for depName mismatch issue

The root cause of the issue was an incorrect version regexp (not allowing the + sign) which was translating into confusing depName mismatch message when trying to apply the version change (`12.1.0+2.7.7`)

```
DEBUG: depName mismatch (branch="renovate/cloudfoundry-haproxy-boshrelease-12.x")
{
"manager": "regex"
"packageFile": "coab-depls/root-deployment.yml"
"currentDepName": "cloudfoundry/haproxy-boshrelease"
"newDepName": "orange-cloudfoundry/helm-kubectl-boshrelease"
}
```
