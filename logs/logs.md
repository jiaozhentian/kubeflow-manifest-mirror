### cert-manager
```
kubectl kustomize common/cert-manager/cert-manager/base | kubectl apply -f -
kubectl kustomize common/cert-manager/kubeflow-issuer/base | kubectl apply -f -
```
namespace/cert-manager created
customresourcedefinition.apiextensions.k8s.io/certificaterequests.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/certificates.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/challenges.acme.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/clusterissuers.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/issuers.cert-manager.io created
customresourcedefinition.apiextensions.k8s.io/orders.acme.cert-manager.io created
serviceaccount/cert-manager created
serviceaccount/cert-manager-cainjector created
serviceaccount/cert-manager-webhook created
role.rbac.authorization.k8s.io/cert-manager-webhook:dynamic-serving created
role.rbac.authorization.k8s.io/cert-manager-cainjector:leaderelection created
role.rbac.authorization.k8s.io/cert-manager:leaderelection created
clusterrole.rbac.authorization.k8s.io/cert-manager-cainjector created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-approve:cert-manager-io created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-certificates created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-challenges created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-clusterissuers created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-ingress-shim created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-issuers created
clusterrole.rbac.authorization.k8s.io/cert-manager-controller-orders created
clusterrole.rbac.authorization.k8s.io/cert-manager-edit created
clusterrole.rbac.authorization.k8s.io/cert-manager-view created
clusterrole.rbac.authorization.k8s.io/cert-manager-webhook:subjectaccessreviews created
rolebinding.rbac.authorization.k8s.io/cert-manager-webhook:dynamic-serving created
rolebinding.rbac.authorization.k8s.io/cert-manager-cainjector:leaderelection created
rolebinding.rbac.authorization.k8s.io/cert-manager:leaderelection created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-cainjector created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-approve:cert-manager-io created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-certificates created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-challenges created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-clusterissuers created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-ingress-shim created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-issuers created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-controller-orders created
clusterrolebinding.rbac.authorization.k8s.io/cert-manager-webhook:subjectaccessreviews created
service/cert-manager created
service/cert-manager-webhook created
deployment.apps/cert-manager created
deployment.apps/cert-manager-cainjector created
deployment.apps/cert-manager-webhook created
mutatingwebhookconfiguration.admissionregistration.k8s.io/cert-manager-webhook created
validatingwebhookconfiguration.admissionregistration.k8s.io/cert-manager-webhook created

clusterissuer.cert-manager.io/kubeflow-self-signing-issuer created

### Istio
```
kubectl kustomize common/istio-1-9/istio-crds/base | kubectl apply -f -
kubectl kustomize common/istio-1-9/istio-namespace/base | kubectl apply -f -
kubectl kustomize common/istio-1-9/istio-install/base | kubectl apply -f -
```
customresourcedefinition.apiextensions.k8s.io/authorizationpolicies.security.istio.io created
customresourcedefinition.apiextensions.k8s.io/destinationrules.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/envoyfilters.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/gateways.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/istiooperators.install.istio.io created
customresourcedefinition.apiextensions.k8s.io/peerauthentications.security.istio.io created
customresourcedefinition.apiextensions.k8s.io/requestauthentications.security.istio.io created
customresourcedefinition.apiextensions.k8s.io/serviceentries.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/sidecars.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/virtualservices.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/workloadentries.networking.istio.io created
customresourcedefinition.apiextensions.k8s.io/workloadgroups.networking.istio.io created

namespace/istio-system created

serviceaccount/istio-ingressgateway-service-account created
serviceaccount/istio-reader-service-account created
serviceaccount/istiod-service-account created
role.rbac.authorization.k8s.io/istio-ingressgateway-sds created
role.rbac.authorization.k8s.io/istiod-istio-system created
clusterrole.rbac.authorization.k8s.io/istio-reader-istio-system created
clusterrole.rbac.authorization.k8s.io/istiod-istio-system created
rolebinding.rbac.authorization.k8s.io/istio-ingressgateway-sds created
rolebinding.rbac.authorization.k8s.io/istiod-istio-system created
clusterrolebinding.rbac.authorization.k8s.io/istio-reader-istio-system created
clusterrolebinding.rbac.authorization.k8s.io/istiod-istio-system created
configmap/istio created
configmap/istio-sidecar-injector created
service/istio-ingressgateway created
service/istiod created
deployment.apps/istio-ingressgateway created
deployment.apps/istiod created
envoyfilter.networking.istio.io/metadata-exchange-1.8 created
envoyfilter.networking.istio.io/metadata-exchange-1.9 created
envoyfilter.networking.istio.io/stats-filter-1.8 created
envoyfilter.networking.istio.io/stats-filter-1.9 created
envoyfilter.networking.istio.io/tcp-metadata-exchange-1.8 created
envoyfilter.networking.istio.io/tcp-metadata-exchange-1.9 created
envoyfilter.networking.istio.io/tcp-stats-filter-1.8 created
envoyfilter.networking.istio.io/tcp-stats-filter-1.9 created
envoyfilter.networking.istio.io/x-forwarded-host created
gateway.networking.istio.io/istio-ingressgateway created
authorizationpolicy.security.istio.io/global-deny-all created
authorizationpolicy.security.istio.io/istio-ingressgateway created
Warning: admissionregistration.k8s.io/v1beta1 MutatingWebhookConfiguration is deprecated in v1.16+, unavailable in v1.22+; use admissionregistration.k8s.io/v1 MutatingWebhookConfiguration
mutatingwebhookconfiguration.admissionregistration.k8s.io/istio-sidecar-injector created
Warning: admissionregistration.k8s.io/v1beta1 ValidatingWebhookConfiguration is deprecated in v1.16+, unavailable in v1.22+; use admissionregistration.k8s.io/v1 ValidatingWebhookConfiguration
validatingwebhookconfiguration.admissionregistration.k8s.io/istiod-istio-system created

