### AnyDesk - How Enable Remote Access from ubuntu/debian terminal.

Note:
Here are the commands might be usefull in this purpose:

`anydesk --get-status` : To get current status of anydesk, which might be offlien,online or nothing.  
`anydesk --get-id` : To get the ID that your system can be accessed by.  
`anydesk --service` : To start anydesk service if not already running (for Linux).  
`anydesk --restart-service` : To restart anydesk service  
`anydesk --stop-service` : To stop anydesk service  
`sudo echo qazwsxedc | anydesk --set-password` : to set password on anydesk (required to access from a remote system).  

In case that your target machine is a kind of a Ubuntu or a Debian based one:  
`echo -e "ad.security.allow_logon_token=true\nad.features.unattended=true" >> ~/.anydesk/user.conf  `
`sudo echo [your-custom-password] | anydesk --set-password`  
`sudo sed -i '' -e 's/# AutomaticLogin/AutomaticLogin/g' -e 's/#WaylandEnable/WaylandEnable/g' /etc/gdm3/custom.conf`  
`sudo reboot` 

`anydesk --get-status` , if its not online then run anydesk --service.  
`anydesk --get-id && echo` to get your desk id.  


ref: https://gist.github.com/imami/4e8b187e7e1e6fc9510d907eb1a7a5b3
