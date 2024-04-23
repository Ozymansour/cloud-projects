User Interface column lists `vit1/vti2` -> these are the IP sec tunnels connected from the customer router to AWS
Note that `10.16.0.0` is the default CIDR range for AWS’s VPC

![Kernel IP routing table](https://github.com/Ozymansour/cloud-projects/blob/main/aws-global-vpn/Final%20result%20screenshots/IPsec%20tunnels.png)

&nbsp;

`B>*` illustrates that 10.16.0.0 is a BGP-learned route, which it learnt from vti1/vit2 (the two IPsec tunnels) of OnPremRouter1

![BGP routing](https://github.com/Ozymansour/cloud-projects/blob/main/aws-global-vpn/Final%20result%20screenshots/BGP%20routing.png)

&nbsp;

Finally, "Tunnel details" in the AWS management console shows the BGP implmenetation for 2 IPsec tunnels per VPN connection:

![AWS management console](https://github.com/Ozymansour/cloud-projects/blob/main/aws-global-vpn/Final%20result%20screenshots/Console.png)
