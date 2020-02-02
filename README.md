# nameserver_tutorial

## Issues with building scaffold
During make, the line @go build -mod=readonly -o build/scaffold main.go returns the following message:

**Error during make**

>  #github.com/cosmos/scaffold/cmd
 
>../../../go/pkg/mod/github.com/cosmos/scaffold@v0.0.0-20200131080246-329ad38d2264/cmd/utils.go:34:20: undefined: AssetNames

>../../../go/pkg/mod/github.com/cosmos/scaffold@v0.0.0-20200131080246-329ad38d2264/cmd/utils.go:97:14: undefined: Asset

>Makefile:19: recipe for target 'install' failed
make: *** [install] Error 2

In main.go, if I change the import location from "github.com/cosmos/scaffold/cmd" to "github.com/sentenientway/nameserver_tutorial/scaffold/cmd", I receive the following error:

>go: finding github.com/sentientway/nameserver_tutorial/scaffold latest

>go: finding github.com/sentientway/nameserver_tutorial/scaffold/cmd latest

>github.com/sentientway/nameserver_tutorial imports
>github.com/sentientway/nameserver_tutorial/scaffold/cmd: no matching versions for query "latest"

>Makefile:7: recipe for target 'mod' failed
make: *** [mod] Error 1

