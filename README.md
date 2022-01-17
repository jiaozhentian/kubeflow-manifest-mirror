# Kubeflow v1.14.1 中国镜像

由于国内网络问题，因此对于kubeflow源码安装的过程过于不友好。这里将kubeflow源码拉了下来，然后对代码中所有的gcr.io镜像进行了替换。
官方源代码地址：https://github.com/kubeflow/manifests.git
这里我没有使用release版本，直接pull的源代码，时间为2022/1/14日。
做国内镜像很辛苦，如果本段代码对你有用，大家都知道该怎么办吧。

## 安装

### 环境
1. kubernetes 1.21.8。这里注意下，我在编译的时候，发现kubeflow大量使用了k8s测试版的API，目前要求k8s版本需要介于[1.17, 1.22)。
2. kustomize(3.x)，我用的k8s自带的kustomize，不要用4.x的kustomize，官方说有bug。
3. nvidia驱动，k8s nvidia插件yaml。
4. 存储sc，不管是local还是nfs，都需要提前创建好并指定为默认存储sc。

### kustomize安装
按照官方的一键安装或分步安装即可。由于我对每个模块均进行了调试，因此我是用的单步安装。需要提出的是，代码有可能有bug，如在执行过程中，出现
```
error: unable to recognize "STDIN": no matches for kind "Image" in version "caching.internal.knative.dev/v1alpha1"
```
这是knative安装过程中出现的bug，根据网上提供的解决方案，执行
```
kubectl apply -f ./patch/knative_serving_releases_download_v0.17.1_serving-crds.yaml
```

如出现
```
error: unable to recognize "STDIN": no matches for kind "CompositeController" in version "metacontroller.k8s.io/v1alpha1"
```
这个问题是在启动pipeline组件时文件顺序执行太快了，没有等待CRD服务创建好就开始进行引用，把pipeline创建组件的明令再执行一遍。

一键安装命令
```
while ! kubectl kustomize example | kubectl apply -f -; do echo "Retrying to apply resources"; sleep 10; done
```
分步安装命令参考官方

## NOTE
如一键安装不好使，可以尝试单独组件安装，由于我目前暂时已经部署好，遂暂无尝试一键安装的方式。