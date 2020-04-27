_Last Updated: 27 April 2020_

### **Setting up a Virtual Private Network (VPN) for Your Clinic or Partner Organization.**

We've included a phased approach for students to practice setting up the Algo VPN,  

The process can be broken into three main phases.

As students go through the steps, they should keep track of things that went well, things that were difficult/went poorly/pain points, and ideas /opportunities for improving the process. They can use the tables below each section. Also, they can flag any “make sure you do this” thoughts that they have and add them to the short list of instructions in each phase.

#### Installation and Dependencies

* Follow instructions: [https://github.com/trailofbits/algo#deploy-the-algo-server](https://github.com/trailofbits/algo#deploy-the-algo-server)
* Install VPN Builder on local machine.
* It’s possible another organization or tech expert needs to help you do this.

<table>
  <tr>
   <td>Name
   </td>
   <td>Good things (Roses)
   </td>
   <td>Bad things (Thorns)
   </td>
   <td>Opportunities (Buds)
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


#### Access and Deployment to AWS

* Follow instructions: [https://github.com/trailofbits/algo/blob/master/docs/cloud-amazon-ec2.md](https://github.com/trailofbits/algo/blob/master/docs/cloud-amazon-ec2.md)
* Setup Amazon Web Service account for hosting the VPN on EC2. 
* Create an “IAM” user such as “Algo VPN” with appropriate permissions.
* Run the VPN builder, select AWS EC2 and input the public/secret key for the “Algo VPN” account: 

```
    Enter your aws_access_key (http://docs.aws.amazon.com/general/latest/gr/managing-aws-access-keys.html)
    Note: Make sure to use an IAM user with an acceptable policy attached (see https://github.com/trailofbits/algo/blob/master/docs/deploy-from-ansible.md).
    [pasted values will not be displayed]
    [AKIA...]: 

    Enter your aws_secret_key (http://docs.aws.amazon.com/general/latest/gr/managing-aws-access-keys.html)
    [pasted values will not be displayed]
    [ABCD...]:
```

<table>
  <tr>
   <td>Name
   </td>
   <td>Good things (Roses)
   </td>
   <td>Bad things (Thorns)
   </td>
   <td>Opportunities (Buds)
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


#### VPN User Setup on Laptops and Mobile devices

* Follow instructions: [https://github.com/trailofbits/algo#configure-the-vpn-clients](https://github.com/trailofbits/algo#configure-the-vpn-clients)
* Users download Wireguard to their phones and laptops.
* Share the setup configurations with users.
* Users finish setting up the VPN by importing config file or scanning the QR code.
* If WireGuard doesn’t work, users can use another setup method, but will need more instructions.

<table>
  <tr>
   <td>Name
   </td>
   <td>Good things (Roses)
   </td>
   <td>Bad things (Thorns)
   </td>
   <td>Opportunities (Buds)
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


