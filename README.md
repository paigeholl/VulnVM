# **Creating the Base Vulnerability Scanner VM**

This VM will run Tenable vulnerability scans against the Cyber Range 2 environment.

Log in to Azure Portal

Search for "Virtual Machines" and select Create > Azure virtual machine

## **Basics Tab:**

Select your Resource Group: **Cyber Range 2**

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_qrGwXAppuTrQITEmYe.png width=400px>

Set Region to **East US 2**

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_biBHoN2rCz0U4JEGKD.png width=400px>

Set Availability Options to **No infrastructure redundancy required**

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_CWdiVZ4RMovnHL57VU.png width=400px>

Set Security Type to **Standard**

Set Image to **Windows 11 Pro**

Set Size to **Standard\_DS1\_v2** (1 vcpu, 3.5 GiB memory - \$41.61/month)

- Click "See all sizes" if not visible

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_goqIvEm6kT6iky2qrc.png width=400px>

Check the licensing agreement box

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_ihmKZM2V9NxiKVloqq.png width=400px>

Select **Next: Disks**

## **Disks Tab:**

Set OS disk type to **Standard SSD** (or Standard HDD)

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_t4bSUjtuwEU84yGEUn.png width=400px>

Select **Next: Networking**

## **Networking Tab:**

Set Virtual Network to **Cyber-Range-2-VNet (Cyber-Range-2-Admin)**

- If missing, verify Region and Resource Group settings

Set Subnet to **Cyber-Range-2-Subnet**

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_oUDTF0oamSF4L7SDcj.png width=400px>

Set Public IP to **None**

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_K1ibC95qxd49NY9AjC.png width=400px>

Set NIC network security group to **None**

Check **Delete public IP and NIC when VM is deleted**

<img src=https://ik.imagekit.io/typeai/tr:w-1200,c-at_max/img_NUfyD7jQ44dyvLcahE.png width=400px>

Select **Next: Management**

## **Management Tab:**

Set Boot diagnostics to **Disable**

Select **Review + Create**

Click **Create**

## **Post-Creation Tasks:**

Verify all resources created successfully in your Resource Group

To reset the VM password: Virtual Machines → Help → Reset Password

## **Stopping the VM:**

Navigate to your Resource Group

Select the Virtual Machine

Click **Stop**

## **Deleting the VM:**

Navigate to your Resource Group

Select the Virtual Machine

Click **Delete**

Verify associated resources (NICs, disks) are also removed from the Resource Group

