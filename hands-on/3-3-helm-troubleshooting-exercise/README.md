# cicd-pipeline-workshop

## Helm

### 基本 Helm 操作


```bash
# 安裝 helm chart release 到指定 Namespace 底下
helm install [release-name] -n [namespace] example-helm-chart/

# 列出指定 Namespace 底下安裝哪些 helm chart release
helm list -n [namespace]

# 升級 release
helm upgrade [release-name] -n [namespace] example-helm-chart/

# 修改完後產生 YAML 檢測 Chart 是否有問題 (靜態檢查)
helm template [release-name] -n [namespace] example-helm-chart/
```


### 基本 kubernetes log 操作


```bash
# 查看 Pod log
kubectl logs -n [namespace] [pod-name]

```

## 實作 

依照先前講師示範的方式，先將 example-helm-chart/ 的 chart 使用 ArgoCD 部署到環境中

進行修改將服務部署到環境中，且 test-job 成功執行結束

deploy-python 執行時需要有 `REDIS_HOST` 及 `REDIS_PORT`，並且會使用這兩個變數連線到 redis