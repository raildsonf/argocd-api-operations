## Authorization

$ k edit configmap argocd-cm -n argocd
```
data:
     accounts.admin: apiKey
```
$ argocd account generate-token


## Create a project:
$curl -k -X POST https://argocd.com.br/api/v1/projects -H "Content-Type: application/json" -H "Authorization: Bearer $ARGOCD_TOKEN" -d @project.json


