

##Installing the VMware VDDK
1. Download VDDK 6.x from the VMware website. (https://code.vmware.com/web/sdk/65/vddk)
2. SCP the downloaded file to the /tmp directory on the appliance. 
	-	(scp VMware-vix-disklib-6.5.0-5136645.x86_64.tar root@appliance:/tmp) Depending on the version the file will have a similar name. 
3. Decompress the GZIP archive file. (**tar -xvf VMware-vix-disklib-6.5.0-5136645.x86_64.tar.gz** or something similar.)
4. Prepare the /usr/lib/vmware-vix-disklib directory:
	- a. If the directory already exists, back up and remove the contents of this directory.
	- b. If the directory does not exist, create it: **mkdir /usr/lib/vmware-vix-disklib**
5. Under the decompressed archive file in the /tmp directory, there are several sub-directories. change directories to **vmware-vix-disklib-distrib.** Copy the following directories and their contents into the **/usr/lib/vmware-vix-disklib** directory using **cp -r**:

	- bin64
	- include
	- lib64

6. Run the following commands:

	- **ln -s /usr/lib/vmware-vix-disklib/lib64/libvixDiskLib.so /usr/lib/libvixDiskLib.so**
	- **ln -s /usr/lib/vmware-vix-disklib/lib64/libvixDiskLib.so.6 /usr/lib/libvixDiskLib.so.6**

7. Run the command **ldconfig**
8. Verify the configs are running;
	- run **ldconfig -p | grep -i vix**
	- The install has been completed successfully if the output is: 
		********- libvixDiskLib.so.6 (libc6,x86-64) => /lib/libvixDiskLib.so.6 libvixDiskLib.so (libc6,x86-64) => /lib/libvixDiskLib.so**tar 