### Dex
```
kubectl kustomize common/dex/overlays/istio | kubectl apply -f -
```
namespace/auth created
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/authcodes.dex.coreos.com created
serviceaccount/dex created
Warning: rbac.authorization.k8s.io/v1beta1 ClusterRole is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 ClusterRole
clusterrole.rbac.authorization.k8s.io/dex created
Warning: rbac.authorization.k8s.io/v1beta1 ClusterRoleBinding is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 ClusterRoleBinding
clusterrolebinding.rbac.authorization.k8s.io/dex created
configmap/dex created
secret/dex-oidc-client created
service/dex created
deployment.apps/dex created
virtualservice.networking.istio.io/dex created

### OIDC AuthService
```
kubectl kustomize common/oidc-authservice/base | kubectl apply -f -
```
configmap/oidc-authservice-parameters created
secret/oidc-authservice-client created
service/authservice created
persistentvolumeclaim/authservice-pvc created
statefulset.apps/authservice created
envoyfilter.networking.istio.io/authn-filter created

### Knative
```
kubectl apply -f patch/knative_serving_releases_download_v0.17.1_serving-crds.yam
kubectl kustomize common/knative/knative-serving/base | kubectl apply -f -
kubectl kustomize common/istio-1-9/cluster-local-gateway/base | kubectl apply -f -
```

customresourcedefinition.apiextensions.k8s.io/certificates.networking.internal.knative.dev created
customresourcedefinition.apiextensions.k8s.io/configurations.serving.knative.dev created
customresourcedefinition.apiextensions.k8s.io/ingresses.networking.internal.knative.dev created
customresourcedefinition.apiextensions.k8s.io/metrics.autoscaling.internal.knative.dev created
customresourcedefinition.apiextensions.k8s.io/podautoscalers.autoscaling.internal.knative.dev created
customresourcedefinition.apiextensions.k8s.io/revisions.serving.knative.dev created
customresourcedefinition.apiextensions.k8s.io/routes.serving.knative.dev created
customresourcedefinition.apiextensions.k8s.io/serverlessservices.networking.internal.knative.dev created
customresourcedefinition.apiextensions.k8s.io/services.serving.knative.dev created
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/images.caching.internal.knative.dev created

namespace/knative-serving created
customresourcedefinition.apiextensions.k8s.io/certificates.networking.internal.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/configurations.serving.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/images.caching.internal.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/ingresses.networking.internal.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/metrics.autoscaling.internal.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/podautoscalers.autoscaling.internal.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/revisions.serving.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/routes.serving.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/serverlessservices.networking.internal.knative.dev configured
customresourcedefinition.apiextensions.k8s.io/services.serving.knative.dev configured
serviceaccount/controller created
clusterrole.rbac.authorization.k8s.io/knative-serving-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/knative-serving-admin created
clusterrole.rbac.authorization.k8s.io/knative-serving-core created
clusterrole.rbac.authorization.k8s.io/knative-serving-istio created
clusterrole.rbac.authorization.k8s.io/knative-serving-namespaced-admin created
clusterrole.rbac.authorization.k8s.io/knative-serving-namespaced-edit created
clusterrole.rbac.authorization.k8s.io/knative-serving-namespaced-view created
clusterrole.rbac.authorization.k8s.io/knative-serving-podspecable-binding created
clusterrolebinding.rbac.authorization.k8s.io/knative-serving-controller-admin created
configmap/config-autoscaler created
configmap/config-defaults created
configmap/config-deployment created
configmap/config-domain created
configmap/config-features created
configmap/config-gc created
configmap/config-istio created
configmap/config-leader-election created
configmap/config-logging created
configmap/config-network created
configmap/config-observability created
configmap/config-tracing created
secret/istio-webhook-certs created
secret/webhook-certs created
service/knative-local-gateway created
service/activator-service created
service/autoscaler created
service/controller created
service/istio-webhook created
service/webhook created
deployment.apps/activator created
deployment.apps/autoscaler created
deployment.apps/controller created
deployment.apps/istio-webhook created
deployment.apps/networking-istio created
deployment.apps/webhook created
Warning: policy/v1beta1 PodDisruptionBudget is deprecated in v1.21+, unavailable in v1.25+; use policy/v1 PodDisruptionBudget
poddisruptionbudget.policy/activator-pdb created
poddisruptionbudget.policy/webhook-pdb created
horizontalpodautoscaler.autoscaling/activator created
horizontalpodautoscaler.autoscaling/webhook created
image.caching.internal.knative.dev/queue-proxy created
destinationrule.networking.istio.io/knative created
gateway.networking.istio.io/knative-local-gateway created
authorizationpolicy.security.istio.io/activator-service created
authorizationpolicy.security.istio.io/autoscaler created
authorizationpolicy.security.istio.io/controller created
authorizationpolicy.security.istio.io/istio-webhook created
authorizationpolicy.security.istio.io/webhook created
peerauthentication.security.istio.io/domainmapping-webhook created
peerauthentication.security.istio.io/istio-webhook created
peerauthentication.security.istio.io/webhook created
mutatingwebhookconfiguration.admissionregistration.k8s.io/webhook.istio.networking.internal.knative.dev created
mutatingwebhookconfiguration.admissionregistration.k8s.io/webhook.serving.knative.dev created
validatingwebhookconfiguration.admissionregistration.k8s.io/config.webhook.istio.networking.internal.knative.dev created
validatingwebhookconfiguration.admissionregistration.k8s.io/config.webhook.serving.knative.dev created
validatingwebhookconfiguration.admissionregistration.k8s.io/validation.webhook.serving.knative.dev created

serviceaccount/cluster-local-gateway-service-account created
role.rbac.authorization.k8s.io/cluster-local-gateway-sds created
rolebinding.rbac.authorization.k8s.io/cluster-local-gateway-sds created
service/cluster-local-gateway created
deployment.apps/cluster-local-gateway created
gateway.networking.istio.io/cluster-local-gateway created
authorizationpolicy.security.istio.io/cluster-local-gateway created

```
kubectl kustomize common/knative/knative-eventing/base | kubectl apply -f -
```

