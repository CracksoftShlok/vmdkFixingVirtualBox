# How to Run .vmdk Files in VirtualBox – Set Up Kioptrix Hacking Lab in Minutes
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609214617.png?raw=true" style="width:100%; height:auto;" />

Virtual machines have become an essential tool for cybersecurity testing, system development, and software experimentation. Among the various formats used for virtual machine disk images, `.vmdk` is one of the most common. Created by VMware, this format is widely used across multiple platforms, including VirtualBox. In this post, we’ll explore what a `.vmdk` file is, how it works, and how you can use it in VirtualBox to set up a lab environment—specifically using the Kioptrix vulnerable machine as an example.

#### **What is a `.vmdk` File and How Does It Work?**

A `.vmdk` file is a virtual disk that acts like a physical hard drive inside a virtual machine. When you install an operating system on a virtual machine, all of its data—including system files, software, and user-generated content—is written to this virtual disk file. It's exactly like installing an OS on a regular hard drive, except everything is stored inside a single `.vmdk` file on your host system. Virtualization software such as VMware or VirtualBox reads from and writes to this file as if it were an actual hard disk. Depending on how the file was created, it can be a single large file or split into smaller parts. Some are preallocated at full size, while others grow as more data is added. Even though the `.vmdk` format was developed by VMware, it's compatible with VirtualBox as well, which makes it convenient for setting up virtual labs using prebuilt images.

#### **Setting Up the Kioptrix Lab in VirtualBox**

To demonstrate how to run a `.vmdk` file in VirtualBox, we’ll be using the Kioptrix vulnerable machine, a well-known target in the ethical hacking and penetration testing community.

To begin, make sure you have downloaded the `.vmdk` file for Kioptrix. Open VirtualBox and click the **New** button to create a new virtual machine. Assign it a name (for example, "Kioptrix"), choose the type as "Linux", and select the version (typically Ubuntu or Other Linux depending on the image). Allocate sufficient RAM—512 MB or more should be fine for this machine. On the hard disk selection screen, do **not** choose an ISO file.

<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609205625.png?raw=true" style="width:100%; height:auto;" />


After the virtual machine is created, click on **Settings** to configure it further.

<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609211543.png?raw=true" style="width:100%; height:auto;" />

Inside the settings window, go to the **Storage** section. 
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609211931.png?raw=true" style="width:100%; height:auto;" />
Click on the small disk icon next to the controller section.
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212151.png?raw=true" style="width:100%; height:auto;" />

On the left-hand panel, click the **add disk** icon.
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212253.png?raw=true" style="width:100%; height:auto;" />

Now browse to the directory where your `.vmdk` file is stored and select it.
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212335.png?raw=true" style="width:100%; height:auto;" />

Once the disk is added, you will see it appear under the list of attached storage devices.
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212520.png?raw=true" style="width:100%; height:auto;" />

Click **OK** to save the changes. You should now see the `.vmdk` listed in the storage settings of your virtual machine.

<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212620.png?raw=true" style="width:100%; height:auto;" />

Now go back to the main VirtualBox window and start the virtual machine. If the `.vmdk` file is bootable and correctly set up, your virtual machine will launch just like a regular computer.

If everything goes well, the Kioptrix machine will boot up and be ready for use.
<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212657.png?raw=true" style="width:100%; height:auto;" />

Congratulations! Your virtual lab is up and running using a `.vmdk` file in VirtualBox. This method is especially useful when working with preconfigured VMs or CTF (Capture the Flag) labs like Kioptrix. **Happy hacking!**

<img src="https://github.com/CracksoftShlok/vmdkFixingVirtualBox/blob/main/Pasted%20image%2020250609212753.png?raw=true" style="width:100%; height:auto;" />

If you found this blog helpful and enjoyed setting up your virtual lab with us, please consider sharing it with your friends, classmates, or fellow tech enthusiasts. Your support means the world to us—it not only motivates us to keep writing and sharing practical tutorials like this, but also helps more people learn and grow in the world of cybersecurity and virtualization. Thank you for being a part of our journey!
