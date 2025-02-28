---

copyright:
  years: 2018, 2023
lastupdated: "2023-08-14"

keywords:

subcollection: vpc

---

{{site.data.keyword.attribute-definition-list}}

# Creating virtual server instances
{: #creating-virtual-servers}

You can create one or more virtual server instances in your {{site.data.keyword.vpc_short}} by using the {{site.data.keyword.cloud_notm}} console, CLI, API, or Terraform.
{: shortdesc}

## Creating a virtual server instance with the UI
{: #creating-virtual-servers-ui}
{: ui}

Use the following steps to create a virtual server instance.

1. In the [{{site.data.keyword.cloud_notm}} console ![External link icon](../icons/launch-glyph.svg "External link icon")](/login), go to **menu icon ![menu icon](../icons/icon_hamburger.svg) > VPC Infrastructure > Compute > Virtual server instances**.

2. Click **Create** and begin by entering the information in Table 1.

   | Field | Value |
   |-------|-------|
   | Architecture | Select the processor architecture that your instance is created with. *x86* means x86_64 bit processor, and *s390x* is z Systems or LinuxONE (s390x processor architecture). |
   | Location | Locations are composed of regions (specific geographic areas) and zones (fault-tolerant data centers within a region). Select the location where you want to create your virtual server instance. |
   | Name  | A name is required for your virtual server instance. |
   | Resource group | Select a resource group for the instance. |
   | Tags | You can assign a user tag to the instance so that you can easily filter instance resources in your resource list. For more information, see [Working with tags](/docs/account?topic=account-tag&interface=ui).|
   | Access management tags | Access management tags help you apply flexible access policies on specific resources. For more information, see the [Controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial) UI tutorial. |
   {: caption="Table 1. Selections to begin instance provisioning" caption-side="bottom"}

3. Select an image and profile for the instance. You can select an image, a snapshot of a boot volume, or an existing boot volume. Table 2 describes image, snapshot, and existing volume options. Then, select a profile. Table 3 describes profile selection. {: #select-image-and-profile}

   | Field | Value |
   |-------|-------|
   | Image | To select from all available images, click **Change image**. You can select a stock image, custom image, or catalog image for the operating system.  \n - For more information about available stock images, see [x86 virtual server images](/docs/vpc?topic=vpc-about-images) and [s390x virtual server images](/docs/vpc?topic=vpc-vsabout-images). All operating system images use cloud-init that you can use to enter user metadata that is associated with the instance for post-provisioning scripts. Metadata isn't supported for {{site.data.keyword.cloud}} Hyper Protect Virtual Server for {{site.data.keyword.vpc_full}} instances and z/OS virtual server instances.  \n If you plan to use Windows operating systems with SQL Server, see the [About Microsoft SQL on VPC](/docs/microsoft?topic=microsoft-mssql-about).  \n - A `custom image` is an image that you create externally and import to {{site.data.keyword.cloud}}, which you can then import into {{site.data.keyword.vpc_short}}. For more information about custom images, see [Getting started with custom images](/docs/vpc?topic=vpc-planning-custom-images).  \n - You can also use a custom image that was created from a boot volume and was attached to an instance. For more information about creating an image from a volume, see [About creating an image from a volume](/docs/vpc?topic=vpc-image-from-volume-vpc).  \n - A `Catalog image` is a custom image that is imported into a private catalog. You can either import a custom image that was already imported into {{site.data.keyword.vpc_short}} or an image from a volume. For more information about catalog images, see [Custom images in a private catalog](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#custom-image-cloud-private-catalog).  \n **Note:** If you select a catalog image that belongs to a different account, you have more considerations and limitations to review. See [Using cross-account image references in a private catalog in the UI](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#private-catalog-image-reference-vpc-ui). To create a private catalog, see the tutorial [Onboarding a virtual server image for VPC](/docs/account?topic=account-catalog-vsivpc-tutorial&interface=ui).  \n - You can also select either an RHEL or Windows custom image and bring your own license (BYOL). For more information about creating BYOL custom images, see [Bring your own license](/docs/vpc?topic=vpc-byol-vpc-about).|
   | Snapshot | Select a snapshot of a boot volume that includes an operating system. \n - If you want to use another bootable snapshot, click **Change** to select a different snapshot from the list. \n - Filter the list of snapshots for [fast restore](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=ui#snapshots-vpc-use-fast-restore). With this option, you can create the boot volume quickly by using a snapshot that is cached in a different zone of your region. For more information about restoring a volume from a snapshot, see [Restoring a volume from a snapshot](/docs/vpc?topic=vpc-snapshots-vpc-restore). |
   | Existing volume | Select an existing boot volume that is not attached to an instance. \n * Select **Existing volumes** to view the existing volume option. Select **Change volume** to view a list of available boot volumes. Choose the volume that you want to use and select **Save volume** to continue. |
   {: caption="Table 2. Instance provisioning image, snapshot, or volume selections" caption-side="bottom"}
   {: #table-select-image-and-profile}
   
   | Field | Value |
   |-------|-------|
   | Profile |  To select from all available vCPU and RAM combinations, click **Change profile**. The profile families are Balanced, Compute, Memory, Ultra High Memory, Very High Memory, and GPU. For more information, see [Profiles](/docs/vpc?topic=vpc-profiles). When you create an {{site.data.keyword.cloud_notm}} {{site.data.keyword.hpvs}} for {{site.data.keyword.vpc_full}} instance, make sure that you select secure execution-enabled profiles, otherwise provisioning fails. For more information, see [s390x instance profiles](/docs/vpc?topic=vpc-vs-profiles). \n \n Some profiles might not be available because the amount of network interfaces in the virtual server exceed profile limits. You can remove network interfaces to select from more profiles. For more information, see [Resizing a virtual server](/docs/vpc?topic=vpc-resizing-an-instance). |
   {: caption="Table 3. Profile selections" caption-side="bottom"}

    _For z/OS virtual server instances only:_ z/OS virtual server instances require a minimum profile of 2 vCPUs x 16 GB RAM (2x16). One vCPU of the selected profile is reserved for running the service. When you select the profile for any z/OS stock images with RAM smaller than 8 GB, you might encounter the `IAR057D` message. For more information, see [IAR057D](https://www.ibm.com/docs/en/zos/2.5.0?topic=messages-iar057d){: external}.
    {: note}

4. Complete SSH keys, storage, and networking details by specifying the information in Table 3.

   | Field | Value |
   |-------|-------|
   | SSH keys | You must select an existing public SSH key or click **Create an SSH key** to create a new one. For more information about creating an SSH key, see [Creating your SSH key by using the UI](/docs/vpc?topic=vpc-ssh-keys&interface=ui#generate-ssh-keys-ui). SSH keys are used to securely connect to the instance after it's running. |
   | | **Note:**  SSH keys can either be RSA or Ed25519. You can generate new RSA key pairs using the UI. Pre-existing RSA and Ed25519 SSH keys can be uploaded. Ed25519 can be used only if the operating system supports this key type. Ed25519 can't be used with Windows or VMware images. |
   | | For more information, see [Getting started with SSH keys](/docs/vpc?topic=vpc-ssh-keys). |
   | Boot volume | The default boot volume size for most profiles is 100 GB. The default boot volume size for a z/OS virtual server instance is 250 GB. If you're importing a custom image, the boot volume capacity can be 10 - 250 GB, depending on what the image requires. Images that are smaller than 10 GB are rounded up to 10 GB. You can toggle the auto-delete option for the boot volume. |
   | |You can increase the size of the boot volume up to 250 GB by clicking the **Size** pencil icon. In the side panel, increase the boot volume size in the **Create size** field. The size must be more than the current size up to 250 GB. |
   | | You can edit the boot volume an add user tags to identify it in the resource list. |
   | Data volumes | You can create one or more secondary data volumes to be attached when you provision the instance. *For z/OS Wazi aaS custom image only*: If you want to use Hyper Protect encryption services for the boot volume, you can click **Create** and select Hyper Protect Crypto Services for the Encryption option.  |
   | |To create a data volume, click **Create** in the Data volumes section. Define the volume in the side panel. For more information about provisioning the volume, see [Create and attach a Block Storage volume when you create a new instance](/docs/vpc?topic=vpc-creating-block-storage#create-from-vsi). |
   | | Specify any user tags that you want to associate with the data volume you're creating and attaching to the instance. |
   | Virtual private cloud | Specify the IBM Cloud VPC where you want to create your instance. You can use the default VPC, another existing VPC, or you can create a new VPC. To create a new VPC, click **New VPC**. |
   | Network interfaces | By default the virtual server instance is created with a single primary network interface. You can click the pencil icon to edit the details of the network interface, for example, the subnet or security group that's associated with the interface. To include extra secondary network interfaces, click **New interface**. You can create and assign up to 15 network interfaces for your virtual server instance, depending on the vCPU count that is included in the instance profile. For more information, see [About network interfaces](/docs/vpc?topic=vpc-using-instance-vnics#about-network-interfaces). |
   {: caption="Table 4. Selections to complete instance provisioning" caption-side="bottom"}

5. For Advanced options, you can choose to complete more instance configurations.

   | Field | Value |
   |-------|-------|
   | User data | You can add user data that automatically performs common configuration tasks or runs scripts. For more information, see [User data](/docs/vpc?topic=vpc-user-data). For more information about using a contract to specify user data when you create an {{site.data.keyword.cloud}} Hyper Protect Virtual Server for {{site.data.keyword.vpc_full}} instance, see [About the contract](/docs/vpc?topic=vpc-about-contract_se). User data is not supported for z/OS virtual server instances. |
   | Metadata | Disabled by default. Click the toggle to enable. This setting informs the instance to collect the instance configuration information and user data. For more information, see [About instance metadata for VPC](/docs/vpc?topic=vpc-imd-about). Metadata isn't supported for {{site.data.keyword.cloud}} Hyper Protect Virtual Server for {{site.data.keyword.vpc_full}} instances and z/OS virtual server instances. |
   | Trusted profile (optional) | If you enable the metadata service, you can select a trusted profile and link it to this instance. Click **Select a trusted profile**. In the side panel, select a trusted profile and click **Select trusted profile** to link it to the instance. A message displays if none exist or if you don't have access to link it. For more information, see [Create a trusted profile](/docs/account?topic=account-trustedprofile-compute-tutorial#trusted-profile-compute-create). For more information about acquiring access, see [IAM authorizations for linking trusted profiles](/docs/vpc?topic=vpc-imd-trusted-profile-metadata&interface=ui#imd-iam-auth). |
   | Add to dedicated host | This selection is disabled by default. To create the virtual server instance in a single-tenant space, click the toggle to enable the dedicated host. To provision a dedicated instance, you must have a dedicated host available or [create one](/docs/vpc?topic=vpc-creating-dedicated-hosts-instances). z/OS virtual server instances do not support the dedicated type. |
   | Add to placement group | Placement groups are disabled by default. Click the toggle to enable placement groups. Then, select or create a placement group for the instance. If you add a placement group, the instance is placed according to the placement group policy. For more information, see [About placement groups](/docs/vpc?topic=vpc-about-placement-groups-for-vpc) |
   | Host failure auto restart | This setting is enabled by default. To disable host failure auto restart, click the toggle. For more information, see [Host failure recovery policies](/docs/vpc?topic=vpc-host-failure-recovery-policies&interface=ui). |
   {: caption="Table 5. Instance provisioning advanced options selections" caption-side="bottom"}

6. Click **Create virtual server instance** when you are ready to provision.

## Next steps after an instance is created in the UI
{: #next-steps-after-creating-virtual-servers-ui}
{: ui}

<!---A series of emails is sent to your administrator: Acknowledgment of the virtual server instance order, order approval and processing, and a message that the instance is created.--->

After the instance is created, you need to [associate a floating IP address to the instance](/docs/vpc?topic=vpc-creating-a-vpc-using-the-ibm-cloud-console#reserving-a-floating-ip-address). Then, you can connect to your instance. For more information, see [Connecting to your Linux instance](/docs/vpc?topic=vpc-vsi_is_connecting_linux), [Connecting to your Windows instance](/docs/vpc?topic=vpc-vsi_is_connecting_windows), or [Connecting to your z/OS instance](/docs/vpc?topic=vpc-vsi_is_connecting_zos).

If you have an existing instance with a floating IP address, it isn't necessary to assign a second floating IP to another instance. You can connect to the first instance with a floating IP, then SSH to the second instance by using the private subnet IP address that is automatically assigned to it.

## Creating a virtual server instance by using the CLI
{: #creating-virtual-servers-cli}
{: cli}

You can create instances by using the command-line interface (CLI). If you would like to use user tags or access management tags to manage your resources, see [Working with tags](/docs/account?topic=account-tag&interface=cli).

{{site.data.keyword.cloud_notm}} CLI is not supported on LinuxONE (s390x processor architecture). However, you can install the CLI on another supported platform and use it with LinuxONE (s390x processor architecture) virtual server instances.
{: note}

### Before you begin
{: #before-creating-virtual-servers-cli}
{: cli}

* Download, install, and initialize the following CLI plug-ins.
   - {{site.data.keyword.cloud_notm}} CLI
   - The infrastructure-service plug-in

   For more information, see [Setting up your API and CLI environment](/docs/vpc?topic=vpc-set-up-environment#cli-prerequisites-setup).

* Make sure that you [created a VPC](/docs/vpc?topic=vpc-creating-vpc-resources-with-cli-and-api&interface=cli).

### Gathering information to create an instance by using the CLI
{: #gather-info-to-create-virtual-servers-cli}
{: cli}

Ready to create an instance? Before you can run the `ibmcloud is instances` command, you need to know the details about the instance, such as what profile or image that you want to use.

Gather the following information by using the associated commands.

|    Instance details   |  Listing options                | VPC CLI reference documentation |
| --------------------- | --------------------------------|----------------------------|
| Image | `ibmcloud is image` | [List all images](/docs/vpc?topic=vpc-vpc-reference#images-list)|
| Boot volume | `ibmcloud is volumes` | [List all volumes](/docs/vpc?topic=vpc-vpc-reference#volumes-list) |
| Profile | `ibmcloud is instances` | [List all virtual server instances](/docs/vpc?topic=vpc-vpc-reference#instances-list) |
| Keys | `ibmcloud is keys` | [List all keys](/docs/vpc?topic=vpc-infrastructure-cli-plugin-vpc-reference#keys)  \n  \n If you don't have any available SSH keys, use [Create a key](/docs/vpc?topic=vpc-infrastructure-cli-plugin-vpc-reference#key-create) to create one.  \n  \n **Note:**  SSH keys can either be RSA or Ed25519. You can generate new RSA key pairs using the UI. Pre-existing RSA and Ed25519 SSH keys can be uploaded. Ed25519 can be used only if the operating system supports this key type. Ed25519 can't be used with Windows or VMware images.  \n For more information, see [Getting started with SSH keys](/docs/vpc?topic=vpc-ssh-keys). |
| VPC | `ibmcloud is vpcs` | [List all VPCs](/docs/vpc?topic=vpc-vpc-reference#vpcs-list) |
| Subnet | `ibmcloud is subnets` | [List all subnets](/docs/vpc?topic=vpc-vpc-reference#subnets-list) |
| Zone | `ibmcloud is zones` | [List all regions](/docs/vpc?topic=vpc-vpc-reference#zones-list) |
| Placement groups | `ibmcloud is placement-groups` | [List all placement groups](/docs/vpc?topic=vpc-vpc-reference#placement-groups-list) |
{: caption="Table 1. Required instance details" caption-side="bottom"}

Use the following commands to determine the required information for creating a new instance.

1. List the regions that are associated with your account.

   ```sh
   ibmcloud is regions
   ```
   {: pre}

   For this example, you see a response that is similar to the following output:
   ```sh
   Name       Endpoint                              Status
   us-south   https://us-south.iaas.cloud.ibm.com   available
   ```
   {: screen}

2. List the zones that are associated with the region.

   ```sh
   ibmcloud is zones us-south
   ```
   {: pre}

   For this example, you see a response that is similar to the following output.

   ```text
   Name         Region     Status
   us-south-1   us-south   available
   us-south-2   us-south   available
   us-south-3   us-south   available
   ```
   {: screen}

3. List the VPCs that are associated with your account.

   ```sh
   ibmcloud is vpcs
   ```
   {: pre}

   For this example, you see a response that is similar to the following output.

   ```text
   ID                                        Name       Status     Classic access   Default network ACL              Default security group        Resource group
   r134-35b9cf35-616e-462e-a145-cf8db4062fcf my-vpc     available  false            immortality-casing-extoll-exit   enhance-corsage-managing-jinx Default
   ```
   {: screen}

   If you do not have an available VPC, you can create one by using the **`ibmcloud is vpc-create`** command. For more information about creating a VPC, see [ibmcloud is vpc-create](/docs/vpc?topic=vpc-vpc-reference#vpc-create).

4. List the subnets that are associated with the {{site.data.keyword.vpc_short}}.

   ```sh
   ibmcloud is subnets
   ```
   {: pre}

   For this example, you see a response that is similar to the following output.

   ```text
   ID                                          Name            Status      Subnet CIDR      Addresses   ACL                              Public Gateway   VPC
   Zone         Resource group
   0726-198db988-3b9b-4cfa-9dec-0206420d37d0   my-subnet       available   10.240.64.0/28   7/16        immortality-casing-extoll-exit   -               my-vpc
   us-south-2   Default
   ```
   {: screen}

   If you do not have a subnet available, you can create one by using the **`ibmcloud is subnet-create`** command. For more information about creating a subnet, see [ibmcloud is subnet-create](/docs/vpc?topic=vpc-vpc-reference#subnet-create).

5. List the available profiles for creating your instance.

   ```sh
   ibmcloud is instance-profiles
   ```
   {: pre}

   For this example, you see a response that is similar to the following output.

   ```text
   Name                         vCPU Manufacturer   Architecture   Family              vCPUs   Memory(GiB)   Bandwidth(Mbps)   Volume bandwidth(Mbps)   GPUs          Storage(GB)   Min NIC Count   Max NIC Count
   bx2-2x8                      intel               amd64          balanced            2       8             4000              1000                     -      -                    1               5
   bx2a-2x8                     amd                 amd64          balanced            2       8             2000              500                      -      -                    1               5
   bx2d-2x8                     intel               amd64          balanced            2       8             4000              1000                     -            1x75          1               5
   bx2-4x16                     intel               amd64          balanced            4       16            8000              2000                     -      -                    1               5
   bx2a-4x16                    amd                 amd64          balanced            4       16            4000              1000                     -      -                    1               5
   bx2d-4x16                    intel               amd64          balanced            4       16            8000              2000                     -            1x150         1               5
   ```
   {: screen}

   For more information about available profiles, see [x86 instance profiles](/docs/vpc?topic=vpc-profiles) and [s390x instance profiles](/docs/vpc?topic=vpc-vs-profiles).

   Secure execution-enabled profiles are now available and are identified by the fourth character of the profile name that is an "e", such as *bz2e*. For more information, see [Confidential computing with LinuxONE](/docs/vpc?topic=vpc-about-se).

   The secure execution-enabled profiles are available for Balanced, Compute, and Memory families. Make sure that you use secure-enabled profiles when you use the IBM Hyper Protect Container Runtime image. Profile validation for the IBM-provided stock images and the IBM Hyper Protect Container Runtime occurs in the RIAS layer. Any profile mismatch results in an error message that is similar to the following example.

   ```text
   FAILED
   Response HTTP Status Code: 400
   Error code: bad_field
   Error message: Image OS IBM Hyper Protect is not supported by the instance profile <profile_name>
   Error target name: profile, type: field
   ```
   {: screen}

6. List the available stock images, custom images, or images that are shared with your account from a private catalog for creating your instance. If you are creating an instance from an existing boot volume, skip this step.

   * To list all available stock or custom images, run the following command.

      ```sh
      ibmcloud is images
      ```
      {: pre}

      For this example, you see a response that is similar to the following output.

      ```text
      ID                                          Name                               Status       Arch    OS name                   OS version       File size(GB)
      Visibility   Owner type   Encryption   Resource group   Catalog Offering
      r134-24d856e2-6aec-41c2-8f36-5a8a3766f0d6   ibm-centos-7-9-minimal-amd64-9     available    amd64   centos-7-amd64            7.x - Minimal Install  1             public       provider     none         Default          -
      r134-9768bb7f-c75d-4408-ba34-61015632f907   ibm-debian-10-13-minimal-amd64-2   available    amd64   debian-10-amd64           10.x Buster/Stable     1             public       provider     none         Default          -
      r134-f83ce520-00b5-40c5-9938-a5c82a273f91   ibm-debian-11-3-minimal-amd64-4    available    amd64   debian-11-amd64           11.x Bullseye/Stable   1
      ```
      {: screen}

      For a full list of command options, see [ibmcloud is images](/docs/vpc?topic=vpc-vpc-reference#images-list).

      Deprecated images do not include the most current support.
      {: tip}

   * To list all available images shared from a private catalog, run the following commands:

      If you select a catalog image that belongs to a different account, you have extra considerations and limitations to review. See [Using cross-account image references in a private catalog in the CLI](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#private-catalog-image-reference-vpc-cli)
      {: note}

       - To list all available private catalog image offerings, run the following command.

          ```sh
          ibmcloud is catalog-image-offerings
          ```
          {: pre}

          This command returns the identifier of each image offering and the identifier of the private catalog where the image is. Save the `offering_id` and `catalog_id` in variables, which are used later to provision an instance.

          ```sh
          offering_id=6bf79f7b-de48-4ce8-8cae-866b376f2889
          catalog_id=71306253-8444-4cae-a45d-64d35e5393ec
          ```
          {: pre}

       - To get the `offering_crn` for the offering and the `offering_version_crn` for each version in the offering, run the following command.

          ```sh
          ibmcloud is catalog-image-offering $catalog_id $offering_id
          ```
          {: pre}

       When you provision an instance, you can either provision the instance from the private catalog-managed image in the latest version in a catalog product offering by using the `offering_crn` value or from the specific version in the catalog product offering by using the `offering_version_crn` value.

       Save the `offering_crn` and `offering_version_crn`in variables, which are used later to provision an instance.

       ```sh
       offering_crn="crn:v1:staging:public:globalcatalog-collection:global:a/efe5afc483594adaa8325e2b4d1290df:0b322820-dafd-4b5e-b694-6465da6f008a:offering:136559f6-4588-4af2-8585-f3c625eee09d"
       offering_version_crn="crn:v1:staging:public:globalcatalog-collection:global:a/efe5afc483594adaa8325e2b4d1290df:0b322820-dafd-4b5e-b694-6465da6f008a:version:136559f6-4588-4af2-8585-f3c625eee09d/8ae92879-e253-4a7c-b09f-8d30af12e518"
       ```
       {: pre}

7. List the available boot volumes for creating your instance.
   If you are creating an instance from an image, skip this step.
   To create an instance from an existing volume, you must use a volume compatible with the instance options chosen previously. A compatible volume is in the same zone as the instance that is being provisioned, in an unattached state, and has an OS compatible with the profile that is selected in step 5.
   Use the `volumes` subcommand to see the compatible volumes.
   For example, to see unattached volumes with an x64 operating system architecture in `us-south-1`:

   ```sh
   ibmcloud is volumes --attachment-state unattached  --operating-system-architecture amd64 --zone us-south-1
   ```
   {: pre}

   You can optionally [create a boot volume from a bootable snapshot](#create-instance-bootable-snapshot-cli) and use that for your image. To list all snapshots for a volume, see [View all snapshots that were created from the Block Storage for VPC volume](/docs/vpc?topic=vpc-viewing-block-storage&interface=ui#view-snapshots-for-volume).

8. List the available SSH keys that you can associate with your instance.

   ```sh
   ibmcloud is keys
   ```
   {: pre}

   For this example, you see a response that is similar to the following output.

   ```text
   ID                                          Name     Type   Length   FingerPrint          Resource group
   r134-89ec781c-9630-4f76-b9c4-a7d204828d61   my-key   rsa    4096     gtnf+pdX2PYI9Ofq..   Default
   ```
   {: screen}

   If you do not have an SSH key available, you can create an SSH key by using the [ibmcloud is key-create](/docs/vpc?topic=vpc-vpc-reference#key-create) command. For more information, see [SSH keys](/docs/vpc?topic=vpc-ssh-keys).

9. List all the available placement groups that you can associate with your instance.

    ```sh
    ibmcloud is placement-groups
    ```
    {: pre}

    For this example, you see a response that is similar to the following output.

    ```text
    ID                                            Name                             State    Strategy       Resource Group
    c5f1f366-b92a-4080-991a-aa5c2e33d96b          placement-group-region-us-south   stable   power_spread  Default
    ```
    {: screen}

### Creating an instance by using the CLI
{: #create-instance-cli}
{: cli}

Use the following information to create an instance with the CLI.

### Provision from a stock or custom image
{: #instance-create-from-image-cli}
{: cli}

After you know the needed values, use them to run the **`ibmcloud is instance-create`** command. You also need to specify a unique name for the instance.

Use the following steps to create a basic virtual server instance from a stock image by using the CLI. By default, a boot volume is attached to the instance when the instance is created. For most virtual server instances, the default boot volume size is 100 GB. The default boot volume size for a z/OS virtual server instance is 250 GB.

1. Create an instance by using the following command.

   ```sh
   ibmcloud is instance-create \
       INSTANCE_NAME \
       VPC \
       ZONE_NAME \
       PROFILE_NAME \
       SUBNET \
       --image IMAGE \
       --keys KEYS \
   ```
   {: pre}

   For example, the following `instance-create` command uses the sample values that are found in the [Gathering information](#gather-info-to-create-virtual-servers-cli) section.

   ```sh
   ibmcloud is instance-create \
       my-instance \
       r134-35b9cf35-616e-462e-a145-cf8db4062fcf \
       us-south-2 \
       bx2-2x8 \
       0726-198db988-3b9b-4cfa-9dec-0206420d37d0 \
       --image r134-f83ce520-00b5-40c5-9938-a5c82a273f91 \
       --keys r134-89ec781c-9630-4f76-b9c4-a7d204828d61 \
   ```
   {: pre}

   Where the following argument and option values are used

      * INSTANCE_NAME: `my-instance`
      * VPC: `r134-35b9cf35-616e-462e-a145-cf8db4062fcf`
      * ZONE_NAME: `us-south-2`
      * PROFILE_NAME: `bx2-2x8`
      * SUBNET: `0726-198db988-3b9b-4cfa-9dec-0206420d37d0`
      * IMAGE: Debian 11 image `r134-f83ce520-00b5-40c5-9938-a5c82a273f91`
      * KEYS: `r134-89ec781c-9630-4f76-b9c4-a7d204828d61`

   The response varies depending on the option values that you use.
   {: note}

   ```text
   ID                                    0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0
   Name                                  my-instance
   CRN                                   crn:v1:public:is:us-south-2:a/2d1bace7b46e4815a81e52c6ffeba5cf::instance:0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0
   Status                                pending
   Availability policy on host failure   restart
   Startable                             true
   Profile                               bx2-2x8
   Architecture                          amd64
   vCPU Manufacturer                     intel
   vCPUs                                 2
   Memory(GiB)                           8
   Bandwidth(Mbps)                       4000
   Volume bandwidth(Mbps)                1000
   Network bandwidth(Mbps)               3000
   Lifecycle Reasons                     Code   Message
                                          -      -

   Lifecycle State                       pending

   Metadata service                      Enabled   Protocol   Response hop limit
                                         false     http       1

   Image                                 ID                                          Name
                                         r134-f83ce520-00b5-40c5-9938-a5c82a273f91   ibm-debian-11-3-minimal-amd64-4

   VPC                                   ID                                          Name
                                         r134-35b9cf35-616e-462e-a145-cf8db4062fcf   my-vpc

   Zone                                  us-south-2
   Resource group                        ID                                 Name
                                         cdc21b72d4e647b195de988b175e3d82   Default

   Created                               2023-03-23T21:50:24+00:00
   Boot volume                           ID   Name   Attachment ID                               Attachment name
                                         -    -      0726-7ccd4284-e59d-45d8-932a-9e52f62f187a   landing-faucet-prankish-sprout
   ```
   {: screen}

   Information about the network interfaces that are created for the new instance aren't returned after the instance is created. You can view the information by using the `ibmcloud is instance INSTANCE` command as described in the following step. The status displays *pending* until the instance is created.

   For more information about some additional features that you can include as command options on the `instance-create` command, see the following topics: [Create a volume attachment JSON](/docs/vpc?topic=vpc-attaching-block-storage&interface=cli#volume_attachment_json), [Enable or disable the metadata service](/docs/vpc?topic=vpc-imd-configure-service&interface=cli#imd-enable-on-instance-cli), and [Creating a placement group](/docs/vpc?topic=vpc-managing-placement-group&interface=cli#creating-placement-group-CLI).
   {: tip}

   For a full list of command options, see [ibmcloud is instance-create](/docs/vpc?topic=vpc-vpc-reference#instance-create).

2. Next, run the following `instance` details command to verify that you can see your new instance and view the network interfaces that were created for the new instance. `0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0` is the virtual server instance ID that was assigned when the instance was created in the previous step.

   ```sh
   ibmcloud is instance 0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0
   ```
   {: pre}

   For this example, you see the following response. The status now shows *running*. Check the Network Interfaces section to locate the ID of the network interface.

   ```text
   ID                                    0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0
   Name                                  my-instance
   CRN                                   crn:v1:public:is:us-south-2:a/2d1bace7b46e4815a81e52c6ffeba5cf::instance:0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0
   Status                                running
   Availability policy on host failure   restart
   Startable                             true
   Profile                               bx2-2x8
   Architecture                          amd64
   vCPU Manufacturer                     intel
   vCPUs                                 2
   Memory(GiB)                           8
   Bandwidth(Mbps)                       4000
   Volume bandwidth(Mbps)                1000
   Network bandwidth(Mbps)               3000
   Lifecycle Reasons                     Code   Message
                                          -      -

   Lifecycle State                       stable

   Metadata service                      Enabled   Protocol   Response hop limit
                                         false     http       1

   Image                                 ID                                          Name
                                         r134-f83ce520-00b5-40c5-9938-a5c82a273f91   ibm-debian-11-3-minimal-amd64-4

   VPC                                   ID                                          Name
                                         r134-35b9cf35-616e-462e-a145-cf8db4062fcf   my-vpc

   Zone                                  us-south-2
   Resource group                        ID                                 Name
                                         cdc21b72d4e647b195de988b175e3d82   Default

   Created                               2023-03-23T21:50:24+00:00
   Network Interfaces                    Interface   Name      ID                                          Subnet            Subnet ID                                   Floating IP   Security Groups                 Allow source IP spoofing   Reserved IP
                                         Primary     primary   0726-4db768bb-65c3-4045-8712-523e62eeabd2   my-subnet   0726-198db988-3b9b-4cfa-9dec-0206420d37d0         -             enhance-corsage-managing-jinx   false                      10.240.64.10

   Boot volume                           ID                                          Name                           Attachment ID                                    Attachment name
                                         r134-7a1d72d1-56ac-438e-bf85-6c0173e3f9a6   expend-anger-whiff-jackknife   0726-7ccd4284-e59d-45d8-932a-9e52f62f187a        landing-faucet-prankish-sprout
   ```
   {: screen}

3. Request a floating IP address to associate to your instance by using the following command. The name that is specified for the floating IP is `my-floatingip`. `0726-4db768bb-65c3-4045-8712-523e62eeabd2` is the ID of the network interface for the virtual server instance that displayed in the previous step.

   ```sh
   ibmcloud is floating-ip-reserve \
       my-floatingip \
       --nic 0726-4db768bb-65c3-4045-8712-523e62eeabd2
   ```
   {: pre}

   For this example, you see a response that is similar to the following output.

   ```text
   ID               r134-9b79b9bc-a2dc-4337-865a-57d9b9198b76
   Address          169.59.214.164
   Name             my-floatingip
   CRN              crn:v1:public:is:us-south-2:a/2d1bace7b46e4815a81e52c6ffeba5cf::floating-ip:r134-9b79b9bc-a2dc-4337-865a-57d9b9198b76
   Status           available
   Zone             us-south-2
   Created          2023-03-23T22:13:07+00:00
   Target           ID                                          Target type         Instance ID                                 Target interface name   Target interface private IP
                    0726-4db768bb-65c3-4045-8712-523e62eeabd2   network_interface   0726_67b1179a-8b25-4ac9-8bc0-7f3027466ed0   primary                 -


   Resource group   ID                                 Name
                    cdc21b72d4e647b195de988b175e3d82   Default
   ```
   {: screen}

    Record the floating IP `Address` to use later.

    For a full list of command options, see [ibmcloud is floating-ip-reserve](/docs/vpc?topic=vpc-vpc-reference#floating-ip-reserve).

Need more help? You can always run `ibmcloud is instance-create --help` to display help for creating an instance.
{: tip}

### Provision from a private catalog image
{: #instance-create-from-private-catalog-image-cli}
{: cli}

After you know the needed values, use them to run the **`ibmcloud is instance-create`** command. You also need to specify a unique name for the instance.

Use the following steps to create a virtual server instance from a private catalog offering or a catalog offering version by using the CLI.

1. Create an instance by using the following command.

   ```sh
   ibmcloud is instance-create \
       INSTANCE_NAME \
       VPC \
       ZONE_NAME \
       PROFILE_NAME \
       SUBNET \
       --catalog-offering <CRN for the IBM Cloud catalog offering> or --catalog-offering-version <The CRN for the version of a IBM Cloud catalog offering> \
       --keys KEYS \
       --placement-group PLACEMENT_GROUP_NAME \
   ```
   {: pre}

   For example, if you create an instance that is called *my-instance* in *us-south-2* and use the *bx2-2x8* profile and the catalog offering, your `instance-create` command looks similar to the following example.

   ```sh
   ibmcloud is instance-create\
       my-instance\
       r134-35b9cf35-616e-462e-a145-cf8db4062fcf\
       us-south-2\
       bx2-2x8\
       0726-198db988-3b9b-4cfa-9dec-0206420d37d0\
       --catalog-offering crn:v1:public:globalcatalog-collection:global:a/efe5afc483594adaa8325e2b4d1290df:0b322820-dafd-4b5e-b694-6465da6f008a:offering:136559f6-4588-4af2-8585-f3c625eee09d
       --keys r134-89ec781c-9630-4f76-b9c4-a7d204828d61\
       --placement-group c5f1f366-b92a-4080-991a-aa5c2e33d96b\
   ```
   {: pre}

   Where the following argument and option values are used

      * INSTANCE_NAME: `my-instance`
      * VPC: `r134-35b9cf35-616e-462e-a145-cf8db4062fcf`
      * ZONE_NAME: `us-south-2`
      * PROFILE_NAME: `bx2-2x8`
      * SUBNET: `0726-198db988-3b9b-4cfa-9dec-0206420d37d0`
      * CATALOG-OFFERING: is `crn:v1:public:globalcatalog-collection:global:a/efe5afc483594adaa8325e2b4d1290df:0b322820-dafd-4b5e-b694-6465da6f008a:offering:136559f6-4588-4af2-8585-f3c625eee09d`
      * KEYS: `r134-89ec781c-9630-4f76-b9c4-a7d204828d61`
      * PLACEMENT_GROUP: `c5f1f366-b92a-4080-991a-aa5c2e33d96b`

   Information about the network interfaces that are created for the new instance aren't returned after the instance is created. You can view the information by using the `ibmcloud is instance INSTANCE` command as described in the following step.

   The status of the virtual server instance displays *pending* until the instance is created.
   {: note}

   For a full list of command options, see [ibmcloud is instance-create](/docs/vpc?topic=vpc-vpc-reference#instance-create).

2. Next, run the following `instance` details command to verify that you can see your new instance and view the network interfaces that were created for the new instance. For `INSTANCE` specify the ID that was assigned to your new virtual server instance in the previous step.

   ```sh
   ibmcloud is instance INSTANCE
   ```
   {: pre}

   The status now shows *running*. Check the Network Interfaces section to locate the ID of the network interface.

3. Request a floating IP address to associate to your instance by using the following command. For `FLOATING_IP_NAME` specify a name for your floating IP, and for `TARGET_INTERFACE` specify the ID of the network interface that you identified in the previous step.

   ```sh
   ibmcloud is floating-ip-reserve \
       FLOATING_IP_NAME \
       --nic TARGET_INTERFACE
   ```
   {: pre}

    Record the floating IP `Address` to use later.

    For a full list of command options, see [ibmcloud is floating-ip-reserve](/docs/vpc?topic=vpc-vpc-reference#floating-ip-reserve).

Need more help? You can always run `ibmcloud is instance-create --help` to display help for creating an instance.
{: tip}

### Provision from an existing volume
{: #create-instance-volume-cli}
{: cli}

After you know the needed values, use them to run the `instance-create` command. You also need to specify a unique name for the instance.

Use the following steps to create a virtual server instance from a bootable volume, and that includes a volume attachment.

1. Create an instance by using the following command.

   ```sh
   ibmcloud is instance-create \
       INSTANCE_NAME \
       VPC \
       ZONE_NAME \
       PROFILE_NAME \
       SUBNET \
       --boot-volume VOLUME_ID \
       --keys KEYS \
       --volume-attach VOLUME_ATTACH_JSON \
   ```
   {: pre}

   For example, if you create an instance that is called *my-instance* in *us-south-1* and use the *bx2-2x8* profile and an existing boot volume, your `instance-create` command looks similar to the following example.

   ```sh
   ibmcloud is instance-create\
       my-instance\
       r134-35b9cf35-616e-462e-a145-cf8db4062fcf\
       us-south-1\
       bx2-2x8\
       0726-198db988-3b9b-4cfa-9dec-0206420d37d0\
       --boot-volume r006-feec3e99-995e-4e8f-896b-48b42c7d05a7\
       --keys r134-89ec781c-9630-4f76-b9c4-a7d204828d61\
       --volume-attach @/Users/myname/myvolume-attachment_create.json\
   ```
   {: pre}

   For an example volume attachment JSON file, see [Create a volume attachment JSON](/docs/vpc?topic=vpc-attaching-block-storage&interface=cli#volume_attachment_json). You can also include [user tags for the volumes](/docs/vpc?topic=vpc-creating-block-storage&interface=cli#create-instance-vol-cli) in the volume attachment.

   Information about the network interfaces that are created for the new instance aren't returned after the instance is created. You can view the information by using the `ibmcloud is instance INSTANCE` command as described in the next step.

   The status displays *pending* until the instance is created.
   {: note}

   For a full list of command options, see [ibmcloud is instance-create](/docs/vpc?topic=vpc-vpc-reference#instance-create).

2. Next, run the following `instance` details command to verify that you can see your new instance and view the network interfaces that were created for the new instance. For `INSTANCE` specify the ID that was assigned to your new virtual server instance in the previous step.

   ```sh
   ibmcloud is instance INSTANCE
   ```
   {: pre}

   The status now shows *running*. Check the Network Interfaces section to locate the ID of the network interface.

3. Request a floating IP address to associate to your instance by using the following command. For `FLOATING_IP_NAME` specify a name for your floating IP, and for `TARGET_INTERFACE` specify the ID of the network interface that you identified in the previous step.

   ```sh
   ibmcloud is floating-ip-reserve \
       FLOATING_IP_NAME \
       --nic TARGET_INTERFACE
   ```
   {: pre}

   Record the floating IP `Address` to use later.

   For a full list of command options, see [ibmcloud is floating-ip-reserve](/docs/vpc?topic=vpc-vpc-reference#floating-ip-reserve).

   Need more help? You can always run `ibmcloud is instance-create --help` to display help for creating an instance.
   {: tip}

### Create a boot volume from a snapshot and use it to provision a new instance with the CLI
{: #create-instance-bootable-snapshot-cli}

You can create a boot volume from a bootable [snapshot](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=ui#snapshots-vpc-restore-concepts) and use that for your image. When you run the `ibmcloud is instance-create` command, specify the `source_snapshot` subproperty in the boot volume JSON and the ID or name of a bootable snapshot. For an example, see [Create a boot volume from a snapshot for a new instance from the CLI](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=cli#snapshots-vpc-restore-boot-CLI).

## Next steps after an instance is created from the CLI
{: #next-step-after-creating-virtual-servers-cli}
{: cli}

A series of emails is sent to your administrator: Acknowledgment of the virtual server instance order, order approval and processing, and a message that the instance is created.

If you choose a GPU profile, see [Managing GPUs](/docs/vpc?topic=vpc-managing-gpus).

After the instance is created, associate a floating IP address to the instance. Then, you can connect to your instance. For more information, see [Connecting to your Linux instance](/docs/vpc?topic=vpc-vsi_is_connecting_linux) or [Connecting to your Windows instance](/docs/vpc?topic=vpc-vsi_is_connecting_windows).

## Creating a virtual server instance by using the API
{: #create-instance-api}
{: api}

You can create instances by using the API.

### Before you begin
{: #before-you-begin-create-instance-api}
{: api}

Ensure that you have the required access. To call these methods, you must be assigned one or more IAM access roles that include the following actions, depending on any listed conditions. You can check your access by going to the **Users** page of [{{site.data.keyword.iamshort}} dashboard](https://test.cloud.ibm.com/iam/overview){: external}.

### Gathering information to create an instance by using the API
{: #gather-info-to-create-virtual-servers-api}
{: api}

Before you can create an instance, you need to know the details about the instance, such as the instance profile or the image that you want to use. Gather information by making the following API calls:

|    Instance details   |  Listing options                | API spec documentation
| --------------------- | ------------------------------- | ----------------------------------------------------------------------
| Image                 | `GET /images`                   | [List all images](/apidocs/vpc/latest#list-images)
| Profile               | `GET /instance/profiles`        | [List all instance profiles](/apidocs/vpc/latest#list-instance-profiles)
| Key                   | `GET /keys`                     | [List all keys](/apidocs/vpc/latest#list-keys)
| VPC                   | `GET /vpcs`                     | [List all VPCs](/apidocs/vpc/latest#list-vpcs)
| Subnet                | `GET /subnets`                  | [List all subnets](/apidocs/vpc/latest#list-subnets)
| Zone                  | `GET /regions/<region>/zones`   | [List all zones in a region](/apidocs/vpc/latest#list-region-zones)
| Placement groups      | `GET /placement_groups`         | [List all placement groups](/apidocs/vpc/latest#list-placement-groups)
{: caption="Table 2. Required instance details api" caption-side="bottom"}

### Creating an instance by using the API
{: #create-vsi-api}
{: api}

After you retrieved the information that you need, you can run the [`POST /instances`](/apidocs/vpc/latest#create-instance) method to create an instance.

### Provision an instance from a stock or custom image by using the API
{: #create-instance-stock-custom-image-api}
{: api}

You can provision an instance with a stock or custom image by specifying the image's `id` subproperty as the value of the `image` property.

 ```bash
    curl -X POST "$vpc_api_endpoint/v1/instances?version=$api_version&generation=2" \
      -H "Authorization:$iam_token" \
      -d '{
            "name": "my-instance",
            "zone": {
              "name": "us-south-3"
            },
            "vpc": {
              "id": "'$vpc'"
            },
            "primary_network_interface": {
              "subnet": {
                "id": "'$subnet'"
              }
            },
            "keys":[{"id": "'$key'"}],
            "profile": {
              "name": "'$profile_name'"
             },
            "image": {
              "id": "'$image_id'"
             }
            }'
 ```
 {: pre}

### Provision an instance from a private catalog image by using the API
{: #create-instance-private-catalog-image-api}
{: api}

You can provision an instance with a private catalog image by specifying the image's `offering_crn` or the `version_crn` subproperty as the value of the `catalog_offering` property.

* Create an instance by using a private catalog image from the latest version of a catalog product offering.

    ```bash
    curl -X POST "$vpc_api_endpoint/v1/instances?version=$api_version&generation=2" \
      -H "Authorization:$iam_token" \
      -d '{
            "name": "my-instance",
            "zone": {
              "name": "us-south-3"
            },
            "vpc": {
              "id": "'$vpc'"
            },
            "primary_network_interface": {
              "subnet": {
                "id": "'$subnet'"
              }
            },
            "keys":[{"id": "'$key'"}],
            "profile": {
              "name": "'$profile_name'"
             },
            "catalog_offering": {
              "offering": {
                "crn": "'$offering_crn'"
             }
            }'
    ```
    {: pre}

* Create an instance by using a private catalog image from a specific version of a catalog product offering.

    ```bash
    curl -X POST "$vpc_api_endpoint/v1/instances?version=$api_version&generation=2" \
      -H "Authorization:$iam_token" \
      -d '{
            "name": "my-instance",
            "zone": {
              "name": "us-south-3"
            },
            "vpc": {
              "id": "'$vpc'"
            },
            "primary_network_interface": {
              "subnet": {
                "id": "'$subnet'"
              }
            },
            "keys":[{"id": "'$key'"}],
            "profile": {
              "name": "'$profile_name'"
             },
            "catalog_offering": {
              "version": {
                "crn": "'$version_crn'"
             }
            }'
    ```
    {: pre}

### Provision from an existing volume
{: #create-instance-ipbv-api}
{: api}

Reusing an existing, bootable volume is faster than creating a new volume from a snapshot or an image.

You can provision an instance with an existing volume by specifying the existing volume's `id` or `crn` subproperty as the value of the `boot_volume_attachment` property.

The existing, bootable volume must be an unattached bootable volume that has the same operating system and architecture as the instance profile. Use the [list volumes](/apidocs/vpc/latest#list-volumes) filter and reference the `attachment_state` property and `operating_system` property to view a volume's eligibility.

For example, to see unattached volumes in `us-south-1` with an x86 operating system.

```sh
curl -X GET "$vpc_api_endpoint/v1/volumes?version=2023-02-08&generation=2?attachment_state=unattached&zone.name=us-south-1&operating_system.architecture=amd64"
-H "Authorization: Bearer $iam_token"
```

By default, a boot volume that is created as part of provisioning a virtual server instance is deleted when the instance is deleted. You can control this behavior by setting the `delete_volume_on_instance_delete` property to `true` when you create the instance or update the boot volume attachment.

Use the [`POST /instances`](/apidocs/vpc/latest#create-instance) method to create an instance with the information you gathered. The following call is an example of provisioning an instance by using an existing boot volume.

```sh
curl -X POST "$vpc_api_endpoint/v1/instances?version=2023-02-08&generation=2"
-H "Authorization: Bearer $iam_token"
-d '{
  "boot_volume_attachment": {
    "volume": {
      "id": "r006-feec3e99-995e-4e8f-896b-48b42c7d05a7"
    }
  },
  "keys": [
    {
      "id": "363f6d70-0000-0001-0000-00000013b96c"
    }
  ],
  "name": "my-instance",
  "placement_target": {
    "id": "0787-8c2a09be-ee18-4af2-8ef4-6a6060732221"
  },
  "primary_network_interface": {
    "name": "my-network-interface",
    "subnet": {
      "id": "bea6a632-5e13-42a4-b4b8-31dc877abfe4"
    }
  },
  "profile": {
    "name": "bx2-2x8"
  },
  "volume_attachments": [
    {
      "volume": {
        "capacity": 1000,
        "encryption_key": {
          "crn": "crn:[...]"
        },
        "name": "my-data-volume",
        "profile": {
          "name": "5iops-tier"
        }
      }
    }
  ],
  "vpc": {
    "id": "f0aae929-7047-46d1-92e1-9102b07a7f6f"
  },
  "zone": {
    "name": "us-south-1"
  }
}'
```

For more information, see [Create an instance](/apidocs/vpc/latest#create-instance).

### Restore a boot volume from a snapshot and use it to provision a new instance
{: #create-instance-bootable-snapshot-api}
{: api}

You can [restore](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=api#snapshots-vpc-restore-concepts) a boot volume from a bootable snapshot and then use that boot volume when you provision an instance. The bootable snapshot must have the same operating system and architecture as the instance profile.

In the `POST /instances` request, specify the `boot_volume_attachment` property and the bootable snapshot ID in the `source_snapshot` subproperty. For example,

```curl
curl -X POST \
"$vpc_api_endpoint/v1/instances?version=2023-03-07&generation=2" \
-H "Authorization: $iam_token" \
-H "Content-Type: application/json" \
-d '{
      "boot_volume_attachment": {
        "delete_volume_on_instance_delete": true,
        "volume": {
            "profile": {
                "name": "general-purpose"
            },
            "source_snapshot": {
                "id": "eb373975-4171-4d91-81d2-c49efb033753"
            }
        }
     },
     .
     .
     .
  }'
```
{: codeblock}

For more information about restoring a volume with the API, see [Restore a volume from a snapshot with the API](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=api#snapshots-vpc-restore-API).

## Creating virtual server instances by using Terraform
{: #create-instance-terraform}
{: terraform}

You can create instances by using Terraform. If you would like to use user tags or access management tags to manage your resources, see [Working with tags](/docs/account?topic=account-tag&interface=terraform).

### Before you begin
{: #before-you-begin-create-instance-terraform}
{: terraform}

Make sure that you set up [Terraform for VPC](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest).

### Creating a private catalog
{: #terraform-create-private-catalog}
{: terraform}

This step is optional. If you plan to share images from a private catalog, the private catalog must be created first. If you select a catalog image that belongs to a different account, review [Using cross-account image references in a private catalog in Terraform](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#private-catalog-image-reference-vpc-terraform) for more considerations and limitations. To create a private catalog, see the tutorial [Onboarding a virtual server image with Terraform](/docs/account?topic=account-catalog-vsi-tutorial&interface=ui).

### Gathering information to create an instance by using Terraform
{: #gather-info-to-create-virtual-servers-terraform}
{: terraform}

Ready to create an instance? Before you can run the `ibm_is_instance` command, you need to know the details about the instance, such as what profile or image that you want to use.

Gather the following information by using `DataSource` command.

1. Gather instance profile details. Run the following command for the profile that you select. See [x86 instance profiles](/docs/vpc?topic=vpc-profiles&interface=ui#profiles) for a list of available profiles. For more information, see the Terraform documentation on [ibm_is_instance_profiles](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_instance_profiles). Use an instance profile by referring to the instance profile data source. For more information, see the Terraform documentation on [ibm_is_instance_profile](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_instance_profile).

   ```terraform
   data "ibm_is_instance_profile" "example_profile" {
      name = "bx2-2x8"
   }
   ```
   {: codeblock}

1. List the available images for creating your instance. The command depends on what image that you want to use. You can use a stock image, a custom image from your account, or an image that was shared with your account from a private catalog. For more information, see the Terraform documentation on [ibm_is_image](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_image). If you plan to use an image that was shared from a private catalog, see the Terraform documentation on [ibm_cm_version](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_version) or [ibm_cm_offering_instance](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_offering_instance).

   * Select a stock image or custom image from your account for your instance.

   ```terraform
   data "ibm_is_image" "example_image" {
      name = "ibm-centos-7-6-minimal-amd64-2"
   }
   ```
   {: codeblock}

   * Select an image that is shared from a private catalog for the instance. For more information, see the Terraform documentation on [ibm_is_images](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_images). You can select an image from the list to create the instance as shown in the section [Go to Creating an instance by using Terraform section](#create-instance-terraform)

   If you select a catalog image that belongs to a different account, you have more considerations and limitations to review. See [Using cross-account image references in a private catalog in Terraform](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#private-catalog-image-reference-vpc-terraform).
     {: note}

      * To list all available private catalog image offerings, run the following command.

         ```terraform
         data "ibm_is_images" "example_images" {
            catalog_managed = true
          }
         ```
         {: codeblock}

1. Create a VPC resource or use an existing VPC by referring to the VPC data source. For more information, see the Terraform documentation on [ibm_is_vpc](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_vpc).

   ```terraform
   resource "ibm_is_vpc" "example_vpc" {
      name = "example-vpc"
   }
   ```
   {: codeblock}

1. Create a subnet resource or use an existing subnet by referring to the subnet data source. For more information, see the Terraform documentation on [ibm_is_subnet](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_subnet).

   ```terraform
   resource "ibm_is_subnet" "example_subnet" {
      name            = "example-subnet"
      vpc             = ibm_is_vpc.example_vpc.id
      zone            = "us-south-1"
      ipv4_cidr_block = "10.240.0.0/24"
   }
   ```
   {: codeblock}

1. Create a ssh-key resource or use an existing ssh-key by referring to the ssh-key data source. For more information, see the Terraform documentation on [ibm_is_ssh_keys](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_ssh_keys){: external}.

   ```terraform
   resource "ibm_is_ssh_key" "example_sshkey" {
      name       = "example-sshkey"
      type       = "rsa"
      public_key = "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCKVmnMOlHKcZK8tpt3MP1lqOLAcqcJzhsvJcjscgVERRN7/9484SOBJ3HSKxxNG5JN8owAjy5f9yYwcUg+JaUVuytn5Pv3aeYROHGGg+5G346xaq3DAwX6Y5ykr2fvjObgncQBnuU5KHWCECO/4h8uWuwh/kfniXPVjFToc+gnkqA+3RKpAecZhFXwfalQ9mMuYGFxn+fwn8cYEApsJbsEmb0iJwPiZ5hjFC8wREuiTlhPHDgkBLOiycd20op2nXzDbHfCHInquEe/gYxEitALONxm0swBOwJZwlTDOB7C6y2dzlrtxr1L59m7pCkWI4EtTRLvleehBoj3u7jB4usR"
   }
   ```
   {: codeblock}

   SSH keys can either be RSA or Ed25519. You can generate new RSA key pairs using the UI. Pre-existing RSA and Ed25519 SSH keys can be uploaded. Ed25519 can be used only if the operating system supports this key type. Ed25519 can't be used with Windows or VMware images.
   {: note}

1. Create a subnet_reserved_ip resource or use an existing subnet_reserved_ip by referring to the subnet_reserved_ip data source. For more information, see the Terraform documentation on [ibm_is_subnet_reserved_ip](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/is_subnet_reserved_ip)

   ```terraform
   resource "ibm_is_subnet_reserved_ip" "example_reserved_ip" {
      subnet    = ibm_is_subnet.example_subnet.id
      name      = "example-reserved-ip1"
      address   = "${replace(ibm_is_subnet.example_subnet.ipv4_cidr_block, "0/24", "13")}"
   }
   ```
   {: codeblock}

### Creating an instance by using Terraform
{: #create-instance-using-terraform}
{: terraform}

Create the instance by using one of the following examples. For more information, see the Terraform documentation on [ibm_is_instance](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/is_instance).

Run one of the following Terraform commands based on the image that you plan to use.

* Create an instance by using a stock image or custom image from your account for your instance.

   ```terraform
   resource "ibm_is_instance" "example_instance" {
     name    = "example-instance-reserved-ip"
     image   = data.ibm_is_image.example_image.id
     profile = data.ibm_is_instance_profile.example_profile.name

     primary_network_interface {
       name   = "eth0"
       subnet = ibm_is_subnet.example_subnet.id
       primary_ip {
         reserved_ip = ibm_is_subnet_reserved_ip.example_reserved_ip.reserved_ip
       }
     }
     network_interfaces {
       name   = "eth1"
       subnet = ibm_is_subnet.example_subnet.id
       primary_ip {
         name = "example-reserved-ip1"
         auto_delete = true
         address = "${replace(ibm_is_subnet.example_subnet.ipv4_cidr_block, "0/24", "14")}"
       }
     }

     vpc  = ibm_is_vpc.example_vpc.id
     zone = "us-south-1"
     keys = [ibm_is_ssh_key.example_sshkey.id]
   }
   ```
   {: codeblock}

* Create an instance that uses a private catalog-managed image.

   ```terraform
   resource "ibm_is_instance" "example_instance" {
     name    = "example-instance-reserved-ip"
     image   = data.ibm_is_image.example_image.id
     profile = data.ibm_is_instance_profile.example_profile.name

     primary_network_interface {
       name   = "eth0"
       subnet = ibm_is_subnet.example_subnet.id
       primary_ip {
         reserved_ip = ibm_is_subnet_reserved_ip.example_reserved_ip.reserved_ip
       }
     }
     network_interfaces {
       name   = "eth1"
       subnet = ibm_is_subnet.example_subnet.id
       primary_ip {
         name = "example-reserved-ip1"
         auto_delete = true
         address = "${replace(ibm_is_subnet.example_subnet.ipv4_cidr_block, "0/24", "14")}"
       }
     }

     vpc  = ibm_is_vpc.example_vpc.id
     zone = "us-south-1"
     keys = [ibm_is_ssh_key.example_sshkey.id]
   }
   ```
   {: codeblock}
