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

**請直接修改 values.yaml 及 templates/api.yaml這兩個檔案**

1. 將 `api.yaml` 內的 image 改成用變數替換的方式，其內容需參照 `values.yaml` 內的 image 欄位
2. 修改 `values.yaml` 內的 image 改成剛剛建置出來並 push 到 container registry 的 image
3. 修改 `values.yaml` 內的 image pull secret 改為適當的值
4. 根據 `api.yaml` 內的 env 寫法，修改 `values.yaml` 將環境變數 `KEY1=VALUE1`,`KEY2=VALUE2` 加到環境變數中

修改完成後可進行以下操作

# 修改完後產生 YAML 檢測 Chart 是否有問題 (靜態檢查)
helm template [release-name] -n [namespace] example-helm-chart/

# 安裝 helm chart release 到指定 Namespace 底下
helm install [release-name] -n [namespace] example-helm-chart/