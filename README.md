# Sisyphus OS Preflight Stuff
This repo doesn't have very much in it, because it's just a safe place for some OS files. 

* the sisyphus.service file should be copied to /etc/systemd/system/
* the preflight-sisyphus.service file should be copied to /etc/systemd/system

After putting the service files in place, test them out:

`sudo systemctl start sisyphus`
`sudo systemctl status sisyphus`

Watch for errors, stop and fix if errors show up. 
Repeat the same for the preflight-sisyphus.

Once the services run without issue, use the following command to enable them (start on startup)

`sudo systemctl enable preflight-sisyphus`
`sudo systemctl enable sisyphus`

This will make sure the node and python processes start on startup :)


