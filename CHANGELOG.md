# 1.1.3
* added value `ingress.backendProtocolAnnotationKey` default to `ingress.kubernetes.io`

# 1.1.2
* Add support for pathType in ingress mappings

# 1.1.1
* Handle `rule[].backend` service yaml schema changes when `ingress.k8sApiVersion = networking.k8s.io/v1` see: https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.19.md#v1190
# 1.1.0
* added value `ingress.k8sApiVersion` default to `networking.k8s.io/v1beta1`
* added value `ingress.pathType` default to nothing, can only be used against k8s 1.18+
* added value `ingress.ingressClassName` defaults to nothing `""`, can only be used against k8s 1.18+
  
# 1.0.12
* change ingress to `networking.k8s.io/v1beta1`
* Added support for `annotations` and `labels` to be defined per ingress mapping `host` array entry

# 1.0.11
* **BREAKING CHANGE:** Changed `ingress.metadata.annotations` and `ingress.metadata.labels` from a list to key-value pairs
* **BREAKING CHANGE:** Fixed `ingress.mappings.hosts.dns.ifTrue.labels` and `ingress.mappings.hosts.dns.else.labels` to be properly named as `ingress.mappings.hosts.dns.ifTrue.annotations` and `ingress.mappings.hosts.dns.else.annotations`

# 1.0.10
Fix default values `ingress.tls` and added `host` level `tls` override for `secretName` and `enabled`

# 1.0.9
Remove `webhook_url` from values, in example only

# 1.0.8
Fix `$targetService` sample handling when building `Ingress` to only sample from actual service bindings for that ingress

# 1.0.7
Scope `contexts` under top level `conduits` in values

# 1.0.6
Fix: Ingress labels, get rid of `externalDns` change to `ingress.mappings.hosts.dns`
Readme updates/ examples

# 1.0.5
Fix: dots to dashes in conduit hook parts names

# 1.0.4
Fix: Ensure `classifier` taken in to account on Hook object names

# 1.0.3
Ensure `classifier` taken in to account on Hook object names

# 1.0.2
Put `host.name` back in the Ingress `name:`

# 1.0.1
Change `Ingress` names to not have `host.name` and account for `classifier`

# 1.0.0
Initial version
