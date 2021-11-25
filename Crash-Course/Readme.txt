1. we also need to pass the data defined in the configMap and secrets to pods 
2. when starting mongodb, username and password should be set, but it'll automatically generate a set of username and password 
3. question: how to set the username and password for the db? check documentation for the container 


final step: create components one by one in k8s
1. need to create the external config first (ConfigMap and Secret must exist before deployments) 
2. 起 component 的 command line: kubectl apply -f [file name] (-f stands for file) 
3. 確認 components : kubectl get [all, configmap, ...] 
4. 確認 詳細內容 : kubectl describe [component] [name]
5. 確認 logs : kubectl logs [pod name] [-f] 