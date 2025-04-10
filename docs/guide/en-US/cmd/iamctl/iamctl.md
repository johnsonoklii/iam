## iamctl

iamctl controls the iam platform

### Synopsis

iamctl controls the iam platform, is the client side tool for iam platform.

 Find more information at: https://github.com/marmotedu/iam/blob/master/docs/guide/en-US/cmd/iamctl/iamctl.md

```
iamctl [flags]
```

### Options

```
      --alsologtostderr                       log to standard error as well as files
  -c, --config FILE                           Read configuration from specified FILE, support JSON, TOML, YAML, HCL, or Java properties formats.
  -h, --help                                  help for iamctl
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

* [iamctl color](iamctl_color.md)	 - Print colors supported by the current terminal
* [iamctl completion](iamctl_completion.md)	 - Output shell completion code for the specified shell (bash or zsh)
* [iamctl info](iamctl_info.md)	 - Print the host information
* [iamctl jwt](iamctl_jwt.md)	 - JWT command-line tool
* [iamctl new](iamctl_new.md)	 - Generate demo command code
* [iamctl options](iamctl_options.md)	 - Print the list of flags inherited by all commands
* [iamctl policy](iamctl_policy.md)	 - Manage authorization policies on iam platform
* [iamctl secret](iamctl_secret.md)	 - Manage secrets on iam platform
* [iamctl set](iamctl_set.md)	 - Set specific features on objects
* [iamctl user](iamctl_user.md)	 - Manage users on iam platform
* [iamctl validate](iamctl_validate.md)	 - Validate the basic environment for iamctl to run
* [iamctl version](iamctl_version.md)	 - Print the client and server version information

###### Auto generated by spf13/cobra on 30-Mar-2025
