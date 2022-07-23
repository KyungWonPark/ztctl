# ztctl
Simple CLI tool for managing zerotier network on self-hosted controller

# Requirements
Your node should have zerotier installed  
https://www.zerotier.com/download/

# Installation
```
$ git clone https://github.com/KyungWonPark/ztctl.git
```

# Usage
First get access token to interface with zerotier
```
$ cd ztctl/
$ . auth
```

List networks hosted on this node
```
$ ./ztctl net list
```

Create new network
```
$ ./ztctl net create
```

Check created network, get its ID
```
$ ./ztctl net list
```

Show details about network
```
$ ./ztctl net get <network-id>
```

Change network configuration using a json file  
Reference: https://docs.zerotier.com/service/v1/#tag/controller
```
$ ./ztctl net set <network-id> <json-file>
```

List members of a network
```
$ ./ztctl net <network-id> member list
```

Approve a member of a network
```
$ ./ztctl net <network-id> member approve <member-id>
```

Get details of a member
```
$ ./ztctl net <network-id> member get <member-id>
```

Change member properties using a json file  
Reference: https://docs.zerotier.com/service/v1/#tag/controller
```
$ ./ztctl net <network-id> member set <member-id> <json-file>
```

Remove a member from a network
```
$ ./ztctl net <network-id> member remove <member-id>
```
