# get-toolkit-action

This GitHub action will lint and test project's image with Dockle and check the deployment diff with ArgoCD and also send notifications to slack depending on the configuration.

## Config

- `registry`:
  - description: `Registry's host`
  - required: `false`
  - default: `"ghcr.io"`
- `user`:
  - description: `Registry's user`
  - required: `false`
  - default: `${{ github.actor }}`
- `password`:
  - description: `Registry user's password or token`
  - required: `true`
- `image`:
  - description: `Docker image name with tag`
  - required: `true`
- `dockle`:
  - description: `Enable dockle linting steps (Default: true)`
  - required: `false`
  - default: `true`
- `argocd`:
  - description: `Enable argocd diff on PRs (Default: true)`
  - required: `false`
  - default: `true`
- `argocd-auth`:
  - description: `ArgoCD Auth token`
  - required: `false`
- `argocd-server`:
  - description: `"ArgoCD server URI"`
  - required: false
- `github-secret`:
  - description: `GitHub Secret for Actions`
  - required: `true`
- `slack-webhook`:
  - description: `Slack Webhook for notifications`
  - required: `true`
- `deploy-fail-notification`:
  - description: `Send notification to Slack for deploy failure`
  - required: `false`
  - default: `false`