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

執行 helm install/upgrade [release-name] -n [namespace] example-helm-chart/ 部數完成後
執行 helm test [release-name] -n [namespace] 進行測試
查看 python 的 log 訊息，試著修正錯誤的部分