namespace/knative-eventing created
customresourcedefinition.apiextensions.k8s.io/apiserversources.sources.knative.dev created
customresourcedefinition.apiextensions.k8s.io/brokers.eventing.knative.dev created
customresourcedefinition.apiextensions.k8s.io/channels.messaging.knative.dev created
customresourcedefinition.apiextensions.k8s.io/containersources.sources.knative.dev created
customresourcedefinition.apiextensions.k8s.io/eventtypes.eventing.knative.dev created
customresourcedefinition.apiextensions.k8s.io/inmemorychannels.messaging.knative.dev created
customresourcedefinition.apiextensions.k8s.io/parallels.flows.knative.dev created
customresourcedefinition.apiextensions.k8s.io/pingsources.sources.knative.dev created
customresourcedefinition.apiextensions.k8s.io/sequences.flows.knative.dev created
customresourcedefinition.apiextensions.k8s.io/sinkbindings.sources.knative.dev created
customresourcedefinition.apiextensions.k8s.io/subscriptions.messaging.knative.dev created
customresourcedefinition.apiextensions.k8s.io/triggers.eventing.knative.dev created
serviceaccount/eventing-controller created
serviceaccount/eventing-webhook created
serviceaccount/imc-controller created
serviceaccount/imc-dispatcher created
serviceaccount/mt-broker-filter created
serviceaccount/mt-broker-ingress created
serviceaccount/pingsource-mt-adapter created
role.rbac.authorization.k8s.io/knative-eventing-webhook created
clusterrole.rbac.authorization.k8s.io/addressable-resolver created
clusterrole.rbac.authorization.k8s.io/broker-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/builtin-podspecable-binding created
clusterrole.rbac.authorization.k8s.io/channel-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/channelable-manipulator created
clusterrole.rbac.authorization.k8s.io/eventing-broker-filter created
clusterrole.rbac.authorization.k8s.io/eventing-broker-ingress created
clusterrole.rbac.authorization.k8s.io/eventing-config-reader created
clusterrole.rbac.authorization.k8s.io/eventing-sources-source-observer created
clusterrole.rbac.authorization.k8s.io/flows-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/imc-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/imc-channelable-manipulator created
clusterrole.rbac.authorization.k8s.io/imc-controller created
clusterrole.rbac.authorization.k8s.io/imc-dispatcher created
clusterrole.rbac.authorization.k8s.io/knative-bindings-namespaced-admin created
clusterrole.rbac.authorization.k8s.io/knative-eventing-controller created
clusterrole.rbac.authorization.k8s.io/knative-eventing-mt-broker-filter created
clusterrole.rbac.authorization.k8s.io/knative-eventing-mt-broker-ingress created
clusterrole.rbac.authorization.k8s.io/knative-eventing-mt-channel-broker-controller created
clusterrole.rbac.authorization.k8s.io/knative-eventing-namespaced-admin created
clusterrole.rbac.authorization.k8s.io/knative-eventing-namespaced-edit created
clusterrole.rbac.authorization.k8s.io/knative-eventing-namespaced-view created
clusterrole.rbac.authorization.k8s.io/knative-eventing-pingsource-mt-adapter created
clusterrole.rbac.authorization.k8s.io/knative-eventing-sources-controller created
clusterrole.rbac.authorization.k8s.io/knative-eventing-webhook created
clusterrole.rbac.authorization.k8s.io/knative-flows-namespaced-admin created
clusterrole.rbac.authorization.k8s.io/knative-messaging-namespaced-admin created
clusterrole.rbac.authorization.k8s.io/knative-sources-namespaced-admin created
clusterrole.rbac.authorization.k8s.io/messaging-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/meta-channelable-manipulator created
clusterrole.rbac.authorization.k8s.io/podspecable-binding created
clusterrole.rbac.authorization.k8s.io/service-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/serving-addressable-resolver created
clusterrole.rbac.authorization.k8s.io/source-observer created
rolebinding.rbac.authorization.k8s.io/eventing-webhook created
clusterrolebinding.rbac.authorization.k8s.io/eventing-controller created
clusterrolebinding.rbac.authorization.k8s.io/eventing-controller-manipulator created
clusterrolebinding.rbac.authorization.k8s.io/eventing-controller-resolver created
clusterrolebinding.rbac.authorization.k8s.io/eventing-controller-source-observer created
clusterrolebinding.rbac.authorization.k8s.io/eventing-controller-sources-controller created
clusterrolebinding.rbac.authorization.k8s.io/eventing-mt-channel-broker-controller created
clusterrolebinding.rbac.authorization.k8s.io/eventing-webhook created
clusterrolebinding.rbac.authorization.k8s.io/eventing-webhook-podspecable-binding created
clusterrolebinding.rbac.authorization.k8s.io/eventing-webhook-resolver created
clusterrolebinding.rbac.authorization.k8s.io/imc-controller created
clusterrolebinding.rbac.authorization.k8s.io/imc-dispatcher created
clusterrolebinding.rbac.authorization.k8s.io/knative-eventing-mt-broker-filter created
clusterrolebinding.rbac.authorization.k8s.io/knative-eventing-mt-broker-ingress created
clusterrolebinding.rbac.authorization.k8s.io/knative-eventing-pingsource-mt-adapter created
configmap/config-br-default-channel created
configmap/config-br-defaults created
configmap/config-imc-event-dispatcher created
configmap/config-leader-election created
configmap/config-logging created
configmap/config-observability created
configmap/config-ping-defaults created
configmap/config-tracing created
configmap/default-ch-webhook created
secret/eventing-webhook-certs created
service/broker-filter created
service/broker-ingress created
service/eventing-webhook created
service/imc-dispatcher created
deployment.apps/eventing-controller created
deployment.apps/eventing-webhook created
deployment.apps/imc-controller created
deployment.apps/imc-dispatcher created
deployment.apps/mt-broker-controller created
deployment.apps/mt-broker-filter created
deployment.apps/mt-broker-ingress created
deployment.apps/pingsource-mt-adapter created
Warning: policy/v1beta1 PodDisruptionBudget is deprecated in v1.21+, unavailable in v1.25+; use policy/v1 PodDisruptionBudget
poddisruptionbudget.policy/eventing-webhook created
horizontalpodautoscaler.autoscaling/broker-filter-hpa created
horizontalpodautoscaler.autoscaling/broker-ingress-hpa created
horizontalpodautoscaler.autoscaling/eventing-webhook created
mutatingwebhookconfiguration.admissionregistration.k8s.io/sinkbindings.webhook.sources.knative.dev created
mutatingwebhookconfiguration.admissionregistration.k8s.io/webhook.eventing.knative.dev created
validatingwebhookconfiguration.admissionregistration.k8s.io/config.webhook.eventing.knative.dev created
validatingwebhookconfiguration.admissionregistration.k8s.io/validation.webhook.eventing.knative.dev created

