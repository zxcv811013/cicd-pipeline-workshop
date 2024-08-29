# cicd-pipeline-workshop

## Helm

### 基本 Helm 操作

```bash
# 建立 Chart 骨架
helm create demo-api

# 安裝 helm chart release 到指定 Namespace 底下
helm install [release-name] -n [namespace] demo-api/

# 列出指定 Namespace 底下安裝哪些 helm chart release
helm list -n [namespace]

# 升級 release
helm upgrade [release-name] -n [namespace] demo-api/

# 修改完後產生 YAML 檢測 Chart 是否有問題 (靜態檢查)
helm template [release-name] -n [namespace] demo-api/
```

## 實作 1

執行 helm template [release-name] -n [namespace] example-helm-chart/ 

有錯誤訊息出現，請根據錯誤訊息去找出是哪邊錯誤，並修改 api.yaml 修正