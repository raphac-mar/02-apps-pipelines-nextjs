# Criar o pipeline (esteira) e as triggers, para o framework nextjs

- Git: `https://github.com/raphac-mar/02-apps-pipelines-nextjs`

## Argo CD

```sh
cd 02-apps-pipelines-nextjs/pipeline-nextjs
oc apply -f argocd/application.yaml

oc delete Application 02-apps-pipelines-nextjs -n openshift-gitops
```

- https://tekton.dev/docs/pipelines/auth/#configuring-ssh-auth-authentication-for-git
- https://deploy-preview-387--tekton.netlify.app/docs/how-to-guides/clone-repository/#git-authentication
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?platform=windows&tool=webui

```
ssh-keyscan -H github.com >> ~/.ssh/known_hosts
cat .ssh/known_hosts | base64 -w0


```