### Kubeflow Namespace
```
kubectl kustomize common/kubeflow-namespace/base | kubectl apply -f -
```
namespace/kubeflow created

### Kubeflow Roles
```
kubectl kustomize common/kubeflow-roles/base | kubectl apply -f -
```
clusterrole.rbac.authorization.k8s.io/kubeflow-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-kubernetes-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-kubernetes-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-kubernetes-view created
clusterrole.rbac.authorization.k8s.io/kubeflow-view created

### Kubeflow Istio Resources
```
kubectl kustomize common/istio-1-9/kubeflow-istio-resources/base | kubectl apply -f -
```
clusterrole.rbac.authorization.k8s.io/kubeflow-istio-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-istio-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-istio-view created
gateway.networking.istio.io/kubeflow-gateway created

### Kubeflow Pipelines
```
kubectl kustomize apps/pipeline/upstream/env/platform-agnostic-multi-user | kubectl apply -f -
```
CDR服务启动没有那么快，因此强烈建议使用以下命令
```
while ! kubectl kustomize apps/pipeline/upstream/env/platform-agnostic-multi-user | kubectl apply -f -; do echo "Retrying to apply resources"; sleep 10; done
```
I0114 09:54:31.344903 2676341 log.go:184] well-defined vars that were never replaced: kfp-app-name,kfp-app-version
customresourcedefinition.apiextensions.k8s.io/clusterworkflowtemplates.argoproj.io created
customresourcedefinition.apiextensions.k8s.io/cronworkflows.argoproj.io created
customresourcedefinition.apiextensions.k8s.io/workfloweventbindings.argoproj.io created
customresourcedefinition.apiextensions.k8s.io/workflows.argoproj.io created
customresourcedefinition.apiextensions.k8s.io/workflowtemplates.argoproj.io created
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/compositecontrollers.metacontroller.k8s.io created
customresourcedefinition.apiextensions.k8s.io/controllerrevisions.metacontroller.k8s.io created
customresourcedefinition.apiextensions.k8s.io/decoratorcontrollers.metacontroller.k8s.io created
customresourcedefinition.apiextensions.k8s.io/scheduledworkflows.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/viewers.kubeflow.org created
serviceaccount/argo created
serviceaccount/kubeflow-pipelines-cache created
serviceaccount/kubeflow-pipelines-cache-deployer-sa created
serviceaccount/kubeflow-pipelines-container-builder created
serviceaccount/kubeflow-pipelines-metadata-writer created
serviceaccount/kubeflow-pipelines-viewer created
serviceaccount/meta-controller-service created
serviceaccount/metadata-grpc-server created
serviceaccount/ml-pipeline created
serviceaccount/ml-pipeline-persistenceagent created
serviceaccount/ml-pipeline-scheduledworkflow created
serviceaccount/ml-pipeline-ui created
serviceaccount/ml-pipeline-viewer-crd-service-account created
serviceaccount/ml-pipeline-visualizationserver created
serviceaccount/mysql created
serviceaccount/pipeline-runner created
role.rbac.authorization.k8s.io/argo-role created
role.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-role created
role.rbac.authorization.k8s.io/kubeflow-pipelines-cache-role created
role.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-role created
role.rbac.authorization.k8s.io/ml-pipeline created
role.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-role created
role.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-role created
role.rbac.authorization.k8s.io/ml-pipeline-ui created
role.rbac.authorization.k8s.io/ml-pipeline-viewer-controller-role created
role.rbac.authorization.k8s.io/pipeline-runner created
clusterrole.rbac.authorization.k8s.io/aggregate-to-kubeflow-pipelines-edit created
clusterrole.rbac.authorization.k8s.io/aggregate-to-kubeflow-pipelines-view created
clusterrole.rbac.authorization.k8s.io/argo-aggregate-to-admin created
clusterrole.rbac.authorization.k8s.io/argo-aggregate-to-edit created
clusterrole.rbac.authorization.k8s.io/argo-aggregate-to-view created
clusterrole.rbac.authorization.k8s.io/argo-cluster-role created
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-clusterrole created
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-cache-role created
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-role created
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-view created
clusterrole.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-role created
clusterrole.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-role created
clusterrole.rbac.authorization.k8s.io/ml-pipeline-ui created
clusterrole.rbac.authorization.k8s.io/ml-pipeline-viewer-controller-role created
Warning: rbac.authorization.k8s.io/v1beta1 ClusterRole is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 ClusterRole
clusterrole.rbac.authorization.k8s.io/ml-pipeline created
rolebinding.rbac.authorization.k8s.io/argo-binding created
rolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-binding created
rolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-rolebinding created
rolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-binding created
rolebinding.rbac.authorization.k8s.io/ml-pipeline created
rolebinding.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-binding created
rolebinding.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-binding created
rolebinding.rbac.authorization.k8s.io/ml-pipeline-ui created
rolebinding.rbac.authorization.k8s.io/ml-pipeline-viewer-crd-binding created
rolebinding.rbac.authorization.k8s.io/pipeline-runner-binding created
clusterrolebinding.rbac.authorization.k8s.io/argo-binding created
clusterrolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-binding created
clusterrolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-clusterrolebinding created
clusterrolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-binding created
clusterrolebinding.rbac.authorization.k8s.io/meta-controller-cluster-role-binding created
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-binding created
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-binding created
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-ui created
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-viewer-crd-binding created
Warning: rbac.authorization.k8s.io/v1beta1 ClusterRoleBinding is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 ClusterRoleBinding
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline created
configmap/kfp-launcher created
configmap/kubeflow-pipelines-profile-controller-code-4dctf4mhgf created
configmap/kubeflow-pipelines-profile-controller-env-5252m69c4c created
configmap/metadata-grpc-configmap created
configmap/ml-pipeline-ui-configmap created
configmap/pipeline-api-server-config-dc9hkg52h6 created
configmap/pipeline-install-config created
configmap/workflow-controller-configmap created
secret/mlpipeline-minio-artifact created
secret/mysql-secret created
service/cache-server created
service/kubeflow-pipelines-profile-controller created
service/metadata-envoy-service created
service/metadata-grpc-service created
service/minio-service created
service/ml-pipeline created
service/ml-pipeline-ui created
service/ml-pipeline-visualizationserver created
service/mysql created
service/workflow-controller-metrics created
persistentvolumeclaim/minio-pvc created
persistentvolumeclaim/mysql-pv-claim created
deployment.apps/cache-deployer-deployment created
deployment.apps/cache-server created
deployment.apps/kubeflow-pipelines-profile-controller created
deployment.apps/metadata-envoy-deployment created
deployment.apps/metadata-grpc-deployment created
deployment.apps/metadata-writer created
deployment.apps/minio created
deployment.apps/ml-pipeline created
deployment.apps/ml-pipeline-persistenceagent created
deployment.apps/ml-pipeline-scheduledworkflow created
deployment.apps/ml-pipeline-ui created
deployment.apps/ml-pipeline-viewer-crd created
deployment.apps/ml-pipeline-visualizationserver created
deployment.apps/mysql created
deployment.apps/workflow-controller created
statefulset.apps/metacontroller created
destinationrule.networking.istio.io/metadata-grpc-service created
destinationrule.networking.istio.io/ml-pipeline created
destinationrule.networking.istio.io/ml-pipeline-minio created
destinationrule.networking.istio.io/ml-pipeline-mysql created
destinationrule.networking.istio.io/ml-pipeline-ui created
destinationrule.networking.istio.io/ml-pipeline-visualizationserver created
virtualservice.networking.istio.io/metadata-grpc created
virtualservice.networking.istio.io/ml-pipeline-ui created
authorizationpolicy.security.istio.io/metadata-grpc-service created
authorizationpolicy.security.istio.io/minio-service created
authorizationpolicy.security.istio.io/ml-pipeline created
authorizationpolicy.security.istio.io/ml-pipeline-ui created
authorizationpolicy.security.istio.io/ml-pipeline-visualizationserver created
authorizationpolicy.security.istio.io/mysql created
authorizationpolicy.security.istio.io/service-cache-server created
error: unable to recognize "STDIN": no matches for kind "CompositeController" in version "metacontroller.k8s.io/v1alpha1"
Retrying to apply resources
I0114 09:54:46.477663 2680937 log.go:184] well-defined vars that were never replaced: kfp-app-name,kfp-app-version
customresourcedefinition.apiextensions.k8s.io/clusterworkflowtemplates.argoproj.io unchanged
customresourcedefinition.apiextensions.k8s.io/cronworkflows.argoproj.io unchanged
customresourcedefinition.apiextensions.k8s.io/workfloweventbindings.argoproj.io unchanged
customresourcedefinition.apiextensions.k8s.io/workflows.argoproj.io unchanged
customresourcedefinition.apiextensions.k8s.io/workflowtemplates.argoproj.io unchanged
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/compositecontrollers.metacontroller.k8s.io unchanged
customresourcedefinition.apiextensions.k8s.io/controllerrevisions.metacontroller.k8s.io unchanged
customresourcedefinition.apiextensions.k8s.io/decoratorcontrollers.metacontroller.k8s.io unchanged
customresourcedefinition.apiextensions.k8s.io/scheduledworkflows.kubeflow.org unchanged
customresourcedefinition.apiextensions.k8s.io/viewers.kubeflow.org unchanged
serviceaccount/argo unchanged
serviceaccount/kubeflow-pipelines-cache unchanged
serviceaccount/kubeflow-pipelines-cache-deployer-sa unchanged
serviceaccount/kubeflow-pipelines-container-builder unchanged
serviceaccount/kubeflow-pipelines-metadata-writer unchanged
serviceaccount/kubeflow-pipelines-viewer unchanged
serviceaccount/meta-controller-service unchanged
serviceaccount/metadata-grpc-server unchanged
serviceaccount/ml-pipeline unchanged
serviceaccount/ml-pipeline-persistenceagent unchanged
serviceaccount/ml-pipeline-scheduledworkflow unchanged
serviceaccount/ml-pipeline-ui unchanged
serviceaccount/ml-pipeline-viewer-crd-service-account unchanged
serviceaccount/ml-pipeline-visualizationserver unchanged
serviceaccount/mysql unchanged
serviceaccount/pipeline-runner unchanged
role.rbac.authorization.k8s.io/argo-role unchanged
role.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-role unchanged
role.rbac.authorization.k8s.io/kubeflow-pipelines-cache-role unchanged
role.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-role unchanged
role.rbac.authorization.k8s.io/ml-pipeline unchanged
role.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-role unchanged
role.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-role unchanged
role.rbac.authorization.k8s.io/ml-pipeline-ui unchanged
role.rbac.authorization.k8s.io/ml-pipeline-viewer-controller-role unchanged
role.rbac.authorization.k8s.io/pipeline-runner unchanged
clusterrole.rbac.authorization.k8s.io/aggregate-to-kubeflow-pipelines-edit unchanged
clusterrole.rbac.authorization.k8s.io/aggregate-to-kubeflow-pipelines-view unchanged
clusterrole.rbac.authorization.k8s.io/argo-aggregate-to-admin unchanged
clusterrole.rbac.authorization.k8s.io/argo-aggregate-to-edit unchanged
clusterrole.rbac.authorization.k8s.io/argo-aggregate-to-view unchanged
clusterrole.rbac.authorization.k8s.io/argo-cluster-role unchanged
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-clusterrole unchanged
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-cache-role unchanged
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-edit configured
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-role unchanged
clusterrole.rbac.authorization.k8s.io/kubeflow-pipelines-view configured
clusterrole.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-role unchanged
clusterrole.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-role unchanged
clusterrole.rbac.authorization.k8s.io/ml-pipeline-ui unchanged
clusterrole.rbac.authorization.k8s.io/ml-pipeline-viewer-controller-role unchanged
Warning: rbac.authorization.k8s.io/v1beta1 ClusterRole is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 ClusterRole
clusterrole.rbac.authorization.k8s.io/ml-pipeline unchanged
rolebinding.rbac.authorization.k8s.io/argo-binding unchanged
rolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-binding unchanged
rolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-rolebinding unchanged
rolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-binding unchanged
rolebinding.rbac.authorization.k8s.io/ml-pipeline unchanged
rolebinding.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-binding unchanged
rolebinding.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-binding unchanged
rolebinding.rbac.authorization.k8s.io/ml-pipeline-ui unchanged
rolebinding.rbac.authorization.k8s.io/ml-pipeline-viewer-crd-binding unchanged
rolebinding.rbac.authorization.k8s.io/pipeline-runner-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/argo-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-cache-deployer-clusterrolebinding unchanged
clusterrolebinding.rbac.authorization.k8s.io/kubeflow-pipelines-metadata-writer-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/meta-controller-cluster-role-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-persistenceagent-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-scheduledworkflow-binding unchanged
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-ui unchanged
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline-viewer-crd-binding unchanged
Warning: rbac.authorization.k8s.io/v1beta1 ClusterRoleBinding is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 ClusterRoleBinding
clusterrolebinding.rbac.authorization.k8s.io/ml-pipeline unchanged
configmap/kfp-launcher unchanged
configmap/kubeflow-pipelines-profile-controller-code-4dctf4mhgf unchanged
configmap/kubeflow-pipelines-profile-controller-env-5252m69c4c unchanged
configmap/metadata-grpc-configmap unchanged
configmap/ml-pipeline-ui-configmap unchanged
configmap/pipeline-api-server-config-dc9hkg52h6 unchanged
configmap/pipeline-install-config unchanged
configmap/workflow-controller-configmap unchanged
secret/mlpipeline-minio-artifact configured
secret/mysql-secret configured
service/cache-server unchanged
service/kubeflow-pipelines-profile-controller unchanged
service/metadata-envoy-service unchanged
service/metadata-grpc-service unchanged
service/minio-service unchanged
service/ml-pipeline unchanged
service/ml-pipeline-ui unchanged
service/ml-pipeline-visualizationserver unchanged
service/mysql unchanged
service/workflow-controller-metrics unchanged
persistentvolumeclaim/minio-pvc unchanged
persistentvolumeclaim/mysql-pv-claim unchanged
deployment.apps/cache-deployer-deployment unchanged
deployment.apps/cache-server configured
deployment.apps/kubeflow-pipelines-profile-controller unchanged
deployment.apps/metadata-envoy-deployment unchanged
deployment.apps/metadata-grpc-deployment unchanged
deployment.apps/metadata-writer configured
deployment.apps/minio unchanged
deployment.apps/ml-pipeline configured
deployment.apps/ml-pipeline-persistenceagent configured
deployment.apps/ml-pipeline-scheduledworkflow configured
deployment.apps/ml-pipeline-ui configured
deployment.apps/ml-pipeline-viewer-crd configured
deployment.apps/ml-pipeline-visualizationserver unchanged
deployment.apps/mysql unchanged
deployment.apps/workflow-controller unchanged
statefulset.apps/metacontroller configured
compositecontroller.metacontroller.k8s.io/kubeflow-pipelines-profile-controller created
destinationrule.networking.istio.io/metadata-grpc-service unchanged
destinationrule.networking.istio.io/ml-pipeline unchanged
destinationrule.networking.istio.io/ml-pipeline-minio unchanged
destinationrule.networking.istio.io/ml-pipeline-mysql unchanged
destinationrule.networking.istio.io/ml-pipeline-ui unchanged
destinationrule.networking.istio.io/ml-pipeline-visualizationserver unchanged
virtualservice.networking.istio.io/metadata-grpc unchanged
virtualservice.networking.istio.io/ml-pipeline-ui unchanged
authorizationpolicy.security.istio.io/metadata-grpc-service unchanged
authorizationpolicy.security.istio.io/minio-service unchanged
authorizationpolicy.security.istio.io/ml-pipeline unchanged
authorizationpolicy.security.istio.io/ml-pipeline-ui unchanged
authorizationpolicy.security.istio.io/ml-pipeline-visualizationserver unchanged
authorizationpolicy.security.istio.io/mysql unchanged
authorizationpolicy.security.istio.io/service-cache-server unchanged

