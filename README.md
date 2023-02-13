## Authorization

```bash
$ k edit configmap argocd-cm -n argocd
```
```
data:
     accounts.admin: apiKey
```
```bash
$ argocd account generate-token
```

## Create a project:
```bash
$ curl -k -X POST https://argocd.com.br/api/v1/projects -H "Content-Type: application/json" -H "Authorization: Bearer $ARGOCD_TOKEN" -d @project.json
```