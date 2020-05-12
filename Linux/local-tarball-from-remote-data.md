# Create a local compressed tarball from a remote directory
To create a local compressed file from a remote folder just do:
```bash
ssh user@host "tar -czf - /path/to/dir" > dir.tar.gz
```

Source: [click here](https://www.commandlinefu.com/commands/view/9900/create-a-local-compressed-tarball-from-remote-host-directory)