### KFServing
```
kubectl kustomize apps/kfserving/upstream/overlays/kubeflow | kubectl apply -f -
```
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/inferenceservices.serving.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/trainedmodels.serving.kubeflow.org created
serviceaccount/kfserving-models-web-app created
role.rbac.authorization.k8s.io/leader-election-role created
clusterrole.rbac.authorization.k8s.io/kfserving-manager-role created
clusterrole.rbac.authorization.k8s.io/kfserving-models-web-app-cluster-role created
clusterrole.rbac.authorization.k8s.io/kfserving-proxy-role created
clusterrole.rbac.authorization.k8s.io/kubeflow-kfserving-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-kfserving-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-kfserving-view created
rolebinding.rbac.authorization.k8s.io/leader-election-rolebinding created
clusterrolebinding.rbac.authorization.k8s.io/kfserving-manager-rolebinding created
clusterrolebinding.rbac.authorization.k8s.io/kfserving-models-web-app-binding created
clusterrolebinding.rbac.authorization.k8s.io/kfserving-proxy-rolebinding created
configmap/inferenceservice-config created
configmap/kfserving-config created
configmap/kfserving-models-web-app-config-99hfgfg5f4 created
secret/kfserving-webhook-server-secret created
service/kfserving-controller-manager-metrics-service created
service/kfserving-controller-manager-service created
service/kfserving-models-web-app created
service/kfserving-webhook-server-service created
deployment.apps/kfserving-models-web-app created
statefulset.apps/kfserving-controller-manager created
certificate.cert-manager.io/serving-cert created
issuer.cert-manager.io/selfsigned-issuer created
virtualservice.networking.istio.io/kfserving-models-web-app created
authorizationpolicy.security.istio.io/kfserving-models-web-app created
Warning: admissionregistration.k8s.io/v1beta1 MutatingWebhookConfiguration is deprecated in v1.16+, unavailable in v1.22+; use admissionregistration.k8s.io/v1 MutatingWebhookConfiguration
mutatingwebhookconfiguration.admissionregistration.k8s.io/inferenceservice.serving.kubeflow.org created
Warning: admissionregistration.k8s.io/v1beta1 ValidatingWebhookConfiguration is deprecated in v1.16+, unavailable in v1.22+; use admissionregistration.k8s.io/v1 ValidatingWebhookConfiguration
validatingwebhookconfiguration.admissionregistration.k8s.io/inferenceservice.serving.kubeflow.org created
validatingwebhookconfiguration.admissionregistration.k8s.io/trainedmodel.serving.kubeflow.org created

