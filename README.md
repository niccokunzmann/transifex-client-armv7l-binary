# Transifex Client for Android and Raspberry Pi

This is an informal build of the [Transifex Client](https://github.com/transifex/transifex-client/) for Raspberry Pi and Android Phones.
This is the architecture it works on:

```
$ uname -m
armv7l
```

You can download the tx file if you are desparate and cannot build it yourself.

```
cd ~/.local/bin
wget -O tx 'https://github.com/niccokunzmann/transifex-client-armv7l-binary/blob/master/tx?raw=true'
chmod +x tx
```

Ready to go:

```
$ tx --help
NAME:
   tx - A new cli application

USAGE:
   tx [global options] command [command options] [arguments...]

COMMANDS:
   migrate, mg  Migrate legacy configuration.
   push         tx push [options] [resource_id...]
   pull         tx pull [options] [resource_id...]
   add, a       Add a resource in config. Use no arguments for an interactive mode.
   init         tx init
   delete       tx delete [options] [resource_id...]
   update       Update the `tx` application if there is a newer version
   status       tx status [resource_id...]
   help, h      Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --root-config FILE          Root configuration from FILE
   --config FILE, -c FILE      Load configuration from FILE
   --token value, -t value     The api token to use [$TX_TOKEN]
   --hostname value, -H value  The API hostname [$TX_HOSTNAME]
   --cacert value              Path to CA certificate bundle file [$TX_CACERT]
   --help, -h                  show help (default: false)
```

Or not?
```
$ tx --help
-bash: tx: command not found
```

Then, you will need to add that path to your `.bashrc` to make it acessible:
```
echo 'export PATH="$PATH:~/.local/bin"' >> ~/.bashrc
source ~/.bashrc
tx --help
```


## Links

- **[Download TX file](https://github.com/niccokunzmann/transifex-client-armv7l-binary/blob/master/tx?raw=true)**
- [Transifex Command Line Client Repository](https://github.com/transifex/transifex-client/) for Raspberry Pi and Android Phones.
- [Blog Post in the Transifex Community Forum](https://community.transifex.com/t/using-transifex-client-on-the-raspberry-pi-android-phone/2687)

