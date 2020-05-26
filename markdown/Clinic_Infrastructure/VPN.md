# **Setting up a Virtual Private Network (VPN)**

## Introduction to Virtual Private Networks (VPNs)

Virtual Private Networks can be an important part to protecting your students' privacy and the security of your client's data. What is a Virtual Private Network or VPN? Read the Center for Democracy & Technology's [VPN Techplanation](https://cdt.org/insights/techsplanations-part-5-virtual-private-networks/).

Below we describe a phased approach for students to practice setting up a virtual private network. The process can be broken into three main phases that allow students and staff to explore the advantages and disadvantages of its installation and management.

As students go through the steps, they should keep track of things that went well, things that were difficult or pain points, and ideas/opportunities for improving the process. They can use the tables below each section. Also, they can flag any “make sure you do this” thoughts that they have and add them to the short list of instructions in each phase.

### Primary Option: Algo VPN

The first option to explore is Algo, an open source VPN project supported by Trail of Bits (https://www.trailofbits.com/).

#### Installation and Dependencies

* Follow these instructions: [https://github.com/trailofbits/algo#deploy-the-algo-server](https://github.com/trailofbits/algo#deploy-the-algo-server)
* Install the VPN Builder on your local machine.
* This is the most complicated step and it’s possible another organization or tech expert needs to help you do this.

<table>
  <tr>
   <td>Strengths 
   </td>
   <td>Weaknesses
   </td>
   <td>Opportunities
   </td>
  </tr>
  <tr>
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
  </tr>
    <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


#### Access and Deployment to AWS

* Follow these instructions: [https://github.com/trailofbits/algo/blob/master/docs/cloud-amazon-ec2.md](https://github.com/trailofbits/algo/blob/master/docs/cloud-amazon-ec2.md)
* Setup an Amazon Web Service account for hosting the VPN on EC2.
* Create an “IAM” user on AWS named something like “Algo VPN” with appropriate permissions. Make sure to use an IAM user with an acceptable policy attached (see https://github.com/trailofbits/algo/blob/master/docs/deploy-from-ansible.md).
* Run the VPN builder, select AWS EC2 and input the public/secret key for the “Algo VPN” account: 
  * Enter your aws_access_key (https://docs.aws.amazon.com/general/latest/gr/managing-aws-access-keys.html): *[AKIA...]:*
  * Enter your aws_secret_key (https://docs.aws.amazon.com/general/latest/gr/managing-aws-access-keys.html): *[ABCD...]:*


<table>
  <tr>
   <td>Strengths 
   </td>
   <td>Weaknesses
   </td>
   <td>Opportunities
   </td>
  </tr>
  <tr>
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
  </tr>
    <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>


#### VPN User Setup on Laptops and Mobile devices

* Follow these instructions: [https://github.com/trailofbits/algo#configure-the-vpn-clients](https://github.com/trailofbits/algo#configure-the-vpn-clients)
* Users will download Wireguard to their phones and laptops.
* Managers will share the setup configurations with users.
* Users finish setting up the VPN by importing config file or scanning the QR code.
* If WireGuard doesn’t work, users can use another setup method, but they will need more instructions.

<table>
  <tr>
   <td>Strengths 
   </td>
   <td>Weaknesses
   </td>
   <td>Opportunities
   </td>
  </tr>
  <tr>
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
  </tr>
    <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
</table>

### Alternative Option: Outline

Beyond using Algo, students can also try setting up Outline by Jigsaw (a Alphabet/Google initiative) to provide "a safer way for news organizations and journalists to access the internet." Visit https://getoutline.org/.

Follow a similar phased setup approach. 

### Wrap Up

Consider the following questions:

* Including security and usability, what other values should be considered when selecting a VPN?
* What are the advantages and disadvantages of using Algo versus Outline? Consider your threat model.
* What are the advantages and disadvantages of using either Algo or Outline versus a commercial VPN provider? Consider your threat model.
* Which contextual factors (PESTLE) may influence selecting one solution over another?

Document your findings and present your recommendations based on your experiences and the answers to the above questions.