### Katib
```
kubectl kustomize apps/katib/upstream/installs/katib-with-kubeflow | kubectl apply -f -
```
customresourcedefinition.apiextensions.k8s.io/experiments.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/suggestions.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/trials.kubeflow.org created
serviceaccount/katib-controller created
serviceaccount/katib-ui created
clusterrole.rbac.authorization.k8s.io/katib-controller created
clusterrole.rbac.authorization.k8s.io/katib-ui created
clusterrole.rbac.authorization.k8s.io/kubeflow-katib-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-katib-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-katib-view created
clusterrolebinding.rbac.authorization.k8s.io/katib-controller created
clusterrolebinding.rbac.authorization.k8s.io/katib-ui created
configmap/katib-config created
configmap/trial-templates created
secret/katib-mysql-secrets created
service/katib-controller created
service/katib-db-manager created
service/katib-mysql created
service/katib-ui created
persistentvolumeclaim/katib-mysql created
deployment.apps/katib-controller created
deployment.apps/katib-db-manager created
deployment.apps/katib-mysql created
deployment.apps/katib-ui created
certificate.cert-manager.io/katib-webhook-cert created
issuer.cert-manager.io/katib-selfsigned-issuer created
virtualservice.networking.istio.io/katib-ui created
mutatingwebhookconfiguration.admissionregistration.k8s.io/katib.kubeflow.org created
validatingwebhookconfiguration.admissionregistration.k8s.io/katib.kubeflow.org created

