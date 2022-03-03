AWS EC2 Security Groups are a firewall mechanism that enables you to control access to your instances by specifying which incoming traffic is allowed. Security groups act as a virtual firewall, enabling you to control inbound and outbound traffic for your instances. Security group settings are specific to an instance, meaning that you can have different security group settings for different instances.

You can get a playbook on how to respond to security incidents in Cloud and Container environments [here](https://offers.cadosecurity.com/the-ultimate-guide-to-forensics-of-mining-malware-in-linux-container-and-cloud-environments).

![image](https://user-images.githubusercontent.com/99908467/154544696-3cde068f-917d-4420-be9a-24082be3bd95.png)


When you create an AWS EC2 Security Group, you specify the following:
* The name of the security group
* The type of traffic the security group allows inbound (ingress)
* The type of traffic the security group allows outbound (egress)
* The security group’s firewall rules

In terms of Best Practices:
* Only allow a limited list of ports and IP addresses
* Don’t allow access from 0.0.0.0/0 unless you really need it

For more, check out this slightly dated video from Linux Academy: https://www.youtube.com/watch?v=-9j7BvAyb2w
