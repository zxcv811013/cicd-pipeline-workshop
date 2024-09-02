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

先執行 helm upgrade [release-name] -n [namespace] example-helm-chart/ 部署 helm chart

再執行 helm test [release-name] -n [namespace] 會發現測試沒過

試著查看 pod log 找出是哪邊設定有誤