### Central Dashboard
```
kubectl kustomize apps/centraldashboard/upstream/overlays/istio | kubectl apply -f -
```
serviceaccount/centraldashboard created
role.rbac.authorization.k8s.io/centraldashboard created
clusterrole.rbac.authorization.k8s.io/centraldashboard created
rolebinding.rbac.authorization.k8s.io/centraldashboard created
clusterrolebinding.rbac.authorization.k8s.io/centraldashboard created
configmap/centraldashboard-config created
configmap/centraldashboard-parameters created
service/centraldashboard created
deployment.apps/centraldashboard created
virtualservice.networking.istio.io/centraldashboard created

### Admission Webhook
```
kubectl kustomize apps/admission-webhook/upstream/overlays/cert-manager | kubectl apply -f -
```
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/poddefaults.kubeflow.org created
serviceaccount/admission-webhook-service-account created
clusterrole.rbac.authorization.k8s.io/admission-webhook-cluster-role created
clusterrole.rbac.authorization.k8s.io/admission-webhook-kubeflow-poddefaults-admin created
clusterrole.rbac.authorization.k8s.io/admission-webhook-kubeflow-poddefaults-edit created
clusterrole.rbac.authorization.k8s.io/admission-webhook-kubeflow-poddefaults-view created
clusterrolebinding.rbac.authorization.k8s.io/admission-webhook-cluster-role-binding created
service/admission-webhook-service created
deployment.apps/admission-webhook-deployment created
certificate.cert-manager.io/admission-webhook-cert created
issuer.cert-manager.io/admission-webhook-selfsigned-issuer created
Warning: admissionregistration.k8s.io/v1beta1 MutatingWebhookConfiguration is deprecated in v1.16+, unavailable in v1.22+; use admissionregistration.k8s.io/v1 MutatingWebhookConfiguration
mutatingwebhookconfiguration.admissionregistration.k8s.io/admission-webhook-mutating-webhook-configuration created

### Notebooks
```
kubectl kustomize apps/jupyter/notebook-controller/upstream/overlays/kubeflow | kubectl apply -f -
```
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/notebooks.kubeflow.org created
serviceaccount/notebook-controller-service-account created
role.rbac.authorization.k8s.io/notebook-controller-leader-election-role created
clusterrole.rbac.authorization.k8s.io/notebook-controller-kubeflow-notebooks-admin created
clusterrole.rbac.authorization.k8s.io/notebook-controller-kubeflow-notebooks-edit created
clusterrole.rbac.authorization.k8s.io/notebook-controller-kubeflow-notebooks-view created
clusterrole.rbac.authorization.k8s.io/notebook-controller-role created
rolebinding.rbac.authorization.k8s.io/notebook-controller-leader-election-rolebinding created
clusterrolebinding.rbac.authorization.k8s.io/notebook-controller-role-binding created
configmap/notebook-controller-config-m44cmb547t created
service/notebook-controller-service created
deployment.apps/notebook-controller-deployment created

```
kubectl kustomize apps/jupyter/jupyter-web-app/upstream/overlays/istio | kubectl apply -f -
```
serviceaccount/jupyter-web-app-service-account created
Warning: rbac.authorization.k8s.io/v1beta1 Role is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 Role
role.rbac.authorization.k8s.io/jupyter-web-app-jupyter-notebook-role created
clusterrole.rbac.authorization.k8s.io/jupyter-web-app-cluster-role created
clusterrole.rbac.authorization.k8s.io/jupyter-web-app-kubeflow-notebook-ui-admin created
clusterrole.rbac.authorization.k8s.io/jupyter-web-app-kubeflow-notebook-ui-edit created
clusterrole.rbac.authorization.k8s.io/jupyter-web-app-kubeflow-notebook-ui-view created
Warning: rbac.authorization.k8s.io/v1beta1 RoleBinding is deprecated in v1.17+, unavailable in v1.22+; use rbac.authorization.k8s.io/v1 RoleBinding
rolebinding.rbac.authorization.k8s.io/jupyter-web-app-jupyter-notebook-role-binding created
clusterrolebinding.rbac.authorization.k8s.io/jupyter-web-app-cluster-role-binding created
configmap/jupyter-web-app-config-76844k4cd7 created
configmap/jupyter-web-app-logos created
configmap/jupyter-web-app-parameters-chmg88cm48 created
service/jupyter-web-app-service created
deployment.apps/jupyter-web-app-deployment created
virtualservice.networking.istio.io/jupyter-web-app-jupyter-web-app created

