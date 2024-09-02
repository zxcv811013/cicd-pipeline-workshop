# ArgoCD

**ArgoCD 的登入帳密請參考課程平台**

helm uninstall [release-name] -n [namespace] 

## 實作 1
1. 確認 3-6-helm-example 有 fork 到各自的 repo 上
2. 根據講師給的帳號密碼登入 ArgoCD 頁面
3. 建立 application 將
4. source 使用各自的 github， path 選擇 3-6-helm-example/example-helm-chart
5. destination 選擇各自的 namespace

## 實作 2
1. 使用 sync 功能，將 helm 部署到 各自的 namespace 中
2. 查看目前的狀態

## 實作 3
1. 修改 values.yaml 裡面的 python replicas 的數量，並推到 github 上
2. 查看目前的狀態
3. 再次使用 sync 同步

## 實作 4
1. 將 k8s 中的 python deployment 刪除
2. 查看目前的狀態
3. 再次使用 sync 同步

## 實作 5
1. 查看 ArgoCD 的 pod log

## demo
使用 private git source 的方法