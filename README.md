# Gardenctl plugin

This plugin adds completion for the [Gardener command-line interface](https://github.com/gardener/gardenctl-v2),
as well as some aliases for common gardenctl commands. If no TERM_SESSION_ID environment variable is defined it generates a uuid and exports it as GCTL_SESSION_ID. 

To use it, add `gardenctl` to the plugins array in your zshrc file:

```zsh
plugins=(... gardenctl)
```

## Aliases

| Alias   | Command                                | Description                                |
|:--------|:---------------------------------------|:-------------------------------------------|
| g       | `gardenctl`                            | The gardenctl command                      |
| gtv     | `gardenctl target view -o yaml`        | Show the current target                    |
| gtc     | `gardenctl target control-plane`       | Target the control-plane of a shoot        |
| gtc-    | `gardenctl target unset control-plane` | Target the shoot of a control-plane        |
| gk      | `eval $(gardenctl kubectl-env zsh)`    | Configure kubetcl environment              |
| gp      | `eval $(gardenctl kubectl-env zsh)`    | Configure cloud provider CLI environment   |
| gcv     | `gardenctl config view -o yaml`        | Show gardenctl configuration               |
