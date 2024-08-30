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

## 實作 1

**請直接修改 example-helm-chart 的內容，不要額外 copy**

## 實作 1

執行 helm template [release-name] -n [namespace] example-helm-chart/ 時正常

但執行 helm upgrade [release-name] -n [namespace] example-helm-chart/ 會失敗 

請根據錯誤訊息讓 helm chart 成功部署