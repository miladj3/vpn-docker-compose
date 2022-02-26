# vpn-docker-compose

remove env.sample to .env after upload to server

CONFIG SSTP: 

> docker exec -it  sstp

 > ./vpnserver start

You will get the following output:
The SoftEther VPN Server service has been started.
Let's get started by accessing to the following URL from your PC:
https://69.28.88.203:5555/
  or
https://69.28.88.203/
Note: IP address may vary. Specify your server's IP address.

 > ./vpncmd

By using vpncmd program, the following can be achieved.

1. Management of VPN Server or VPN Bridge
2. Management of VPN Client
3. Use of VPN Tools (certificate creation and Network Traffic Speed Test Tool)

Select 1, 2 or 3: 1

Specify the host name or IP address of the computer that the destination VPN Server or VPN Bridge is operating on.
By specifying according to the format 'host name:port number', you can also specify the port number.
(When the port number is unspecified, 443 is used.)
If nothing is input and the Enter key is pressed, the connection will be made to the port number 8888 of localhost (this computer).
Hostname of IP Address of Destination:

If connecting to the server by Virtual Hub Admin Mode, please input the Virtual Hub name.
If connecting by server admin mode, please press Enter without inputting anything.
Specify Virtual Hub Name:
Connection has been established with VPN Server "localhost" (port 443).

You have administrator privileges for the entire VPN Server.

 > ServerPasswordSet

ServerPasswordSet command - Set VPN Server Administrator Password
Please enter the password. To cancel press the Ctrl+D key.

Password: **********
Confirm input: **********


The command completed successfully.

> HubCreate myhub

HubCreate command - Create New Virtual Hub
Please enter the password. To cancel press the Ctrl+D key.

Password: **********
Confirm input: **********


The command completed successfully.

> Hub myhub

Hub command - Select Virtual Hub to Manage
The Virtual Hub "myhub" has been selected.
The command completed successfully.

VPN Server/myhub>

> SecureNatEnable

SecureNatEnable command - Enable the Virtual NAT and DHCP Server Function (SecureNat Function)
The command completed successfully.

> UserCreate vpnuser

UserCreate command - Create User
Assigned Group Name:

User Full Name: VPN User

User Description: IT

The command completed successfully.

> UserPasswordSet vpnuser

UserPasswordSet command - Set Password Authentication for User Auth Type and Set Password
Please enter the password. To cancel press the Ctrl+D key.

Password: **********
Confirm input: **********


The command completed successfully.

> IPsecEnable

IPsecEnable command - Enable or Disable IPsec VPN Server Function
Enable L2TP over IPsec Server Function (yes / no): yes

Enable Raw L2TP Server Function (yes / no): yes

Enable EtherIP / L2TPv3 over IPsec Server Function (yes / no): yes

Pre Shared Key for IPsec (Recommended: 9 letters at maximum): vpnserver

Default Virtual HUB in a case of omitting the HUB on the Username: myhub

The command completed successfully.
> exit

https://cloudinfrastructureservices.co.uk/how-to-install-softether-vpn-server-on-ubuntu-20-04/