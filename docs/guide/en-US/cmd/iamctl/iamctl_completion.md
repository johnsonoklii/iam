## iamctl completion

Output shell completion code for the specified shell (bash or zsh)

### Synopsis

Output shell completion code for the specified shell (bash or zsh). The shell code must be evaluated to provide interactive completion of iamctl commands.  This can be done by sourcing it from the .bash_profile.

 Detailed instructions on how to do this are available here: http://github.com/marmotedu/iam/docs/installation/iamctl.md#enabling-shell-autocompletion

 Note for zsh users: [1] zsh completions are only supported in versions of zsh >= 5.2

```
iamctl completion SHELL
```

### Examples

```
  # Installing bash completion on macOS using homebrew
  ## If running Bash 3.2 included with macOS
  brew install bash-completion
  ## or, if running Bash 4.1+
  brew install bash-completion@2
  ## If iamctl is installed via homebrew, this should start working immediately.
  ## If you've installed via other means, you may need add the completion to your completion directory
  iamctl completion bash > $(brew --prefix)/etc/bash_completion.d/iamctl
  
  
  # Installing bash completion on Linux
  ## If bash-completion is not installed on Linux, please install the 'bash-completion' package
  ## via your distribution's package manager.
  ## Load the iamctl completion code for bash into the current shell
  source <(iamctl completion bash)
  ## Write bash completion code to a file and source if from .bash_profile
  iamctl completion bash > ~/.iam/completion.bash.inc
  printf "
  # IAM shell completion
  source '$HOME/.iam/completion.bash.inc'
  " >> $HOME/.bash_profile
  source $HOME/.bash_profile
  
  # Load the iamctl completion code for zsh[1] into the current shell
  source <(iamctl completion zsh)
  # Set the iamctl completion code for zsh[1] to autoload on startup
  iamctl completion zsh > "${fpath[1]}/_iamctl"
```

### Options

```
  -h, --help   help for completion
```

### Options inherited from parent commands

```
      --alsologtostderr                       log to standard error as well as files
  -c, --config FILE                           Read configuration from specified FILE, support JSON, TOML, YAML, HCL, or Java properties formats.
      --iamconfig string                      Path to the iamconfig file to use for CLI requests
      --log-backtrace-at traceLocations       when logging hits line file:N, emit a stack trace
      --log-dir string                        If non-empty, write log files in this directory
      --log-link string                       If non-empty, add symbolic links in this directory to the log files
      --logbuflevel int                       Buffer log messages logged at this level or lower (-1 means don't buffer; 0 means buffer INFO only; ...). Has limited applicability on non-prod platforms.
      --logtostderr                           log to standard error instead of files
      --match-server-version                  Require server version to match client version
      --profile string                        Name of profile to capture. One of (none|cpu|heap|goroutine|threadcreate|block|mutex) (default "none")
      --profile-output string                 Name of the file to write the profile to (default "profile.pprof")
  -s, --server.address string                 The address and port of the IAM API server
      --server.certificate-authority string   Path to a cert file for the certificate authority
      --server.insecure-skip-tls-verify       If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --server.max-retries int                Maximum number of retries.
      --server.retry-interval duration        The interval time between each attempt. (default 1s)
      --server.timeout duration               The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default 30s)
      --server.tls-server-name string         Server name to use for server certificate validation. If it is not provided, the hostname used to contact the server is used
      --stderrthreshold severityFlag          logs at or above this threshold go to stderr (default 2)
      --user.client-certificate string        Path to a client certificate file for TLS
      --user.client-key string                Path to a client key file for TLS
      --user.password string                  Password for basic authentication to the API server
      --user.secret-id string                 SecretID for JWT authentication to the API server
      --user.secret-key string                SecretKey for jwt authentication to the API server
      --user.token string                     Bearer token for authentication to the API server
      --user.username string                  Username for basic authentication to the API server
  -v, --v Level                               log level for V logs
      --version version[=true]                Print version information and quit.
      --vmodule vModuleFlag                   comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [iamctl](iamctl.md)	 - iamctl controls the iam platform

###### Auto generated by spf13/cobra on 30-Mar-2025