### Profiles + KFAM
```
kubectl kustomize apps/profiles/upstream/overlays/kubeflow | kubectl apply -f -
```
customresourcedefinition.apiextensions.k8s.io/profiles.kubeflow.org created
serviceaccount/profiles-controller-service-account created
role.rbac.authorization.k8s.io/profiles-leader-election-role created
rolebinding.rbac.authorization.k8s.io/profiles-leader-election-rolebinding created
clusterrolebinding.rbac.authorization.k8s.io/profiles-cluster-role-binding created
configmap/namespace-labels-data-48h7kd55mc created
configmap/profiles-config-46c7tgh6fd created
service/profiles-kfam created
deployment.apps/profiles-deployment created
virtualservice.networking.istio.io/profiles-kfam created

### Volumes Web App
```
kubectl kustomize apps/volumes-web-app/upstream/overlays/istio | kubectl apply -f -
```
serviceaccount/volumes-web-app-service-account created
clusterrole.rbac.authorization.k8s.io/volumes-web-app-cluster-role created
clusterrole.rbac.authorization.k8s.io/volumes-web-app-kubeflow-volume-ui-admin created
clusterrole.rbac.authorization.k8s.io/volumes-web-app-kubeflow-volume-ui-edit created
clusterrole.rbac.authorization.k8s.io/volumes-web-app-kubeflow-volume-ui-view created
clusterrolebinding.rbac.authorization.k8s.io/volumes-web-app-cluster-role-binding created
configmap/volumes-web-app-parameters-4gg8cm2gmk created
service/volumes-web-app-service created
deployment.apps/volumes-web-app-deployment created
virtualservice.networking.istio.io/volumes-web-app-volumes-web-app created

### Tensorboard
```
kubectl kustomize apps/tensorboard/tensorboards-web-app/upstream/overlays/istio | kubectl apply -f -
```
serviceaccount/tensorboards-web-app-service-account created
clusterrole.rbac.authorization.k8s.io/tensorboards-web-app-cluster-role created
clusterrole.rbac.authorization.k8s.io/tensorboards-web-app-kubeflow-tensorboard-ui-admin created
clusterrole.rbac.authorization.k8s.io/tensorboards-web-app-kubeflow-tensorboard-ui-edit created
clusterrole.rbac.authorization.k8s.io/tensorboards-web-app-kubeflow-tensorboard-ui-view created
clusterrolebinding.rbac.authorization.k8s.io/tensorboards-web-app-cluster-role-binding created
configmap/tensorboards-web-app-parameters-g28fbd6cch created
service/tensorboards-web-app-service created
deployment.apps/tensorboards-web-app-deployment created
virtualservice.networking.istio.io/tensorboards-web-app-tensorboards-web-app created

```
kubectl kustomize apps/tensorboard/tensorboard-controller/upstream/overlays/kubeflow | kubectl apply -f -
```
customresourcedefinition.apiextensions.k8s.io/tensorboards.tensorboard.kubeflow.org created
serviceaccount/tensorboard-controller created
role.rbac.authorization.k8s.io/tensorboard-controller-leader-election-role created
clusterrole.rbac.authorization.k8s.io/tensorboard-controller-manager-role created
clusterrole.rbac.authorization.k8s.io/tensorboard-controller-proxy-role created
rolebinding.rbac.authorization.k8s.io/tensorboard-controller-leader-election-rolebinding created
clusterrolebinding.rbac.authorization.k8s.io/tensorboard-controller-manager-rolebinding created
clusterrolebinding.rbac.authorization.k8s.io/tensorboard-controller-proxy-rolebinding created
configmap/tensorboard-controller-config-bf88mm96c8 created
service/tensorboard-controller-controller-manager-metrics-service created
deployment.apps/tensorboard-controller-controller-manager created

### Training Operator
```
kubectl kustomize apps/training-operator/upstream/overlays/kubeflow | kubectl apply -f -
```
customresourcedefinition.apiextensions.k8s.io/mxjobs.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/pytorchjobs.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/tfjobs.kubeflow.org created
customresourcedefinition.apiextensions.k8s.io/xgboostjobs.kubeflow.org created
serviceaccount/training-operator created
clusterrole.rbac.authorization.k8s.io/kubeflow-training-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-training-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-training-view created
clusterrole.rbac.authorization.k8s.io/training-operator created
clusterrolebinding.rbac.authorization.k8s.io/training-operator created
service/training-operator created
deployment.apps/training-operator created

### MPI Operator
```
kubectl kustomize apps/mpi-job/upstream/overlays/kubeflow | kubectl apply -f -
```
Warning: apiextensions.k8s.io/v1beta1 CustomResourceDefinition is deprecated in v1.16+, unavailable in v1.22+; use apiextensions.k8s.io/v1 CustomResourceDefinition
customresourcedefinition.apiextensions.k8s.io/mpijobs.kubeflow.org created
serviceaccount/mpi-operator created
clusterrole.rbac.authorization.k8s.io/kubeflow-mpijobs-admin created
clusterrole.rbac.authorization.k8s.io/kubeflow-mpijobs-edit created
clusterrole.rbac.authorization.k8s.io/kubeflow-mpijobs-view created
clusterrole.rbac.authorization.k8s.io/mpi-operator created
clusterrolebinding.rbac.authorization.k8s.io/mpi-operator created
configmap/mpi-operator-config created
deployment.apps/mpi-operator created

### 
```
kubectl kustomize common/user-namespace/base | kubectl apply -f -
```
configmap/default-install-config-9h2h2b6hbk created
profile.kubeflow.org/kubeflow-user-example-com created
