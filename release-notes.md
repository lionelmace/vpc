---

copyright:
  years: 2019, 2023

lastupdated: "2023-10-12"

keywords:

subcollection: vpc

content-type: release-note

---

{{site.data.keyword.attribute-definition-list}}
{:external: target="_blank" .external}
{:release-note: data-hd-content-type='release-note'}

# Release notes for {{site.data.keyword.vpc_short}}
{: #release-notes}

Use the release notes to learn the latest updates to {{site.data.keyword.vpc_full}} that are grouped by date.
{: shortdesc}

For more information about changes to the {{site.data.keyword.vpc_short}} API, see [{{site.data.keyword.vpc_short}} API change log](/docs/vpc?topic=vpc-api-change-log).

For more information about changes to the {{site.data.keyword.vpc_short}} command line interface (CLI), see [{{site.data.keyword.vpc_short}} CLI release notes](/docs/vpc?topic=vpc-infrastructure-cli-plugin-vpc-cli-rn).

## October 2023
{: #vpc-oct23}


### 12 October 2023
{: #vpc-oct1223}
{: release-note}

VPNs for VPC: Diagnose unhealthy VPN gateways and servers
:   When you see an existing VPN gateway or server in a `degraded` or `faulted` state, you can now diagnose the issue. You are presented with reasons for the state and actions to resolve the issue. For more information, see [Diagnosing VPN gateway health](/docs/vpc?topic=vpc-vpn-health), [Diagnosing VPN gateway connection health](/docs/vpc?topic=vpc-vpn-connection-health), and [Diagnosing VPN server health](/docs/vpc?topic=vpc-vpn-server-health).

Next generation instance profiles available in Dallas region (Select Availability)
:   The 3rd generation of {{site.data.keyword.cloud_notm}} {{site.data.keyword.vsi_is_short}} are available as a Select Availability offering in the Dallas region. This new generation features virtual server profile families that hosted exclusively on 4th Generation Intel&reg; Xeon&reg; Scalable processors to provide the most powerful and performant general-purpose profiles available. For more information, see [Next generation instance profiles](/docs/vpc?topic=vpc-profiles&interface=ui#next-gen-profiles). In the [Balanced](/docs/vpc?topic=vpc-profiles&interface=ui#balanced) family, see the *bx3d* profiles tab. In the [Compute](/docs/vpc?topic=vpc-profiles&interface=ui#compute) family, see the *cx3d* profiles tab. In the [Memory](/docs/vpc?topic=vpc-profiles&interface=ui#memory) family, see the *mx3d* profiles tab. 3rd generation dedicated host profiles are also available. For more information, see *bx3d*, *cx3d*, and *mx3d* profiles in [x86 dedicated host profiles](/docs/vpc?topic=vpc-dh-profiles&interface=ui). 

UI enhancements
:   The following enhancements were made to the VPC UI. 

   * General fixes and updates
   * VPN status reason and suspended status
   * VPN Route Advertisement

### 03 October 2023
{: #vpc-oct0323}
{: release-note}

New regions for ux2d profiles
:   The Ultra High Memory family of profiles are now available in the Brazil (São Paulo), Japan (Tokyo), Japan (Osaka), and Australia (Sydney) regions.


## September 2023
{: #vpc-sep23}

## 29 September 2023
{: #vpc-september2923}
{: release-note}

Backup as a Service Enterprise enablement
:   As an enterprise account administrator, you can view and manage the backup policies and plans for the subaccounts for compliance reporting and billing from one place. Enterprise account users can see all backup policies and associated jobs. They can also see the reference of the backup snapshot that is created in the subaccount. Subaccounts can create and manage their backups as before. For more information, see [About Backup for VPC](/docs/vpc?topic=vpc-backup-service-about).

### 22 September 2023
{: #vpc-sep2223}
{: release-note}

IBM Wazi as a Service available in Spain region
:   {{site.data.keyword.waziaas_full_notm}} (Wazi aaS) is now available in the Spain (Madrid) region in IBM Cloud. For more information, see [{{site.data.keyword.waziaas_full_notm}} product page](https://www.ibm.com/cloud/wazi-as-a-service){: external}.

### 21 September 2023
{: #vpc-sep2123}
{: release-note}

IBM Cloud Hyper Protect Virtual Server for {{site.data.keyword.vpc_full}}
:   You can now create IBM Cloud Hyper Protect Virtual Server for {{site.data.keyword.vpc_short}} instances on LinuxONE (s390x processor architecture) in the Spain (Madrid) region, in addition to Brazil (São Paulo), Canada (Toronto), Japan (Tokyo), and US East (Washington DC) regions. To create IBM Cloud Hyper Protect Virtual Server for {{site.data.keyword.vpc_short}} instances on LinuxONE (s390x processor architecture), see [Creating virtual server instances](/docs/vpc?topic=vpc-creating-virtual-servers), and [IBM Hyper Protect Container Runtime image](/docs/vpc?topic=vpc-vsabout-images#hyper-protect-runtime). A valid contract is required for creating an instance. For more information, see [About the contract](/docs/vpc?topic=vpc-about-contract_se&interface=ui).

LinuxONE (s390x processor architecture)
:   You can now create virtual server instances on LinuxONE (s390x processor architecture) in IBM Cloud in the Spain (Madrid) region, in addition to Japan (Tokyo), Brazil (São Paulo), Canada (Toronto), and United Kingdom (London) regions. For more information about available LinuxONE (s390x processor architecture) profiles, see [s390x instance profiles](/docs/vpc?topic=vpc-vs-profiles). To create instances on LinuxONE (s390x processor architecture), see [Creating virtual server instances by using the UI](/docs/vpc?topic=vpc-creating-virtual-servers).

## 14 September 2023
{: #vpc-september2623}
{: release-note}

UI Enhancements for Backup plans
:   You can now specify both age and count when you define the retention policy of a backup plan.

### 05 September 2023
{: #vpc-sep0523}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-12` updates
:   For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-12`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-12-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-12-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-12-intermediate.crt){: external}

:   You can now roll or rotate the seeds that are used in the contract to improve the security posture, or if the seed is compromised. For more information, see [The workload - volumes subsection](/docs/vpc?topic=vpc-about-contract_se#hpcr_contract_volumes), and [The env - volumes subsection](/docs/vpc?topic=vpc-about-contract_se#hpcr_contract_env_vol).

Ultra High Memory profiles are now available in the United Kingdom region
:   The Ultra High Memory profile family (`ux2d`) is now available in the United Kingdome (London) region. For more information on this profile family, see [Ultra High Memory](/docs/vpc?topic=vpc-profiles&interface=ui#uhmemory).

## August 2023
{: #vpc-aug23}

### 31 August 2023
{: #vpc-august3123}
{: release-note}

Bare metal network hardware
:   Bare metal servers now use upgraded network cards. For network workloads that leverage very high packets per second for smaller packets, you can update your drivers to the latest available Pensando device drivers. For more information, see [Special considerations for bare metal network performance upgrade](/docs/vpc?topic=vpc-bare-metal-image#bare-metal-pensando-considerations) and [AMD Pensando Support](https://www.amd.com/en/support/pensando){: external}.

File Storage for Bare metal servers for VPC
:   File Storage for VPC is now supported by Bare Metal Servers for VPC. Users can leverage file storage as an addition or alternative to local NVMe drives. [About File Storage for VPC](/docs/vpc?topic=vpc-file-storage-vpc-about).

### 25 August 2023
{: #vpc-aug2523}
{: release-note}

Next generation instance profiles (Beta)
:   The 3rd generation of {{site.data.keyword.cloud_notm}} {{site.data.keyword.vsi_is_short}} are available as a Beta offering to select customers. This new generation features virtual server profile families hosted exclusively on 4th Generation Intel&reg; Xeon&reg; Scalable processors to provide the most powerful and performant general-purpose profiles available. For more information, see [Next generation instance profiles](/docs/vpc?topic=vpc-profiles&interface=ui#next-gen-profiles) and the *bx3d* and *mx3d* profiles in the [Balanced](/docs/vpc?topic=vpc-profiles&interface=ui#balanced) and [Memory](/docs/vpc?topic=vpc-profiles&interface=ui#memory) profile families. 

### 22 August 2023
{: #vpc-august2223}
{: release-note}

VPC Status History
:   You can now customize notification settings for your VPC dashboard. When status history is enabled, your notification history is retained to help you find old error messages or track down when the creation or deletion of a resource occurred. To enable Status History, make sure that your browser alllows local storage access. For more information, see [Enabling local storage in your browser](/docs/vpc?topic=vpc-enable-local-browser-storage).

### 15 August 2023
{: #vpc-august1523}
{: release-note}

Metadata Instance identity certificates
:   You can now use the instance identity access token and a Certificate Signing Request (CSR) to [create](/apidocs/vpc-metadata-beta#create-certificate) an instance identity certificate with the Metadata API. For more information, see [Generating an instance identity certificate by using an instance identity access token](/docs/vpc?topic=vpc-imd-configure-service&interface=api#imd-acquire-certificate). Instance identity certificates can be used when the traffic between an authorized client and the mounted file share is [encrypted in transit](/docs/vpc?topic=vpc-file-storage-vpc-eit).

### 08 August 2023
{: #vpc-august0823}
{: release-note}

File Storage for VPC (GA)
:   NFS-based file shares for a zone within a region are now generally available. You can create and share file storage over multiple virtual service instances within the same zone across multiple VPCs. For more information about this service, see [About File Storage for VPC](/docs/vpc?topic=vpc-file-storage-vpc-about).

## July 2023
{: #vpc-jul23}

## 21 July 2023
{: #vpc-july2123}
{: release-note}

VPC services using IBM Cloud Metrics Routing
:  You can use IBM Cloud Metrics Routing to manage metrics at the account-level by configuring targets and routes that define where data points are routed. This platform service can only route metrics that are generated in [supported regions](/docs/metrics-router?topic=metrics-router-regions#regions-metrics-router) by enabled services. Other regions, where IBM Cloud Metrics Routing is not available, continue to manage metrics by using [IBM Cloud Monitoring](/docs/monitoring?topic=monitoring-getting-started).

   For a list of supported IBM Cloud VPC services, see [IBM Cloud services that generate metrics that are managed through IBM Cloud Metrics Routing](/docs/metrics-router?topic=metrics-router-cloud-services-mr#vpc). To learn more about IBM Cloud Metrics Routing, see [Getting started with IBM Cloud Metrics Routing](/docs/metrics-router?topic=metrics-router-getting-started).

### 14 July 2023
{: #vpc-july1423}
{: release-note}

Very High Memory (vx2d) profile family now available in all regions
:   The vx2d profile is now available in the Sao Paolo region. Adding this region makes this profile family available in all regions.

### 11 July 2023
{: #vpc-jul1123}
{: release-note}

Image lifecycle management for custom images (GA)
:   This image lifecycle management feature is now generally available. You can use the UI, CLI, and API to manage the lifecycle of your custom images with the following three statuses. You can move the image back and forth through all the statuses. You can also schedule status changes to manage the entire lifecycle of the image. For more information, see [Custom image lifecycle](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#custom-image-lifecycle) in [Getting started with custom images](/docs/vpc?topic=vpc-planning-custom-images&interface=ui).
    * `available`: The image can be used to create an instance.
    * `deprecated`: The image can be used to create an instance. Using the `deprecated` status can discourage use of the image before the status changes to `obsolete`.
    * `obsolete`: The image can't be used to create an instance.

## June 2023
{: #vpc-jun23}

### 27 June 2023
{: #vpc-jun2723}
{: release-note}

Snapshots for VPC Cross Regional Copy (GA)
:   Customers can now create a copy of a snapshot in a different region, and later use that copy to restore a volume in the new region. This feature can be beneficial in disaster recovery scenarios when the customer needs to start their virtual server instance and data volumes in a different region. Customers can also use the remote copy to create storage volumes in a new region and expand their VPC in new locations. For more information, see [Cross Regional Snapshot copies](/docs/vpc?topic=vpc-snapshots-vpc-about#snapshots_vpc_crossregion_copy).

Backup for VPC Cross Regional Copy (GA)
:   Customers can now save a copy of their backup in a different region. Customers can copy the backup snapshot to another region manually or add the copy option to their backup policy plans. Customers can manage and use the cross-regional copy in the target region independently from the parent volume or the original backup. For more information, see [Cross Regional backup copies](/docs/vpc?topic=vpc-backup-service-about&interface=ui#backup-service-crc).

### 22 June 2023
{: #vpc-jun2223}
{: release-note}

New Ed25519 SSH key type is available (GA)
:   The Ed25519 SSH key type is a new, supported SSH key type and can be used as an alternative to the RSA SSH key type. The Ed25519 SSH key can be used with Linux operating systems, but is not supported for Windows or VMware images. For more information, see [Getting started with SSH keys](/docs/vpc?topic=vpc-ssh-keys) and [Managing SSH Keys](https://cloud.ibm.com/docs/vpc?topic=vpc-managing-ssh-keys).

Madrid multi zone region (MZR)
:   A new MZR is available for VPC and Classic infrastructures. Classic Virtual Servers will not be available in the Madrid MZR. The Madrid region supports only dedicated host profiles with instance storage. For more information, see [Region and data center locations for resource deployment](/docs/overview?topic=overview-locations), [Setting up access to classic infrastructure](/docs/vpc?topic=vpc-setting-up-access-to-classic-infrastructure&interface=ui), and [Dedicated host profiles](/docs/vpc?topic=vpc-dh-profiles&interface=ui).

### 20 June 2023
{: #vpc-june2023}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-11` updates
:  For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-11`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-11-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-11-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-11-intermediate.crt){: external}

   Support for customer-managed keys through integration with Hyper Protect Crypto Services
   - **Without** the feature, the data volume that you attach to your instance is encrypted automatically with a LUKS passphrase generated by using the **two** seeds from the `workload` - `volumes` and `env` - `volumes` sections of the contract. **Starting from the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-11`**, Hyper Protect Virtual Servers support integration with the key management service (KMS) Hyper Protect Crypto Services. You can enable the integration by providing KMS configurations in the contract. Your Hyper Protect Virtual Server instance calls Hyper Protect Crypto Services to generate a random value as the third seed and wrap it with your root key. The wrapped seed is stored in the metadata partition of your data volume. The LUKS passphrase is generated by using **three** seeds - the seed in the metadata partition (unwrapped first) and the two seeds from the contract. For more information about how the integration works and detailed instructions, see [Securing your data](/docs/vpc?topic=vpc-hyper-protect-virtual-server-mng-data).

   Deploying multiple containers
   - In the `workload` section of the contract, you can define the workload via Pod descriptors. Each pod can contain one or more container definitions. Previously, only one container described by docker compose was supported. For more information about using Pod descriptors, see the [`play` subsection](/docs/vpc?topic=vpc-about-contract_se#hpcr_contract_play). Container images described by Pod descriptors can be [validated by RedHat Simple Signing](/docs/vpc?topic=vpc-about-contract_se#container-image-by-pod-descriptors). 
   
   Changes to the attestation document
   - In the attestation document **se-checksums.txt**, `user-data.decrypted` is removed, and `Machine Type/Plant/Serial` (the information required to identify the host machine) is added. For more information, see [Attestation](/docs/vpc?topic=vpc-about-attestation).

Virtual network interface (beta)
:  Virtual network interfaces are now available in a beta release for use with file share mount targets. For more information see [About virtual network interfaces](/docs/vpc?topic=vpc-vni-about).

Instance group integration with network load balancers
:    IBM Cloud Network Load Balancer (NLB) for VPC now integrates with instance groups to improve pool member scaling. When you create or update an instance group for auto scaling, you can specify an NLB pool for the instance group to manage. Attaching an instance group to a load balancer allows your pool back-end members to automatically scale up or down depending upon your usage and requirements. For more information see [Integrating an IBM Cloud Network Load Balancer for VPC with instance groups](/docs/vpc?topic=vpc-nlb-integration-with-instance-groups).

Access control modes and granular authorization for File Storage for VPC file shares (beta)
:   For users with accounts that have access to file shares, you can now specify an access control mode to either restrict mounting a file share to a specific virtual server instance in the VPC or allow VPC-wide file share mounting. File share mount targets that were created before `20-June-2023` have a default of VPC-wide file share mounting. File shares that are created after that date can specify security group access control mode to restrict access to a specific instance. For this option, file shares must be based on the [`dp2` profile](/docs/vpc?topic=vpc-file-storage-profiles&interface=ui#dp2-profile). From the UI, CLI, or API, you set the access control mode when you create or update file shares, and can see the setting when you list file shares and in the file share details. When you create a mount target for a file share with security group access mode, you can specify a [virtual network interface](/docs/vpc?topic=vpc-vni-about) to be created and attached to the mount target with a [security group](/docs/vpc?topic=vpc-using-security-groups). For the virtual network interface, you can specify an existing reserved IP, or specify a subnet and allow the system to assign an IP address. When the mount target is attached and the share is mounted, the virtual network interface performs security group policy check to ensure only authorized virtual server instances can communicate with the share. For more information, see [Mount targets for file shares](/docs/vpc?topic=vpc-file-storage-vpc-about#fs-share-mount-targets).

Data encryption in transit for file shares (beta)
:    For users with accounts that have access to file shares, you can enable secure end-to-end encryption of your data when using security group based access control on file shares and mount targets with virtual network interfaces. The traffic between the authorized virtual server and the file share can optionally be IPsec encapsulated by the client. By using an Internet Security Protocol (IPsec), you can establish an encrypted mount connection between the virtual server instance and a file share with the `dp2` profile. The {{site.data.keyword.cloud}} file service provides a [mount helper utility](/docs/vpc?topic=vpc-file-storage-vpc-eit#fs-mount-helper-utility) to automate the complex tasks of configuring and maintaining the connection. For more information, see [Encryption in transit - Securing mount connections between file share and host](/docs/vpc?topic=vpc-file-storage-vpc-eit).

### 16 June 2023
{: #vpc-jun1623}
{: release-note}

VPC routing table authorizations
:   You can use the new VPC routing table authorizations to allow users to administer VPC routing tables but not allow them to administer the broader VPC. Routing table operations were updated to check for these new authorizations, instead of the broader VPC authorizations. The VPC Administrator, Editor, Operator, and Viewer IAM access roles were updated so that users with those roles function as before. However, custom roles that require access to routing tables must be updated. For more information, see [IAM actions for VPC routing tables](/docs/vpc?topic=vpc-iam-actions-vpc-routing-tables).

### 15 June 2023
{: #vpc-jun1523}
{: release-note}

New regions available for Ultra High Memory profiles:
:   Ultra High Memory (ux2d) profiles are now available in the US East (Washington DC), Canada (Toronto), and EU Germany (Frankfurt) regions. For more information, see the [Ultra High Memory](/docs/vpc?topic=vpc-profiles&interface=ui#uhmemory) profiles documentation.

### 08 June 2023
{: #vpc-jun0823}
{: release-note}

New stock images for bare metal servers
:    The following stock images are now available for bare metal servers:
    * CentOS 7.x is now supported as an image when you provision a bare metal server.
    * CentOS Stream 9.x is now supported as an image when you provision a bare metal server.
      For more information, see [Bare metal server images](/docs/vpc?topic=vpc-bare-metal-image).

### 01 June 2023
{: #vpc-jun0123}
{: release-note}

UI Enhancement to the List view
:    You can now export table data with the current table column format. The supported export formats are CSV and Microsoft Excel.

## May 2023
{: #vpc-may23}

### 30 May 2023
{: #vpc-may3023}
{: release-note}

{{site.data.keyword.filestorage_vpc_short}} file share activity tracker event name changes (beta)
:    For users with accounts that have access to file shares, when you make API requests by using a `version` query parameter of `2023-05-30` or later, the shares `targets` property was changed to `mount_targets`. This change affects file share Activity Tracker events. Events generated when [creating](/apidocs/vpc-beta#create-share-mount-target), [listing](/apidocs/vpc-beta#list-share-mount-targets), [retrieving](/apidocs/vpc-beta#get-share-mount-target), [deleting](/apidocs/vpc-beta#delete-share-mount-target), and [updating](/apidocs/vpc-beta#update-share-mount-target) mount targets for a file share are now `is.share.mount-target.create`, `is.share.mount-target.list`,`is.share.mount-target.read`, `is.share.mount-target.delete`, and `is.share.mount-target.update`. Events for `is.share.target.create`, `is.share.target.list`, `is.share.target.read`, `is.share.target.delete`, and `is.share.target.update` are deprecated and will be removed in a future API release per the VPC beta API [versioning policy](/apidocs/vpc-beta#api-versioning-beta).

### 19 May 2023
{: #vpc-may1923}
{: release-note}

Removal of weak VPN for VPC ciphers
:   Effective 18 May 2023, the following VPN IKE and IPsec ciphers are now removed:
    * Authentication algorithms `md5` and `sha1`
    * Encryption algorithm `triple_des`
    * Diffie–Hellman groups `2` and `5`

   After this date, you cannot create an IKE/IPsec policy or connection that includes a weak cipher, but you can still [upgrade weak cipher suites](/docs/vpc?topic=vpc-upgrading-weak-ciphers&interface=ui) on an existing policy or connection. Starting 10 July 2023, any existing connections with customized IKE or IPsec policies that contain weak ciphers will be disabled, and any connections with auto IKE or IPsec policies that were created before September 20, 2022 will be forced to upgrade to the [enhanced auto-negotiation policy](/docs/vpc?topic=vpc-using-vpn#policy-negotiation).

### 11 May 2023
{: #vpc-may1123}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-10`
:  For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-10`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-10-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-10-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-10-intermediate.crt){: external}

### 9 May 2023
{: #vpc-may0923}
{: release-note}

New `-a100` GPU profile is available (LA)
:   A new profile is available for customers with special approval to preview this service that is for provisioning instances based on NVIDIA's A100 Amperere GPU attached to a single virtual server instance. The `gx2-80x1280x8a100` profile supports artificial intelligence and machine language frameworks and includes instance storage. Only Red Hat and Ubuntu are supported for this profile. This profile is only available in the Washington DC region. For more information, see [GPU profiles](https://test.cloud.ibm.com/docs/vpc?topic=vpc-profiles&interface=ui#gpu). To request access to this profile, you must open a [support case](https://cloud.ibm.com/unifiedsupport/supportcenter).

## April 2023
{: #vpc-apr23}

## 27 April 2023
{: #vpc-apr2723}
{: release-note}

Documentation enhancement: Deploying an application for financial transactions with Confidential Computing on Hyper Protect Virtual Server for VPC
:   The newly added [**Deploying an application on Hyper Protect Virtual Server for VPC** tutorial](/docs/vpc?topic=vpc-financial-transaction-confidential-computing-on-hyper-protect-virtual-server-for-vpc) walks you through how to deploy the PayNow application with Confidential Computing on Hyper Protect Virtual Server for VPC.

UI update to enable deletion of nested resources
:    When you delete a resource, such as a VPC or a subnet, any attached resources must be deleted first before you can delete the VPC. The UI is updated to display a side panel listing all the resources that are still attached to the VPC that must be deleted. You can delete these resources from this side panel and then continue with deleting the VPC.

Export custom images (GA)
:   The ability to export custom images to {{site.data.keyword.cos_full_notm}}, a feature previously available in beta, is now generally available. For more information, see [Exporting a custom image to IBM Cloud Object Storage](/docs/vpc?topic=vpc-managing-custom-images&interface=ui#custom-image-export-to-cos).

### 6 April 2023
{: #vpc-apr0623}
{: release-note}

Image lifecycle management for custom images (beta)
:   For customers with special access to this feature, you can use the UI, CLI, and API to manage the lifecycle of your custom images with the following three statuses. You can move the image back and forth through all the statuses. You can also schedule status changes to manage the entire lifecycle of the image. For more information, see [Custom image lifecycle](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#custom-image-lifecycle) in [Getting started with custom images](/docs/vpc?topic=vpc-planning-custom-images&interface=ui).
    * `available`: The image can be used to create an instance.
    * `deprecated`: The image can be used to create an instance. Using the `deprecated` status can discourage use of the image before the status changes to `obsolete`.
    * `obsolete`: The image can't be used to create an instance.

### 4 April 2023
{: #vpc-apr0423}
{: release-note}

{{site.data.keyword.filestorage_vpc_short}} high-performance profile (beta)
:    For customers with special access to this feature, you can now create file shares by using the **dp2** high-performance profile. This profile provides higher IOPS and greater capacity than earlier profiles. You can also modify existing file shares to use this profile. For more information, see the [file share profiles overview](/docs/vpc?topic=vpc-file-storage-profiles&interface=ui#file-storage-profile-overview).

## March 2023
{: #vpc-mar23}

### 31 March 2023
{: #vpc-mar3123}
{: release-note}

New network latency dashboard to view latency between zones in a multi-zone region (MZR)
:   Not only can you view inter-region latency metrics, but you can now view inter-AZ metrics between all regions and availability zones (AZs) to help you plan the optimal selection for your cloud deployment. To view performance metrics, see the [Network latency dashboards](/docs/vpc?topic=vpc-network-latency-dashboard).

## 30 March 2023
{: #vpc-mar3023}
{: release-note}

Documentation enhancement: Encrypting log messages for {{site.data.keyword.hpvs}} for VPC
:   The newly added [**Encrypting log messages** tutorial](/docs/vpc?topic=vpc-encrypt-log-messages-for-hyper-protect-virtual-servers-for-vpc) walks you through how to encrypt log messages that are generated by your container workload in your Hyper Protect Virtual Server for VPC instance. You can use the tutorial as reference to encrypt log messages if your workload produces sensitive information.

### 29 March 2023
{: #vpc-mar2923}
{: release-note}

VCPU manufacturer support for instances and dedicated hosts (LA)
:   For accounts authorized to preview this functionality, you can now choose between profiles from different processor manufacturers when you provision an instance or dedicated host in the TOR region. For more information, see [x86-64 instance profiles](/docs/vpc?topic=vpc-profiles&interface=ui#balanced), [Dedicated host profiles](/docs/vpc?topic=vpc-dh-profiles&interface=ui#balanced-dh-pr).

### 28 March 2023
{: #vpc-mar2823}
{: release-note}

Private DNS zones for network load balancers
:    You can now use IBM Cloud Application and Network Load Balancers for VPC to bind DNS zones from [IBM Cloud DNS Services](/docs/dns-svcs?topic=dns-svcs-getting-started), so you can move all DNS resolutions into private networks. Private DNS zones are resolvable only on IBM Cloud, and only from explicitly permitted networks in an account or with cross account access. For more information, see [Integrating a load balancer with IBM Cloud DNS Services](/docs/vpc?topic=vpc-lb-dns).

Enhancements to viewing profiles - number of supported network interfaces
:   In {{site.data.keyword.cloud_notm}} console, when you click **View all profiles** on the **Create virtual server instance** page, the **Bandwidth** column values include a tooltip. The tooltip now includes the number of network interfaces that can be attached for the profile. A similar feature is now available in the API when you list instance profiles. For more information, see [Network interface configuration for instance profiles](/docs/vpc?topic=vpc-api-change-log&interface=cli#28-march-2023-all-version-dates).

### 23 March 2023
{: #vpc-mar2323}
{: release-note}

New network latency dashboard
:   Provides visibility into network latency between all regions to help you plan the optimal selection for your cloud deployment and plan for scenarios, such as data residency and performance. This dashboard provides the average network round-trip latency (round-trip time or RTT) for all pairs of regions in {{site.data.keyword.cloud_notm}} over a 30-day period.

   You can view and monitor performance in the following {{site.data.keyword.cloud_notm}} regions: Dallas, Toronto, Washington DC, Frankfurt, London, Osaka, Sydney, Tokyo, and São Paulo.

   To view performance metrics, see the [Network latency dashboard](/docs/vpc?topic=vpc-network-latency-dashboard).

### 21 March 2023
{: #vpc-mar2123}
{: release-note}

Instance provision by volume
:   You can now reuse an existing boot volume to provision a virtual server instance. The specified volume must be unattached, be in the same zone as the instance profile, and must have an operating system with the same architecture as the instance profile. By default, a boot volume that is created as part of provisioning a virtual server instance is deleted when the instance is deleted. You can control this behavior when you create or updating an instance. For more information, see [Creating virtual server instances](/docs/vpc?topic=vpc-creating-virtual-servers&interface=ui), and [Managing virtual server instances](/docs/vpc?topic=vpc-managing-virtual-server-instances&interface=ui).

Designating VPC route priority
:   When multiple VPC routes exist for a destination, you can now control the priority of these routes (from `0` to `4`). New and existing routes that are created without a priority value, are automatically set to the default priority (`2`). Smaller values have higher priority. For more information, see [Determining route preference](/docs/vpc?topic=vpc-about-custom-routes#cr-determining-route-preference).

   The route priority is considered on identical destinations only.
   {: note}

Modifying the next hop for VPC routes
:   You can now [update](/apidocs/vpc/latest#update-vpc-routing-table-route) the next-hop of a VPC route. For more information, see [Creating a route](/docs/vpc?topic=vpc-create-vpc-route).


### 20 March 2023
{: #vpc-mar2023}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-9` updates
:  For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-9`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-9-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-9-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-9-intermediate.crt){: external}

   Two partitions in new data volume
   - For new {{site.data.keyword.hpvs}} instances, the data volume is partitioned into two parts. The first partition (100Mib) is reserved for internal metadata; the second partition remains as the data volume for workload. Only new volumes are partitioned, and you can't use the partitioned volume with an older version of the HPCR image. Provisioning with an existing encrypted volume also works. The difference is that the existing volume does not get partitioned, and you can also go back to an older image with this volume.

   Support for using a dynamic registry reference
   - There exist use cases in which the registry is **not known** when the workload section is pre-encrypted, for example, when the workload provider wants to allow the deployer to use a registry mirror or a private container registry. In such a case, it's possible to dynamically override the registry and the pull credentials - which is coordinated between the workload provider and the deployer. For more information, see [Using a dynamic registry reference](/docs/vpc?topic=vpc-hyper-protect-virtual-server-use-dynamic-registry-reference).

### 16 March 2023
{: #vpc-mar1623}
{: release-note}

Client-to-site VPN server private certificate support
:    VPN servers now support the use of Secrets Manager private certificates. Private certificates are SSL/TLS certificates that you can sign, issue, and manage in the Secrets Manager service. For VPN server considerations, see [Using a private certificate](/docs/vpc?topic=vpc-client-to-site-authentication#using-private-certificate). For Secrets Manager information, see [Creating a private certificate](/docs/secrets-manager?topic=secrets-manager-certificates&interface=ui#create-certificates).

### 10 March 2023
{: #vpc-mar1023}
{: release-note}

Client-server timeout for application load balancers
:    You can now configure the client and server timeout parameters for IBM Cloud Application Load Balancer for VPC by using the UI, CLI, and API. The maximum timeout period for each listener is 2 hours, and the minimum is 50 seconds. If you need a timeout amount greater than 2 hours, open a [support case](/docs/vpc?topic=vpc-getting-help) with IBM Support. For more information about setting the client and server timeout period, see [Creating an application load balancer](/docs/vpc?topic=vpc-load-balancers&interface=ui). This functionality is only available for application load balancers.

## February 2023
{: #vpc-feb23}

### 14 February 2023
{: #vpc-feb1423}
{: release-note}

VPC instance metadata communication protocol and hop limit
:    You can now control the communication protocol and hop limit for IP response packets that are used by the [VPC Instance Metadata service](/docs/vpc?topic=vpc-imd-about). When you provision or update an instance, use the new **Secure access** setting to specify either `http` (default) or `https` (secure access) communication. In addition, use the new **Hop limit** setting to specify a value between `1` (default) and `64`. Both of these settings apply only when the metadata service is enabled. For more information, see [Configure metadata settings by using the UI](/docs/vpc?topic=vpc-imd-configure-service&interface=ui#metadata-config-ui).

Hyper Protect Secure Build
:    You can now use [Hyper Protect Secure Build](/docs/vpc?topic=vpc-about-hpsb) to securely build an Open Container Initiative (OCI) image in [Hyper Protect Virtual Servers for VPC](/docs/vpc?topic=vpc-about-se). You can push the image to DockerHub or IBM Cloud Container Registry (ICR). Later, you can pull the image from the registry to provision it in another {{site.data.keyword.hpvs}} for VPC instance. You can also pull SLES BaseContainerImages (BCI) from the SUSE registry, and use the images to provision {{site.data.keyword.hpvs}} for VPC instances.

### 9 February 2023
{: #vpc-feb0923}
{: release-note}

Export custom images (Beta)
:   For accounts that are authorized to preview this feature, you can now export custom images to {{site.data.keyword.cos_full_notm}}. For more information, see [Exporting a custom image to IBM Cloud Object Storage (Beta)](/docs/vpc?topic=vpc-managing-custom-images&interface=ui#custom-image-export-to-cos).

### 7 February 2023
{: #vpc-feb0723}
{: release-note}

Block Storage fast restore snapshots
:    You can now restore a fully provisioned volume with all its data from a snapshot by using a fast restore snapshot clone. You can use fast restor to restore a volume more quickly than restoring from a regular snapshot. To create the clone, you specify a zone or zones in the same region as the source snapshot. The clone is used to automatically restore a volume with all of its data in the zone where the clone exists. For more information, see [Restoring a volume by using fast restore](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=api#snapshots-vpc-use-fast-restore).

Extra security for VPC snapshots (closed beta)
:    For customers with special access to this security beta feature, data isolation is provided to store snapshots created from your dedicated hosts. With data isolation extra security, your data is encrypted at rest with a unique key and access to your data is protected by a private firewall.

### 3 February 2023
{: #vpc-feb0323}
{: release-note}

Images for VPC UI Updates
:    Previously, the path to custom images was **VPC Infrastructure > Compute > Custom Images**. The new path is **VPC Infrastructure > Compute > Images**. The new page is **Images for VPC** and now has a tab for each type of image:
    - Custom images
    - Stock images
    - Catalog images

## January 2023
{: #vpc-jan23}

### 31 January 2023
{: #vpc-jan3123}
{: release-note}

Secure boot with Trusted Plaform Module (TPM) (LA)
:   Secure boot makes sure that your server starts with trusted software by verifying the signatures for all code in the boot process. Trusted Platform Module (TPM) provides hardware-based security functions. With supporting software, TPM helps maintain platform integrity and generates cryptographic keys. For more information, see [Secure boot with Trusted Platform Module (TPM)](/docs/vpc?topic=vpc-secure-boot-tpm).

### 30 January 2023
{: #vpc-jan3023}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-8` updates
:  For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-8`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-8-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-8-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-8-intermediate.crt){: external}

   Using {{site.data.keyword.hpvs}} for VPC in a private network
   - You can use your {{site.data.keyword.hpvs}} for VPC instance in **private-only** network configurations, in which the VPC doesn't have a public gateway, and the virtual server instance doesn't have a floating IP. You can connect to private endpoints of other services, including container registry and [IBM Log Analysis](/docs/vpc?topic=vpc-logging-for-hyper-protect-virtual-servers-for-vpc). The prerequisite is that you need a DNS server that is attached to your virtual server instance. You don't need to do any extra configurations.

   Security enhancement to disk encryption verification
   - To address Denial-of-Service attacks, the requests to [verify disk encryption status](/docs/vpc?topic=vpc-hpvs-disks-encryption-validate) are throttled at three per five minutes.

### 27 January 2023
{: #vpc-jan2723}
{: release-note}

Context-based restrictions
:   Context-based restrictions are now available for {{site.data.keyword.vpc_short}} resources. With context-based restrictions, account owners and administrators can define and enforce network access policies. For more information, see [Protecting Virtual Private Cloud (VPC) Infrastructure Services with context-based restrictions](/docs/vpc?topic=vpc-cbr).

### 17 January 2023
{: #vpc-jan1723}
{: release-note}

Application Load Balancer and VPN for VPC
:    As a reminder, end of support for IBM Cloud Certificate Manager was 31 December 2022. Remaining instances of Certificate Manager were deleted. If any user-provided Ingress secrets are stored in Certificate Manager, they are no longer valid.

End of support (EOS) for deprecated VPN for VPC IKE and IPsec ciphers
:    On 20 September 2022, the following VPN IKE and IPsec ciphers were deprecated:
   - Authentication algorithms `md5` and `sha1`
   - Encryption algorithm `triple_des`
   - Diffie–Hellman groups `2` and `5`

   Effective today, these ciphers are no longer supported in the UI and EOS for use with the CLI and API is forthcoming. If you didn't upgrade to more secure ciphers, do so now. For more information, see [Upgrading weak cipher suites on a VPN gateway](/docs/vpc?topic=vpc-upgrading-weak-ciphers).

## December 2022
{: #vpc-dec22}

### 20 December 2022
{: #vpc-dec2022}
{: release-note}

Instance provision by volume (Beta)
:   By default, when a virtual server instance is deleted attached boot volumes are deleted.
You can disable this behavior, causing the boot volume to instead be detached when the virtual server instance is deleted. You can then attach the boot volume to a new virtual server instance.
For more information, see [Creating virtual server instances](/docs/vpc?topic=vpc-creating-virtual-servers&interface=ui), [Creating VPC resources with CLI and API](/docs/vpc?topic=vpc-creating-vpc-resources-with-cli-and-api&interface=cli), and [Managing virtual server instances](/docs/vpc?topic=vpc-managing-virtual-server-instances&interface=ui).

Backup for VPC
:   The backup policy jobs feature, previously released as a Beta, is now generally available. You can now view all backup policy jobs or details of a single job from the UI, CLI, or API.  A backup policy job is triggered when a scheduled backup snapshot is being created or deleted. If the create or delete action is successful, the job contains information about the backup snapshot that was created or deleted. If the job ran unsuccessfully, the job contains the reason for the failure. For more information, see [Viewing backup jobs](/docs/vpc?topic=vpc-backup-view-policy-jobs).

### 17 December 2022
{: #vpc-dec1722}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-7` updates
:  For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-7`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-7-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-7-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-7-intermediate.crt){: external}

   Certificate revocation list
   - Starting from `ibm-hyper-protect-container-runtime-1-0-s390x-7-encrypt.crt` and `ibm-hyper-protect-container-runtime-1-0-s390x-7-attestation.crt`, the certificates contain **Certificate Revocation List (CRL) Distribution Points**. You can use the CRL to verify that your certificates are valid (not revoked). For more information, see [Certificate revocation list](/docs/vpc?topic=vpc-cert_validate#certificate-revocation-list).

### 15 December 2022
{: #vpc-dec1522}
{: release-note}

Bare metal servers now support custom images
:   You can now create custom images to use on your bare metal servers. For more information, see [Custom image considerations](/docs/vpc?topic=vpc-bare-metal-image&interface=ui#bare-metal-custom-images-requirements) and [Bare metal server considerations](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#bare-metal-server-custom-images-considerations).

### 13 December 2022
{: #vpc-dec1322}
{: release-note}

Volume creation from a Block Storage snapshot
:   You can now use the UI and CLI, in addition to the VPC API, to create a stand-alone Block Storage volume from a snapshot. Stand-alone data volumes can be attached to a virtual server instance at any time. You can select a snapshot of a boot volume and use it to boot a new virtual server instance. For more information, see
[Restore a stand-alone data volume from a snapshot](/docs/vpc?topic=vpc-snapshots-vpc-restore).

Block Storage volume health states
:   You can now view the health state of a Block Storage volume from the UI, CLI, and API. Health indicated whether a volume is performing as expected or degraded. You can view health status and reasons from the list of volumes and volume details, and when you create and update volumes. For more information, see [Block Storage volume health states](/docs/vpc?topic=vpc-managing-block-storage#block-storage-vpc-health-states).

## November 2022
{: #vpc-nov22}

### 14 November 2022
{: #vpc-nov1422}
{: release-note}

IBM Hyper Protect Container Runtime image `ibm-hyper-protect-container-runtime-1-0-s390x-6` updates
:  For the IBM Hyper Protect Container Runtime image version `ibm-hyper-protect-container-runtime-1-0-s390x-6`, new certificates are available.
   - [Attestation certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-6-attestation.crt){: external}
   - [Encryption certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-6-encrypt.crt){: external}
   - [Intermediate certificate](/media/docs/downloads/hyper-protect-container-runtime/ibm-hyper-protect-container-runtime-1-0-s390x-6-intermediate.crt){: external}

   Logging for {{site.data.keyword.hpvs}} for VPC
   - Apart from IBM Log Analysis, you can now configure logging with a generic syslog backend. For more information, see [Logging for {{site.data.keyword.hpvs}} for VPC](/docs/vpc?topic=vpc-logging-for-hyper-protect-virtual-servers-for-vpc#syslog).

   Security claims on disks encryption
   - Both the root disk and data disks in the {{site.data.keyword.hpvs}} for VPC instance are configured with Linux Unified Key Setup (LUKS) Encryption. You can verify the encryption status by checking related messages in the log. For more information, see [Verifying disk encryption status](/docs/vpc?hpvs-disks-encryption-validate).

### 11 November 2022
{: #vpc-nov1122}
{: release-note}

Access management tags to manage VPC resources
:   You can now use access management tags to control access to VPC resources, such as virtual server instances and Block Storage volumes. See the [Access management tags](/docs/vpc?topic=vpc-iam-getting-started&interface=ui#iam-access-management-tags) section in [Managing IAM access for VPC Infrastructure Services](/docs/vpc?topic=vpc-iam-getting-started). For more information about using access management tags, see the following IAM resources:
    * [Controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial) UI tutorial
    * [Working with tags](/docs/account?topic=account-tag&interface=ui)
    * [Granting users access to tag resources and service IDs](/docs/account?topic=account-access&interface=ui)

### 8 November 2022
{: #vpc-nov0822}
{: release-note}

Backup policy jobs
:    You can now list all jobs for a backup policy and retrieve backup policy job details from the UI, CLI, or API. Backup policy job information includes the backup plan that is used to create the backup snapshot, the backup job type, job status, source volume, target snapshot, and additional information. For more information, see [Viewing backup jobs](/docs/vpc?topic=vpc-backup-view-policy-jobs).

## October 2022
{: #vpc-oct22}

### 31 October 2022
{: #vpc-oct3122}
{: release-note}

Terraform is now available for sharing images across an enterprise account
:    You can now share or publish custom images by using Terraform to other accounts within your enterprise by using a private catalog. If you select a catalog image that belongs to a different account, review [Using cross-account image references in a private catalog in Terraform](/docs/vpc?topic=vpc-planning-custom-images&interface=terraform#private-catalog-image-reference-vpc-terraform) for extra considerations and limitations. To create a private catalog, see the tutorial [Onboarding a virtual server image with Terraform](/docs/account?topic=account-catalog-vsi-tutorial&interface=ui). To create an instance from a catalog image by using Terraform, see [Creating virtual server instances by using Terraform](/docs/vpc?topic=vpc-creating-virtual-servers&interface=terraform#create-instance-terraform).

### 21 October 2022
{: #vpc-oct2122}
{: release-note}

Context-based restrictions (limited availability)
:   For accounts authorized to preview this functionality, account owners and administrators can now define and enforce network access policies for IBM Cloud VPC resources. For more information about specific VPC Infrastructure services that are supported for context-based restrictions, see [Protecting Virtual Private Cloud (VPC) Infrastructure Services with context-based restrictions (limited availability)](/docs/vpc?topic=vpc-cbr).

### 19 October 2022
{: #vpc-oct1922}
{: release-note}

Windows BYOL for multi-tenant hosts
:   You can now bring your own license for Windows operating systems with a custom image to provision virtual server instances on multi-tenant hosts. Previously Windows BYOL was limited to dedicated hosts. For more information, see [Bring your Own License](/docs/vpc?topic=vpc-byol-vpc-about) and [Getting started with custom images](/docs/vpc?topic=vpc-planning-custom-images).

## 3 October 2022
{: #vpc-oct0322}

VPC Public Ingress Routing
:   You can now route public internet ingress traffic (destined to a floating IP) to a VPC next-hop IP. For more information, see [Creating a routing table](/docs/vpc?topic=vpc-create-vpc-routing-table) and limitations and guidelines for [Ingress routes](/docs/vpc?topic=vpc-about-custom-routes&interface=ui#routes-ingress).

   Currently, public ingress routing (`public internet` traffic choice) is available in the UI and API only. CLI is forthcoming.
   {: note}

Flow Logs for VPC
:   Flow log collectors now support the following cross-account service virtual interfaces at VPC and subnet levels:

   - IBM Cloud Kubernetes Service (IKS) workers
   - Red Hat OpenShift Kubernetes Service (ROKS)
   - Load Balancer as a Service (LBaaS)

   For more information, see [About IBM Cloud Flow Logs for VPC](/docs/vpc?topic=vpc-flow-logs).

## September 2022
{: #vpc-september22}


### 23 September 2022
{: #vpc-september2322}

IBM Wazi as a Service
:   {{site.data.keyword.waziaas_full_notm}} (Wazi aaS) is now generally available in IBM Cloud in Japan (Tokyo), Brazil (São Paulo), Canada (Toronto), United Kingdom (London), and US East (Washington DC) regions. For more information, see [{{site.data.keyword.waziaas_full_notm}} product page](https://www.ibm.com/cloud/wazi-as-a-service){: external}.
* For the latest updates of z/OS dev and test stock images, see [Change log for z/OS stock images](https://www.ibm.com/docs/en/wazi-aas/1.0.0?topic=vpc-change-log-zos-stock-images){: external}.
* For instructions on creating z/OS virtual server instances, see [Creating virtual server instances](/docs/vpc?topic=vpc-creating-virtual-servers).


Network interfaces for virtual servers
:   You can now add up to 15 network interfaces to virtual server instances. The number of interfaces that a virtual server supports depends on the vCPU count that is in the [instance profile](/docs/vpc?topic=vpc-profiles). Profiles that include 17 - 48 vCPUs now support up to 10 network interfaces. Profiles that include 49 or more vCPUs now support up to 15 network interfaces. For existing virtual servers with 17 or more vCPUs to take advantage of the new network interface limits, a running virtual server instance must be stopped and restarted. For more information about multiple network interfaces, see [Managing network interfaces](/docs/vpc?topic=vpc-using-instance-vnics).

### 22 September 2022
{: #vpc-september2222}
{: release-note}

Sharing images across an enterprise account
:    You can now share or publish custom images to other accounts within your enterprise by using a private catalog. A private catalog provides a way for you to manage access to products for multiple accounts. You can use any existing x86 virtual server custom image with a private catalog, except for an encrypted image. For more information, see [Custom images in a private catalog](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#custom-image-cloud-private-catalog) and the tutorial [Onboarding a virtual server image for VPC](/docs/account?topic=account-catalog-vsivpc-tutorial). Custom images can't be deleted if they are managed from a catalog and can be managed from only one catalog product offering version at a time. Deleting the catalog does not free its managed resources for a 7-day reclamation period. For more information, see [Deleting a custom image in a private catalog](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#deleting-private-catalog-custom-image-vpc) and [Using resource reclamations](/docs/account?topic=account-resource-reclamation). If you plan to share images with other accounts, users in those accounts must be aware of considerations that are related to cross-account references to those images. For more information, see [Using cross-account image references in a private catalog](/docs/vpc?topic=vpc-planning-custom-images&interface=ui#private-catalog-image-reference-vpc-ui). Custom images can also be published to the IBM Cloud catalog and to other (nonenterprise) accounts. This process requires onboarding to the [IBM Cloud Partner Center](https://cloud.ibm.com/partner-center/sell).

Deprecated VPN for VPC ciphers
:    The following VPN for VPC IKE and IPsec ciphers are now deprecated:
   - Authentication algorithms `md5` and `sha1`
   - Encryption algorithm `triple_des`
   - Diffie–Hellman groups `2` and `5`

   You have until 13 December 2022 to upgrade to more secure ciphers. After this date, VPN connections that use deprecated ciphers show a `status` of `down` (and no longer transfer data) until you upgrade from the weak cipher. For more information, see [Upgrading weak cipher suites on a VPN gateway](/docs/vpc?topic=vpc-upgrading-weak-ciphers).

More VPN for VPC ciphers
:    VPN gateways now provide new algorithms to help meet your security and compliance requirements.

   * IKE policy now supports the `sha384` value for authentication, `aes192` for encryption, and `15`, `16`, `17`, `18`, `20`, `21`, `22`, `23`, `24`, and `31` values for Diffie–Hellman groups.

   * IPsec policy now supports `sha384` and `disabled` values for authentication, `aes192`, `aes128gcm16`, `aes192gcm16`, and `aes256gcm16` values for encryption, and `group_15`, `group_16`, `group_17`, `group_18`, `group_20`, `group_21`, `group_22`, `group_23` , `group_24`, and `group_31` Diffie–Hellman groups.

   Specifying IKE and IPsec policies when you configure a VPN connection is optional. If a policy is not selected, one is chosen through _auto-negotiation_. For more information, see [About policy negotiation](/docs/vpc?topic=vpc-using-vpn#policy-negotiation).
   {: note}

### 20 September 2022
{: #vpc-september2022}
{: release-note}

Updating subnets for existing application load balancers
:   You can now add or remove subnets for existing ALBs by using the UI, API, or CLI. ETag support was added for load balancer resources, as it is required for any resource that allows arrays to be updated. For more information, see to [Updating subnets for existing application load balancers](/docs/vpc?topic=vpc-alb-updating-subnets&interface=ui).

:   For more information about using ETags, see [Concurrent update protection](/apidocs/vpc/latest#concurrent-update-protection).

### 12 September 2022
{: #vpc-september1222}
{: release-note}

New stock images for VPC
:   The following stock images are now available for x86-64 virtual server instances:
    - The Windows Server 2019 Standard Edition with SQL Server 2019 Web Edition bundle is now supported as an image when you provision a   {{site.data.keyword.vpc_short}} server. If you select this stock image when you provision a virtual server instance, the software that is part of that bundle is also included in your instance.
    - SUSE Linux Enterprise Server is now supported as an operating system stock image when you provision an x86-64 virtual server. For more information, see [x86-64 virtual server images](/docs/vpc?topic=vpc-about-images).

## August 2022
{: #vpc-august22}

### 31 August 2022
{: #vpc-august3122}
{: release-note}

Configuration governance
:   New VPC config rules for the Image service and Virtual Servers are now available with the Security and Compliance Center. For more information, see [Governing VPC Resource configuration](/docs/vpc?topic=vpc-manage-security-compliance#govern-vpc) in [Managing security and compliance with VPC Infrastructure Services](/docs/vpc?topic=vpc-manage-security-compliance).

### 30 August 2022
{: #vpc-august3022}
{: release-note}

IBM Cloud Hyper Protect Virtual Server for {{site.data.keyword.vpc_full}}
:   You can now create IBM Cloud Hyper Protect Virtual Server for {{site.data.keyword.vpc_short}} instances on LinuxONE (s390x processor architecture) in the United Kingdom (London) region, in addition to Brazil (São Paulo), Canada (Toronto), Japan (Tokyo), and US East (Washington DC) regions. To create IBM Cloud Hyper Protect Virtual Server for {{site.data.keyword.vpc_short}} instances on LinuxONE (s390x processor architecture), see [Creating virtual server instances](/docs/vpc?topic=vpc-creating-virtual-servers), and [IBM Hyper Protect Container Runtime image](/docs/vpc?topic=vpc-vsabout-images#hyper-protect-runtime). A valid contract is required for creating an instance. For more information, see [About the contract](/docs/vpc?topic=vpc-about-contract_se&interface=ui).

### 23 August 2022
{: #vpc-august2322}
{: release-note}

Additional user tag support for boot and data volumes
:  You can now add user tags to boot and data volumes when provisioning a virtual server instance or creating an instance template. You can add tags to the boot volume by editing it during instance provisioning. You can also add user tags for any data volumes you create and attach. If you import from a snapshot, any tags defined for the snapshot will be applied to the new volume. For more information, see [Create and attach a Block Storage volume when you create a new instance](/docs/vpc?topic=vpc-creating-block-storage&interface=api). For more information about user tags, see [Working with tags](/docs/account?topic=account-tag&interface=api).

### 17 August 2022
{: #vpc-august1722}
{: release-note}

New stock image for bare metal servers
:   Debian 11 is now supported as an image when you provision a bare metal server.

### 15 August 2022
{: #vpc-august1522}
{: release-note}

Health check metrics for application load balancer pools
:   Two new health check metrics have now been added to IBM Cloud Monitoring for application load balancers, specifically for pools:

* A metric for reporting the total number of members in a pool.
* A second metric for reporting the total number of healthy (or active) members in a pool.

:   For more information on these new metrics or the IBM Cloud Monitoring service, refer to [Monitoring Application Load Balancer for VPC metrics](/docs/vpc?topic=vpc-monitoring-metrics-alb).

### 09 August 2022
{: #vpc-august0922}
{: release-note}

VPC Instance Metadata service
:   A restriction was removed from the [instance metadata service](/docs/vpc?topic=vpc-imd-about&interface=ui) in which you had to stop and restart the virtual server instance to fully enable the metadata service. You can now create instances with the metadata service disabled and then enable the service for the instance to start using it immediately.

### 08 August 2022
{: #vpc-august0822}
{: release-note}

Virtual servers for VPC
:   You can now use the UI, CLI, and API to specify user tags for volume resources when you create an instance. You can add user tags to the instance's boot volume by editing the boot volume. You can also add user tags when attaching a data volume to the instance. For more information, see [Adding user tags to Block Storage volumes](/docs/vpc?topic=vpc-file-storage-vpc-about&interface=ui#storage-about-user-tags).

Snapshot and Backup for VPC
:   The [quota of snapshots and backup snapshots](/docs/vpc?topic=vpc-quotas#block-storage-quotas) you can create per volume has been increased to 750. For more information about how these quotas are applied, see [Considerations when creating snapshots](/docs/vpc?topic=vpc-snapshots-vpc-about#snapshots_vpc_considerations).

### 01 August 2022
{: #vpc-august0122}
{: release-note}

Sharing images across an enterprise account (beta)
:    You can now share or publish custom images to other accounts within your enterprise by using a private catalog. A private catalog provides a way for you to manage access to products for multiple accounts. You can use any existing x86 virtual server custom image with a private catalog, with the exception of an encrypted image. For more information, see [Getting started with custom images](https://test.cloud.ibm.com/docs/vpc?topic=vpc-planning-custom-images&interface=ui#custom-image-cloud-private-catalog).


## June 2022
{: #vpc-june22}

### 30 June 2022
{: #vpc-june0630}
{: release-note}

IBM Wazi as a Service (s390x processor architecture)
:   You can now create virtual server instances of IBM z/OS with IBM Wazi as a Service (Wazi aaS) image on IBM Z (s390x processor architecture) in IBM Cloud in the Japan (Tokyo), Brazil (São Paulo), Canada (Toronto), and United Kingdom (London) regions. The option to select the Wazi aaS z/OS dev and test image is offered as an IBM Cloud allow-listed service. For more information, see [IBM Wazi as a Service product page](https://www.ibm.com/cloud/wazi-as-a-service){: external}.

File Storage for VPC
:   You can now access a customer root key (CRK) from one account, and then use that key to encrypt file shares you create in another account. When you create the file share, you specify the CRN of a root key from the account that contains the key. For more information, see [Cross-account encryption for multitenant file storage resources](/docs/vpc?topic=vpc-vpc-byok-cross-acct-key-file).

### 24 June 2022
{: #vpc-june2422}
{: release-note}

New stock image for bare metal servers
:   Ubuntu (20.04 and 18.04) is now supported as an image when you provision a bare metal server.

### 21 June 2022
{: #vpc-june2122}
{: release-note}

Backup for VPC (GA)
:    You can now create automated backup snapshots of your Block Storage volumes. If your original volume is compromised, you can restore it from a backup snapshot. You create a backup policy to control which source volumes are selected for backup by matching user tags in the volume with tags that are defined in the policy. Each policy contains up to four backup plans, which define how often backup snapshots are taken (daily, weekly, monthly, or more frequently by using a cron-spec) and retained (by date or by count). You can also view backup jobs, which show status of backup snapshots that are being created or deleted. For more information about this service, see [Backup for VPC](/docs/vpc?topic=vpc-backup-service-about).

The backup policy jobs API remains in [beta](/apidocs/vpc-beta#24-may-2022).
{: note}

### 10 June 2022
{: #vpc-june0610}
{: release-note}

Block Storage for VPC
:    You can use the `volumes` API to restore an unattached data volume from a snapshot. Restoring from a snapshot creates a new, fully provisioned volume. The data volume that was created from the snapshot is fully hydrated (data is restored) when you later attach it to an instance. For more information, see [Restoring an unattached data volume from a snapshot](/docs/vpc?topic=vpc-snapshots-vpc-restore&interface=api#snapshots-vpc-restore-unattached-vol).

### 01 June 2022
{: #vpc-june0122}
{: release-note}

File Storage for VPC
:    For accounts authorized to preview this service, you can increase or decrease file share IOPS to meet your performance needs. Adjust IOPS within an IOPS tier profile or a custom profile. Or, adjust IOPS between profiles, for example, from a 3 IOPS/GB tiered profile to a custom profile. Adjusting IOPS within a profile or between profiles depends on the file share size. For more information, see [Adjusting file share IOPS](/docs/vpc?topic=vpc-adjusting-share-iops).

## May 2022
{: #vpc-may22}

### 27 May 2022
{: #vpc-may2722}
{: release-note}

Secrets Manager for application load balancers
:    Application load balancers now support [IBM Secrets Manager](/docs/secrets-manager?topic=secrets-manager-getting-started). With Secrets Manager, you can create, lease, and centrally manage secrets that are used in {{site.data.keyword.cloud}} services or your custom-built applications.

:    As a reminder, end of support for IBM Cloud Certificate Manager was 31 December 2022. Remaining instances of Certificate Manager have been deleted. If you have any user-provided Ingress secrets stored in Certificate Manager, they are no longer valid.

### 17 May 2022
{: #vpc-may1722}
{: release-note}

File Storage for VPC
:    For accounts authorized to preview this service, you can configure replication for new and existing file shares. Replication creates a read-only copy of your file share data in a different zone. You can fail over to the replica share if the source share becomes damaged or compromised. For more information, see [About file share replication](/docs/vpc?topic=vpc-file-storage-replication).

:    You can now add user tags from the UI, CLI, or API when you create a new file share or update file shares. For more information, see [Adding user tags](/docs/vpc?topic=vpc-file-storage-managing&interface=ui#fs-add-tags-shares-ui).


## April 2022
{: #vpc-apr22}

### 29 April 2022
{: #vpc-apr2922}
{: release-note}

Backup for VPC (LA)
:    Accounts authorized to preview this service can create backup policies and plans to automatically back up Block Storage volumes. Backup policies control which source volumes are selected for backup by matching user tags in the volume with tags that are defined in the backup policy. Policies can contain up to four backup plans, which specify how often backup snapshots are taken (daily, weekly, monthly, or by using a `cron-spec`) and retained (by date or by count). You can also view backup jobs, which show status of backup snapshots that are being created or deleted. This release also provides new functionality for restoring volumes from backup snapshots. For more information about this service, see [Backup for VPC](/docs/vpc?topic=vpc-backup-service-about) concepts.

### 28 April 2022
{: #vpc-apr2822}
{: release-note}

UI Updates
:   The following UI updates were made:
    - The custom image details information was moved from the side panel to a separate custom image details page.
    - Previously, when you changed the region or zone while you provision a virtual server instance, you had to click either Save or Cancel to continue. This behavior was changed and you don't need to make that selection when you change the region or zone.
    - You can now delete the virtual server instance without manually unbinding the floating IP address. When you delete the virtual server instance, the floating IP address is now automatically unbound before the virtual server instance is deleted. This UI change now matches how the virtual server instance is deleted when you use the CLI or API.

### 11 April 2022
{: #vpc-apr1122}
{: release-note}

2022-03-29 release of the VPC API introduced incompatible changes
:    The `2022-03-29` release of the VPC API necessitated incompatible changes in support of the reserved IPs feature:
     - IP addresses are now modeled as objects (resources), rather than strings.
     - Security groups must now be associated with targets rather than network interfaces.

:    Even if you are not planning to use reserved IPs, to avoid regressions in client functionality, be sure to reference [2022-03-29 API migration](/docs/vpc?topic=vpc-2022-03-29-migration) and follow the Action needed recommendations before you specify version `2022-03-29` or later. For more information, see the [API change log](/docs/vpc?topic=vpc-api-change-log#version-2022-03-29) and [Reserved IP known issues](/docs/vpc?topic=vpc-known-issues#ip-known-issues).

### 7 April 2022
{: #vpc-apr0722}
{: release-note}

Backup for VPC (limited availability)
:    For accounts authorized to preview this service, you can create backup policies that automatically back up your Block Storage volumes. Backups are triggered when a user tag is applied to a volume matches a backup policy tag. Each backup policy has a backup plan, which defines how often backups are taken and how long they're retained. With this release, you can create and update up to four backup plans per policy. You can also track backup job status when a backup is created. For more information, see [About Backup for VPC](/docs/vpc?topic=vpc-backup-service-about).

## March 2022
{: #vpc-mar22}

### 31 March 2022
{: #vpc-march3122}
{: release-note}

Add "Other" device types as Application Load Balancer (ALB) pool members
:   You can now add "Other" device types as ALB back-end pool members, such as servers contained within a Power Systems Virtual Server instance connected over IBM Cloud Direct Link. In the past, you were only able to select virtual server instances or Bare Metal servers within a VPC. When you create a new member, select the **Other** tab from the Attach server screen and enter the device IP address. For more information, see [Creating an IBM Cloud Application Load Balancer for VPC](/docs/vpc?topic=vpc-load-balancer&interface=ui).

### 30 March 2022
{: #vpc-march3022}
{: release-note}

New stock image for bare metal servers
:   RHEL 8.4 is now supported as an image when you provision a bare metal server.

### 29 March 2022
{: #vpc-march2922}
{: release-note}

UDP support for Network Load Balancers (NLB)
:   You can now set User Datagram Protocol (UDP) as the communication protocol for the {{site.data.keyword.nlb_full}} (NLB) listener and pool. UDP is a communications protocol for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party. For more information, see [Configuring the UDP protocol for network load balancers](/docs/vpc?topic=vpc-nlb-udp&interface=ui).

:   When you configure UDP and attaching a pool to your listener, you must configure the pool with the same protocol as the listener.
{: important}

Reserved IPs
:   You can now assign an IP address to your virtual server instance by specifying an already reserved IP for private IPs and bind them to network interfaces. For more information, see [Managing IP addresses](/docs/vpc?topic=vpc-managing-ip-addresses).

## 25 March 2022
{: #vpc-march2522}
{: release-note}

LinuxONE (s390x processor architecture)
:   You can now create virtual server instances on LinuxONE (s390x processor architecture) in IBM Cloud in the Japan (Tokyo), Brazil (São Paulo), Canada (Toronto), and United Kingdom (London) regions. For more information about available LinuxONE (s390x processor architecture) profiles, see [s390x instance profiles](/docs/vpc?topic=vpc-vs-profiles). To create instances on LinuxONE (s390x processor architecture), see [Creating virtual server instances by using the UI](/docs/vpc?topic=vpc-creating-virtual-servers).

## 24 March 2022
{: #vpc-march2422}
{: release-note}

New stock image for virtual servers
:   Windows&reg; 2022 is now supported as a stock image when you provision {{site.data.keyword.vpc_short}} virtual servers.

## 10 March 2022
{: #vpc-march1022}
{: release-note}

New stock image for virtual servers
:   Debian 11 is now supported as a stock image when you provision {{site.data.keyword.vpc_short}} virtual servers.


## February 2022
{: #vpc-feb22}

### 24 February 2022
{: #vpc-feb2422}
{: release-note}

VPC Instance Metadata Service (GA)
:   The VPC Instance Metadata service is now generally available in all regions. This free service provides a REST API that you invoke within an instance to get information about that instance. Access to the API is unavailable from outside the instance. The service is disabled by default. Before you can access the metadata, you need to use the service to generate an instance identity access token for accessing the metadata service. You can optionally get an IAM token from this token to access all IAM-enabled services. For more information, see [About VPC Instance Metadata](/docs/vpc?topic=vpc-imd-about).

:   Virtual server instances created on LinuxONE (s390x processor architecture) are not enabled for the VPC Instance Metadata service. The metadata service is supported only on x86 systems.
{: note}

UI Update
:   A new Location cascading selector is available. For example, when you provision a virtual server, the Location section now has three new cascading selector boxes. You can now choose the geographic location, the metro (region) location, and the zone. The options available in these boxes are updated that are based on your selections. If you select “Americas” for the Geography, then the Metro box displays only the Metros available for the Americas.

### 22 February 2022
{: #vpc-feb2222}
{: release-note}

Host failure recovery policies
:    Host failure recovery policies for VPC are generally available (GA). For more information about host failure recovery policies, see [Host failure recovery policies](/docs/vpc?topic=vpc-host-failure-recovery-policies&interface=ui).

### 15 February 2022
{: #vpc-feb1522}
{: release-note}

LinuxONE (s390x processor architecture)
:   You can now create virtual server instances on LinuxONE (s390x processor architecture) in IBM Cloud in the Japan (Tokyo), United Kingdom (London), and São Paulo regions. For more information about available LinuxONE (s390x processor architecture) profiles, see [s390x instance profiles](/docs/vpc?topic=vpc-vs-profiles). To create instances on LinuxONE (s390x processor architecture), see [Creating virtual server instances by using the UI](/docs/vpc?topic=vpc-creating-virtual-servers).

Resizable boot volumes
:    You can now increase the capacity of a boot volume, up to 250 gigabytes (GB), when you create an instance from an image or instance template. You can also directly update an existing boot volume to increase its capacity. For more information, see [Increasing boot volume capacity](/docs/vpc?topic=vpc-resize-boot-volumes).

Backup for VPC (closed beta)
:    For accounts authorized to preview this service, you can create backup policies that automatically backup your Block Storage volumes. Backups are triggered when a user tag is applied to a volume matches a backup policy tag. Each backup policy has a backup plan, which defines how often backups are taken and how long they're retained. For more information, see [About Backup for VPC (Beta)](/docs/vpc?topic=vpc-backup-service-about).

File Storage for VPC
:    The file service is now integrated with the Security and Compliance Center to help you manage security and compliance for your organization. For more information about this feature, see [Managing security and compliance](/docs/vpc?topic=vpc-file-storage-managing&interface=ui#fs-vpc-manage-security).

### 14 February 2022
{: #vpc-feb1422}
{: release-note}

Snapshots for VPC
:    The snapshots service is now integrated with the Security and Compliance Center to help you manage security and compliance for your organization. For more information about this feature, see [Managing security and compliance](/docs/vpc?topic=vpc-snapshots-vpc-manage&interface=ui#snapshots-vpc-manage-security).

### 11 February 2022
{: #vpc-feb1122}
{: release-note}

Maximum bandwidth for each vNIC is increased
:   The maximum bandwidth for a vNIC is now 25 Gbps instead of the previous 16 Gbps to 25 Gbps. For more information, see [Optimizing network bandwidth allocation for profiles](/docs/vpc?topic=vpc-bandwidth-allocation-profiles#network-perf-notes-for-profiles).

### 10 February 2022
{: #vpc-feb1022}
{: release-note}

Block Storage attachments
:    Limits on the number of Block Storage data volumes you can attach to an instance are amended. Previously, instances that were created from smaller vCPU profiles attached only up to four data volumes. These limits are removed. For all instances, you can attach up to 12 Block Storage data volumes.

### 08 February 2022
{: #vpc-feb0822}
{: release-note}

Port ranges for public network load balancers
:    When [creating a public network load balancer](/docs/vpc?topic=vpc-nlb-ui-creating-network-load-balancer&interface=api), you can now specify a range of listener ports.

Bare Metal server support for application load balancers
:    Bare Metal server members are now supported on application load balancers. For more information, see [Load balancers for VPC overview](/docs/vpc?topic=vpc-nlb-vs-elb&interface=ui).

## January 2022
{: #vpc-jan22}

### 31 January 2022
{: #vpc-jan3122}
{: release-note}

Bare Metal Servers for VPC
:    Bare Metal Servers for VPC is generally available (GA). For more information about bare metal servers, see [About Bare Metal Servers for VPC](/docs/vpc?topic=vpc-about-bare-metal-servers).

### 25 January 2022
{: #vpc-jan2522}
{: release-note}

Security group support for Virtual Private Endpoint (VPE) gateways
:   You can now attach security groups to your endpoint gateways and manage them for your application needs. Attach security groups when you create an endpoint gateway, or modify security groups that are bound to an endpoint gateway after provisioning. For more information, see [Configuring ACLs and security groups for use with endpoint gateways](/docs/vpc?topic=vpc-configure-acls-sgs-endpoint-gateways).

Update to Snapshots for VPC
:   When you view details of a snapshot from the [UI](/docs/vpc?topic=vpc-snapshots-vpc-view&interface=ui#snapshots-vpc-view-snapshot-ui), [CLI](/docs/vpc?topic=vpc-snapshots-vpc-view&interface=cli#snapshots-vpc-view-details-cli), or [API](/docs/vpc?topic=vpc-snapshots-vpc-view&interface=api#snapshots-vpc-view-api), a new field shows when the snapshot was captured from the volume. This feature applies to snapshots created after January 2022.

### 21 January 2022
{: #vpc-jan2122}
{: release-note}

New stock images for virtual servers
:   The following stock images are now available for virtual servers:
    - Red Hat 8.4 for SAP
    - SLES 12 SP5 for SAP
    - SLES 15 SP3 for SAP

### 14 January 2022
{: #vpc-jan1422}
{: release-note}

Application Load Balancer (ALB) for VPC
:   Application load balancers now support HTTP/HTTPS compression, which you use to compress data that is transmitted to your users. For more information, see [Compression (HTTP/HTTPS only)](/docs/vpc?topic=vpc-advanced-traffic-management#compression).

High Availability (HA) Virtual Network Function (VNF) support
:   Support for a highly available, highly resilient virtual network functions can be achieved by using the "routing mode" feature of the IBM Cloud Network Load Balancer (NLB) for VPC. For more information, see [About virtual network functions over VPC](/docs/vpc?topic=vpc-about-vnf) and [About HA VNF deployments](/docs/vpc?topic=vpc-about-vnf-ha).

Updates to Getting started with IBM Cloud VPC button
:   The "Getting started with IBM Cloud VPC" button now includes access to tours that are specific to what you are doing on the IBM console. If a tour is not available, the button takes you to the VPC List view.

### 06 January 2022
{: #vpc-jan0622}
{: release-note}

UI update when you create a virtual server
:   When you create a virtual server, the UI is updated to include a link in the Operating system section that opens a panel that contains information about the image lifecycle.

## December 2021
{: #vpc-dec21}

### 16 December 2021
{: #vpc-dec1621}
{: release-note}

File Storage for VPC (LA)
:   {{site.data.keyword.filestorage_vpc_full}} is now available for customers with special approval to preview this service in the Washington, Dallas, Frankfurt, London, Sydney, and Tokyo regions.

:   For more information about this service, see [About File Storage for VPC](/docs/vpc?topic=vpc-file-storage-vpc-about).

### 09 December 2021
{: #vpc-dec0921}
{: release-note}

Security updates
:   The following stock images were refreshed with the most recent fixes and security updates.
    - Debian version 10
    - CentOS version 7
    - RHEL versions 7, 8.2, and 8.4
    - Ubuntu version 20.04

Windows stock image updates
:   For all Windows&reg; stock images, TLS 1.2 was enabled and all earlier versions were disabled.

:   The following cloudbase-init configuration files were updated to add the value "ntp_use_dhcp_config=true":
    - C:\Program Files\Cloudbase Solutions\Cloudbase-Init\conf\cloudbase-init.conf
    - C:\Program Files\Cloudbase Solutions\Cloudbase-Init\conf\cloudbase-init-unattend.conf

New stock image for virtual servers
:   Rocky Linux version 8.5 is now supported as a stock image when you provision {{site.data.keyword.vpc_short}} virtual servers.

## November 2021
{: #vpc-nov21}

### 30 November 2021
{: #vpc-nov3021}
{: release-note}

VPN client-to-site servers update (open beta)
:   You can now update a VPN server after the VPN is provisioned. For example, you can upgrade a stand-alone VPN server (one subnet) to a High Availability (HA) VPN server (two subnets in different zones). You can also detach a subnet to downgrade an HA VPN server to a stand-alone deployment, or change an attached subnet after your VPN server is provisioned. For more information, see [Upgrading to an HA VPN server](/docs/vpc?topic=vpc-vpn-client-to-site-change-server-types).

### 16 November 2021
{: #vpc-nov1621}
{: release-note}

New Very High Memory and Ultra High Memory instance profile family for dedicated host (LA)
:   Very High Memory with instance storage and Ultra High Memory with instance storage profiles are now available for dedicated host.

:   Very High Memory profiles offer a core to RAM ratio of 1 vCPU to 14 GiB of RAM. This family is hosted exclusively on the latest generation Intel® Xeon® Platinum Cascade Lake server hosts and is best for OLAP workloads and SAP-related services, such as SAP NetWeaver. Very High Memory profiles are available in the US South (Dallas), US East (Washington DC), Canada (Toronto), United Kingdom (London), EU Germany (Frankfurt), Japan (Tokyo), Japan (Osaka), and Australia (Sydney) regions. For more information, see [Very High Memory with instance storage profiles](/docs/vpc?topic=vpc-dh-profiles#vhm-is-dh-pr).

:   Ultra High Memory profiles offer a core to RAM ratio of 1 vCPU to 28 GiB of RAM. This family is hosted exclusively on the latest generation Intel® Xeon® Platinum Cascade Lake server hosts and is optimized for running memory intensive applications and in-memory database such as SAP HANA, Memcached, or Redis. Ultra High Memory profiles are available in the US South (Dallas) and EU Germany (Frankfurt) regions. For more information, see [Ultra HIgh Memory with instance storage profiles](/docs/vpc?topic=vpc-dh-profiles#uhm-is-dh-pr).

### 12 November 2021
{: #vpc-nov1221}
{: release-note}

Fedora Core OS
:   Fedora Core OS is now available in all regions as a stock image. The user login ‘root’ is disabled by default in Fedora Core OS. The user login ‘core’ can be used to log in to Fedora Core OS instances. For more information, see [Virtual server images](/docs/vpc?topic=vpc-about-images#x86-supported-os) and [User data examples for Fedora Core OS](/docs/vpc?topic=vpc-user-data#user-data-examples-for-fed-core).

### 02 November 2021
{: #vpc-nov0221}
{: release-note}

Instance Metadata Service for VPC (LA)
:   The metadata service is now available in all regions to customer accounts authorized to access this service. This service is enabled by default when you create new instances by using the UI, CLI, or API. You can also disable the service from these interfaces. For more information, see [Enable or disable the metadata service](/docs/vpc?topic=vpc-imd-configure-service&interface=ui#imd-metadata-service-enable).

:   The metadata service also provides a new API call to generate an IAM token from the instance identity access token by using trusted profile information. For more information, see [Generate an IAM token from an instance identity access token](/docs/vpc?topic=vpc-imd-configure-service&interface=api#imd-token-exchange).

Snapshots for VPC (GA)
:   You can now delete any or all snapshots not actively restoring a volume. Snapshots can be anywhere in the snapshot chain and must be in a `stable` state. For more information, see [Deleting snapshots](/docs/vpc?topic=vpc-snapshots-vpc-manage&interface=ui#snapshots-vpc-delete).

## October 2021
{: #vpc-oct21}

### 21 October 2021
{: #vpc-oct2121}
{: release-note}

UI Updates
:    When you create a virtual server instance by using the UI, the image selection on the UI was updated. The image selection is changed from a tile selection to a drop-down menu. For both custom and catalog images, a new side panel is available that you can use to filter, sort, and search for images.

### 15 October 2021
{: #vpc-oct1521}
{: release-note}

New GPU Instance Profile family
:   GPU profiles are available for all images. The profiles include attached NVIDIA 16 GB PCIe v100 GPUs. Drivers must be installed separately. You can use these instances to accelerate certain processing functions for workloads such as inferencing and machine learning. For more information about this service, see [Managing GPUs](/docs/vpc?topic=vpc-managing-gpus).

### 05 October 2021
{: #vpc-oct0521}
{: release-note}

New regions for Very High Memory instance profile family (LA)
:   Very High Memory profiles now are available in the United Kingdom (London), Japan (Osaka), and Australia (Sydney) regions. For more information, see [Very High Memory profiles](/docs/vpc?topic=vpc-profiles&interface=ui#vhmemory).

### 01 October 2021
{: #vpc-oct0121}
{: release-note}

File Storage for VPC (LA)
:   {{site.data.keyword.filestorage_vpc_full}} is now available in the United Kingdom (London) region. For more information about this service, see [About File Storage for VPC](/docs/vpc?topic=vpc-file-storage-vpc-about).

## September 2021
{: #vpc-sep21}

### 23 September 2021
{: #vpc-sep2321}
{: release-note}

VNF routing mode for network load balancers
:   With {{site.data.keyword.vpc_short}}, you can provision Virtual Network Function (VNF) devices to gain better and more affordable scalability than you would by purchasing physical network devices. {{site.data.keyword.vpc_short}} network load balancers with routing mode that you use to send traffic to only VNF devices as back-end targets. In addition, their health checks ensure that workloads only travel through healthy VNF devices. For more information about this service, see [Creating a network load balancer with routing mode for VPC](/docs/vpc?topic=vpc-nlb-vnf).

### 14 September 2021
{: #vpc-sep1421}
{: release-note}

Terraform available for Placement Groups
:   You can now create and manage placement groups in your {{site.data.keyword.vpc_short}} by using Terraform. See [Managing placement groups](/docs/vpc?topic=vpc-managing-placement-group&interface=terraform).

### 07 September 2021
{: #vpc-sep0721}
{: release-note}

New Very High Memory instance profile family (LA)
:   Very High Memory profiles are available in the US South (Dallas), US East (Washington DC), Canada (Toronto), EU Germany (Frankfurt), and Japan (Tokyo) regions. Very High Memory profiles offer a core to RAM ratio of 1 vCPU to 14 GiB of RAM. This family is optimized for running high-compute-intensity in-memory workloads like SAP BW/4 HANA. For more information, see [Very High Memory profiles](/docs/vpc?topic=vpc-profiles&interface=ui#vhmemory).

Instance Bandwidth (LA)
:   Instance bandwidth is now available in the US South (Dallas), US East (Washington DC), Canada (Toronto), EU Germany (Frankfurt), Japan (Osaka), Brazil (Sao Paulo) regions. When you provision a virtual server instance, you can now allocate bandwidth between attached volumes and networking by using the API and CLI. You can adjust bandwidth after you provision a virtual server instance by using the UI, API, and CLI. The maximum bandwidth capacity is determined by the instance profile that you select during instance provisioning. For more information, see [Bandwidth allocation for instance profiles](/docs/vpc?topic=vpc-bandwidth-allocation-profiles).

### 01 September 2021
{: #vpc-sep0121}
{: release-note}

New GPU Instance Profile family (Beta)
:   GPU profiles are available in a limited, allow-listed beta for all images. The profiles include attached NVIDIA 16 GB PCIe v100 GPUs. Drivers must be installed separately. You can use these instances to accelerate certain processing functions for workloads such as inferencing and machine learning. For more information about this service, see [Managing GPUs](/docs/vpc?topic=vpc-managing-gpus).

## August 2021
{: #vpc-aug21}

### 26 August 2021
{: #vpc-aug2621}
{: release-note}

RHEL on SAP image support update
:   When you provision a virtual server instance and select {{site.data.keyword.redhat_full}} Enterprise Linux, be aware that locking a version must be done manually. When you log in to your operating system, a message is displayed with the command that you need to manually lock the operating system version. Performing a “yum update” without the version locking results in the operating system that is upgrading to the latest RHEL release, which is 8.4.

Block Storage for VPC
:   For Block Storage for VPC volumes attached to a virtual server instance, you can increase or decrease IOPS for a volume by specifying a different IOPS tier profile or different IOPS value withing a custom IOPS band. For more information, see [Adjusting IOPS for Block Storage volumes](/docs/vpc?topic=vpc-adjusting-volume-iops).

Client-to-site VPN servers (Beta)
:   Until now, the {{site.data.keyword.cloud_notm}} VPN for VPC service that is supported only site-to-site connectivity, which connects your on-premises network to the {{site.data.keyword.cloud_notm}} VPC network. This Beta adds client-to-site connectivity, which allows users to connect to their {{site.data.keyword.cloud_notm}} VPC infrastructure through a secure or encrypted connection over the internet. This service is especially useful for individuals that are working at home, traveling, or at locations where site-to-site VPN might not be available. For more information, see [About client-to-site VPN servers](/docs/vpc?topic=vpc-vpn-client-to-site-overview).

### 24 August 2021
{: #vpc-aug2421}
{: release-note}

HTTPS redirect listeners
:   The [HTTPS redirect feature](/docs/vpc?topic=vpc-load-balancers#https-redirect-listener) is now available on Application Load Balancer for VPC to redirect traffic from an HTTP load balancer listener to an HTTPS listener. You can configure an HTTPS redirect on either [load balancer listeners](/docs/vpc?topic=vpc-load-balancers), [load balancer policies](/docs/vpc?topic=vpc-layer-7-load-balancing), or both.

Virtual server instances for VPC
:   When you provision an instance, you can now allocate I/O bandwidth between storage and network bandwidth from the total instance bandwidth. The maximum bandwidth capacity is determined by the instance profile that you selected during instance provisioning. For more information, see [Bandwidth allocation for instance profiles](/docs/vpc?topic=vpc-bandwidth-allocation-profiles).

### 19 August 2021
{: #vpc-aug1921}
{: release-note}

Larger size boot volumes for custom images
:   You can import custom images with a boot disk size from 10 - 250 GB, which becomes the image's minimum provisioned size after you import. When you specify the image as part of [creating an instance](/docs/vpc?topic=vpc-creating-block-storage), the boot volume capacity is set to this size. For more information, see [Planning custom images](/docs/vpc?topic=vpc-planning-custom-images).

### 18 August 2021
{: #vpc-aug1821}
{: release-note}

File Storage for VPC
:   Custom IOPS profiles are available with capacity up to 16,000 GB. For more information, see [File Storage profiles](/docs/vpc?topic=vpc-file-storage-profiles).

:   You can also increase the file share size from its original capacity in GB increments up to 32,000 GB capacity, depending on your share profile. For more information, see [Expanding file share capacity](/docs/vpc?topic=vpc-file-storage-expand-capacity).

:   {{site.data.keyword.filestorage_vpc_full}} is available to customers with special approval to preview this service in the Washington, Dallas, and Frankfurt regions.

### 17 August 2021
{: #vpc-aug1721}
{: release-note}

Instance Identifier Update
:   The instance identifier (ID) now includes the SMBIOS system-uuid as a portion of the ID. The ID, including the SMBIOS system-uuid portion, is static and persists for the lifecycle of the virtual server instance until that virtual server instance is deleted. For more information, including how to retrieve this information from within your virtual server, see [Retrieving the virtual server instance identifier](/docs/vpc?topic=vpc-managing-virtual-server-instances#retrieve-VSI-instance-identifer) section in Managing virtual server instances.

Placement groups (GA)
:   Placement groups for {{site.data.keyword.vpc_full}} are used to create placement group strategies for managing high availability workloads. A placement group contains virtual server instances that share a common placement strategy. Placement strategies influence the physical placement of select VPC resources to meet certain workload demands. For more information about placement groups, see [About placement groups](/docs/vpc?topic=vpc-about-placement-groups-for-vpc).

### 11 August 2021
{: #vpc-aug1121}
{: release-note}

Auto scale supports data volumes and private catalog
:   Instance groups now support by using an instance template that includes one or more data volumes. In addition, instance groups are now supported in private catalog. For more information about instance groups, see [Creating an instance group for auto scaling](/docs/vpc?topic=vpc-creating-auto-scale-instance-group).

### 9 August 2021
{: #vpc-aug0921}
{: release-note}

LinuxONE (s390x processor architecture)
:   You can now create virtual server instances on LinuxONE (s390x processor architecture) in IBM Cloud in the Tokyo region. For more information about available LinuxONE (s390x processor architecture) profiles, see [s390x instance profiles](/docs/vpc?topic=vpc-vs-profiles). To create instances on LinuxONE (s390x processor architecture), see [Creating virtual server instances by using the UI](/docs/vpc?topic=vpc-creating-virtual-servers).
For more information about some of the limitations of LinuxONE (s390x processor architecture), see [Service limitations](/docs/vpc?topic=vpc-limitations).

## July 2021
{: #vpc-jul21}

### 26 July 2021
{: #vpc-jul2621}
{: release-note}

New São Paulo region
:   The São Paulo region endpoint is now in service at `https://br-sao.iaas.cloud.ibm.com`. For more information, see [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region).

### 22 July 2021
{: #vpc-jul2221}
{: release-note}

Block Storage for VPC
:   IOPS tier and custom profiles are available with volume capacity up to 16,000 GB. For more information, see [Block Storage profiles](/docs/vpc?topic=vpc-block-storage-profiles).

:   For secondary volumes attached to a virtual server instance, you can increase capacity in GB increments up to 16,000 GB, depending on the volume's profile. The volume capacity is immediately increased. For more information, see [Expanding Block Storage volume capacity](/docs/vpc?topic=vpc-expanding-block-storage-volumes).

### 21 July 2021
{: #vpc-jul2121}
{: release-note}

Bare Metal Servers for VPC (closed beta)
:   If your account is granted special approval to preview this feature, you can now create bare metal servers to host VMware clusters in VPC. You can set up VMware management applications and create VMware virtual machines (VM) on the bare metal servers. As bare metal servers are integrated with the VPC platform, you can take advantage of the network, storage, and security capabilities provided by the VPC. For more information, see [About Bare Metal Servers for VPC (beta)](/docs/vpc?topic=vpc-about-bare-metal-servers).

:   The bare metal console feature is temporarily unavailable. An "unauthorized" error is returned if you try to connect to the console.

### 13 July 2021
{: #vpc-jul1321}
{: release-note}

Instance Identifier Update
:   The instance identifier (ID) now includes the SMBIOS system-uuid as a portion of the ID. The ID, including the SMBIOS system-uuid portion, is static and persists for the lifecycle of the virtual server instance until that virtual server instance is deleted. For more information, including how to retrieve this information from within your virtual server, see [Retrieving the virtual server instance identifier](/docs/vpc?topic=vpc-managing-virtual-server-instances#retrieve-VSI-instance-identifer) section in Managing virtual server instances.

### 6 July 2021
{: #vpc-jul0621}
{: release-note}

File Storage for VPC
:   The file storage general purpose 3 IOPS/GB profile is expanded so you can create file shares up to 32 TB with potential max IOPS performance of 96,000 IOPS. For more information, see [File Storage profiles](/docs/vpc?topic=vpc-file-storage-profiles). File Storage for VPC is available to customers with special approval to preview this service in the Washington, Dallas, and Frankfurt regions.

## June 2021
{: #vpc-jun21}

### 30 June 2021
{: #vpc-jun3021}
{: release-note}

Placement groups (Beta)
:   Placement groups for {{site.data.keyword.vpc_full}} are used to create placement group strategies for managing high availability workloads. A placement group contains virtual server instances that share a common placement strategy. Placement strategies influence the physical placement of select VPC resources to meet certain workload demands. For more information about placement groups, see [About placement groups](/docs/vpc?topic=vpc-about-placement-groups).

### 17 June 2021
{: #vpc-jun1721}
{: release-note}

UI enhancement
:   When you provision a VPC, you can now create multiple subnets from the default address prefix. When you create a VPC, one subnet is created in each zone of the VPC region. You can add up to a maximum of nine subnets.”

Application Load Balancer (ALB) support for cookie-based session persistence
:   ALBs now supports HTTP-cookie persistence and application-cookie persistence. For more information, see [Advanced traffic management](/docs/vpc?topic=vpc-advanced-traffic-management#session-persistence).

### 03 June 2021
{: #vpc-jun0321}
{: release-note}

UI enhancement
:   When you delete a virtual server, you must now confirm that you want to delete an instance by typing *delete*.

## May 2021
{: #vpc-may21}

### 25 May 2021
{: #vpc-may2521}
{: release-note}

Snapshots for VPC
:   Snapshots for VPC is a regional offering that lets you create a point-in-time copy of your Block Storage boot or data volume. Select a snapshot during instance provisioning and restore a new, fully-provisioned boot volume to start the instance. You can also create and attach a data volume from a snapshot within a running virtual server instance. Learn more [about creating and using snapshots](/docs/vpc?topic=vpc-snapshots-vpc-about) and explore the new [snapshots API methods](/apidocs/vpc#delete-snapshots).

## 21 May 2021
{: #vpc-may2121}
{: release-note}

Image from volume
:   You can create a custom image from a boot volume on a virtual server instance. The image is a full copy of the source volume, including the operating system and any user data. You can create new virtual server instances from the image created from the volume. For more information, see [About creating an image from a volume](/docs/vpc?topic=vpc-image-from-volume-vpc).

### 13 May 2021
{: #vpc-may1321}
{: release-note}

Scheduled Scaling for VPC (GA)
:   Scheduled Scaling for VPC lets you set scheduled actions to automatically scale instance group capacity up or down based on daily, intermittent, or seasonal demand. You can set multiple, recurring scheduled action frequencies that can scale monthly, weekly, daily, hourly, or even every set number of minutes. For more information, see [Scheduled scaling](/docs/vpc?topic=vpc-scheduled-scaling-vpc).

### 15 May 2021
{: #vpc-may1521}
{: release-note}

Virtual Private Cloud (VPC) Gen 1 end of service
:   Virtual Private Cloud (VPC) Gen 1 reached end of service on 26 February 2021. The VPC on Classic API reference has been removed from the library page on 15 May, 2021. VPC on Classic users are being redirected to the [Virtual Private Cloud API](/apidocs/vpc).

### 06 May 2021
{: #vpc-may0621}
{: release-note}

New Ultra High Memory instance profile family (LA)
:   Ultra High Memory profiles are hosted exclusively on the latest generation Intel® Xeon® Platinum Cascade Lake server hosts and are optimized for running memory intensive applications and in-memory database such as SAP HANA, Memcached, or Redis. This profile family offers our highest vCPU to memory ratio with 28 GiB of memory for every 1 vCPU of compute and up to 5.7 TiB of available RAM. For more information, see [x86 Instance Profiles](/docs/vpc?topic=vpc-profiles).

:   The Ultra High Memory family of profiles is currently available in the Dallas and Frankfurt multizone regions(MZRs). For more information, see the Multizone regions section in [Locations for resource deployment](/docs/overview?topic=overview-locations#mzr-table). Contact your IBM Sales representative if you need Ultra High Memory profiles in a MZR other than Dallas or Frankfurt.

## April 2021
{: #vpc-apr21}

### 30 April 2021
{: #vpc-apr3021}
{: release-note}

File Storage for VPC
:   File Storage for VPC is available to customers with special approval to preview this service in the Washington, Dallas, and Frankfurt regions. With this feature, you can create NFS-based file shares in a single zone in a region. You can share file storage over multiple virtual service instances within the same zone across multiple VPCs. For more information about this service, see [About File Storage for VPC](/docs/vpc?topic=vpc-file-storage-vpc-about). Contact your IBM Sales representative if you are interested in getting access.

### 07 April 2021
{: #vpc-april0721}
{: release-note}

File Storage for VPC (beta)
:   NFS-based file shares for a zone within a region are available in a limited, allow-listed beta. You can share file storage over multiple virtual service instances within the same zone across multiple VPCs. For more information about this service, see [About File Storage for VPC (beta)](/docs/vpc?topic=vpc-file-storage-vpc-about).

UI enhancement
:   When provisioning a new VPN gateway in a default VPC, the UI now populates the subnet table with the default subnet information.

### 06 April 2021
{: #vpc-apr0621}
{: release-note}

New Toronto region
:   The Toronto region endpoint is now in service at `https://ca-tor.iaas.cloud.ibm.com`. For more information, see [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region).

### 01 April 2021
{: #vpc-apr0121}
{: release-note}

Instance storage
:   You can now provision a virtual server instance with instance storage, a set of one or more solid state drives directly attached to your instance. An instance storage disk provides fast, affordable, temporary storage to improve the performance of cloud-native workloads with scratch space, caching buffers, or a place for replicated data. To provision a virtual server instance with instance storage, you must select an instance storage [profile](/docs/vpc?topic=vpc-profiles). For more information, see [About instance storage](/docs/vpc?topic=vpc-instance-storage).

Dedicated hosts support instance storage
:   You can now provision a dedicated host with an instance storage profile, providing the capability to host virtual server instances that include instance storage. For more information, see [Dedicated host profiles](/docs/vpc?topic=vpc-dh-profiles).

Instance resize (GA)
:   The ability to resize a virtual server instance by selecting a different profile to assign to the instance is now generally available. Profiles are a combination of instance attributes, such as the number of vCPUs, amount of RAM, network bandwidth, and more that define the size and capabilities of the virtual server instance. For more information, see [Resizing an instance](/docs/vpc?topic=vpc-resizing-an-instance).

## March 2021
{: #vpc-mar21}

### 31 March 2021
{: #vpc-mar3121}
{: release-note}

Virtual server instance console
:   The virtual server instance console feature is now generally available in all regions. For more information, see [Accessing virtual server instances by using VNC or serial consoles](/docs/vpc?topic=vpc-vsi_is_connecting_console).

### 25 March 2021
{: #vpc-mar2521}
{: release-note}

New parameter-based rule types for application load balancers
:   When creating policy rules for {{site.data.keyword.cloud}} {{site.data.keyword.alb_full}} (ALB), the `field` property may now be set to `query` or `body` to perform additional forms of layer 7 load balancing.
   * `query` - Write layer 7 rules that use the query string to route traffic to a specific target.
   * `body` - If the body of the `POST` request uses form encoding (UTF-8), then you can create layer 7 rules to route traffic based on the parameter name and value in the body. For more information, refer to [Layer 7 load balancing](/docs/vpc?topic=vpc-layer-7-load-balancing).

TCP keep alive support for application load balancers
:   {{site.data.keyword.cloud}} {{site.data.keyword.alb_full}} (ALB) now supports `TCP keep alive`. With this setting, the ALB sends TCP-keep-alive packets to both client and back-end servers every five seconds. For more information, refer to [Advanced traffic management](/docs/vpc?topic=vpc-advanced-traffic-management#tcp-keep-alive).

New monitoring metrics
:   {{site.data.keyword.cloud}} {{site.data.keyword.alb_full}} (ALB) now has additional monitoring metrics to help track the traffic and usage patterns for your load balancers. These new metrics can provide insight about peak traffic hours, usage dropoffs, and overall usage patterns. The new metrics are:

   * Total number of HTTP/HTTPS requests received by the back-end
   * Average response time for HTTP/HTTPS requests
   * Count of responses with the HTTP 2xx back-end response code
   * Count of responses with the HTTP 3xx back-end response code
   * Count of responses with the HTTP 4xx back-end response code
   * Count of responses with the HTTP 5xx back-end response code

   For more information, refer to [Monitoring Application Load Balancer for VPC metrics](/docs/vpc?topic=vpc-monitoring-metrics-alb).

Private network load balancers
:   {{site.data.keyword.cloud}} {{site.data.keyword.nlb_full}} (NLB) now supports the creation of private network load balancers. A private NLB is a load balancer only accessible from within the VPC network and/or where the client has reachability to the VPC network (for example, through Direct Link or a transit gateway). To create private load balancers, you must have a dedicated subnet with no custom routes configured for the subnet. For information on creating a private NLB, refer to [Creating a network load balancer for VPC](/docs/vpc?topic=vpc-nlb-ui-creating-network-load-balancer).

### 19 March 2021
{: #vpc-mar1921}
{: release-note}

Virtual server instance console
:   The virtual server instance console feature is now generally available in the following regions: Dallas, Frankfurt, London, Osaka, and Washington DC. For more information, see [Accessing virtual server instances by using VNC or serial consoles](/docs/vpc?topic=vpc-vsi_is_connecting_console).

Bring you own license (GA)
:   You can bring your own license (BYOL) when you import a RedHat Enterprise Linux (RHEL) or Windows&reg; custom image to IBM Cloud VPC. Because these images are registered and licensed by you, you maintain control over your licenses and with no additional cost. Acquisition and activation of the license is between you and and the OS vendor. For more information, see [Bring your own license](/docs/vpc?topic=vpc-byol-vpc-about).

Dedicated hosts (GA)
:   Dedicated hosts are available in all regions. Use a dedicated host to carve out a single-tenant compute node for {{site.data.keyword.vpc_short}}. For more information, see [Creating dedicated hosts and groups](/docs/vpc?topic=vpc-creating-dedicated-hosts-instances)

### 12 March 2021
{: #vpc-mar1221}
{: release-note}

New profiles
:   The Balanced, Compute, and Memory profile families now include three new profiles with 64, 96, and 128 vCPUs. Profiles with 64 or more vCPUs are deployed exclusively on 2nd generation Intel Xeon Platinum 8260 (Cascade Lake) running at a base speed of 2.4 GHz and an all-core turbo frequency of 3.1 GHz.

VPN for VPC
:   For high-security standards, VPN now supports SHA-512 authentication and Diffie-Hellman Group 19.

:   Gateway private IP addresses are now visible for gateway members.

### 05 March 2021
{: #vpc-mar0521}
{: release-note}

Instance resize (Beta)
:   Beta users can now resize a virtual server instance by selecting a different profile to assign to the instance. Profiles are a combination of instance attributes, such as the number of vCPUs, amount of RAM, network bandwidth, and more that define the size and capablilities of the virtual server instance. For more information, see [Resizing an instance (Beta)](/docs/vpc?topic=vpc-resizing-an-instance).

Snapshots for VPC (Beta)
:   Select Beta users can now create snapshots of their Block Storage boot and data volumes attached to a running virtual server instance. These snapshots can be used to create new volumes, which function like the original volume. For more information, see [About Snapshots for VPC (Beta)](/docs/vpc?topic=vpc-snapshots-vpc-about).

UI enhancement
:   When creating or editing a VPN policy (IKE or IPsec), a new authentication option is available, SHA512. Additionally, a new Diffie-Hellman key exchange group is supported: group 19.

## February 2021
{: #vpc-feb21}

### 25 February 2021
{: #vpc-feb2521}
{: release-note}

Dedicated hosts
:   You can now use dedicated hosts to carve out a single-tenant compute node for {{site.data.keyword.vpc_short}} in the following regions: Dallas, Washington DC, London, Tokyo, and Osaka. For more information, see [Creating dedicated hosts and groups](/docs/vpc?topic=vpc-creating-dedicated-hosts-instances).

Application load balancer security group integration
:   For enhanced security, application load balancers can now be associated with security groups. You can specify one or more security groups when you create the application load balancer, and associate security groups with your existing application load balancers. For more information, see [Integrating an IBM Cloud Application Load Balancer for VPC with security groups](/docs/vpc?topic=vpc-alb-integration-with-security-groups).

UI enhancement
:   On the New virtual server for VPC page, selected SSH keys persist if you leave the page and then return to it during a single logged in session. If you log out or switch your account, the selected SSH keys change.

VPC address prefixes are no longer restricted to RFC-1918 addresses
:   You must now configure VPCs that use both non-RFC-1918 addresses and have public connectivity (floating IPs or public gateways) using a custom route that contains the new `Delegate-VPC` action. You must specify this action for destination CIDRs that are non-RFC-1918 compliant and also outside of the VPC, such as for destinations that are reachable through Direct Link, Transit Gateway, or VPC classic access. For more information about when to use the `Delegate-VPC` action, see [Routing considerations for IANA-registered IP assignments](/docs/vpc?topic=vpc-interconnectivity#routing-considerations-iana).

### 18 February 2021
{: #vpc-feb1821}
{: release-note}

UI enhancement
:   You can now provision a VPN gateway or load balancer without first creating a VPC. If you don't have an existing VPC you can provision the VPN gateway or load balancer in the default VPC. The new VPN gateway or load balancer is created along with a default VPC that includes a default security group, access control list, and subnet.

### 07 February 2021
{: #vpc-feb0721}
{: release-note}

Virtual server instance console (Beta)
:   You can now access your virtual server by connecting to a VNC or serial console. This feature provides a quick-and-easy way for you to interact with the virtual server without using a Secure Shell. This is a Beta feature that requires special approval. Contact your IBM Sales representative if you are interested in getting access. For more information, see [Accessing virtual server instances by using VNC or serial consoles (Beta)](/docs/vpc?topic=vpc-vsi_is_connecting_console)

## January 2021
{: #vpc-jan21}

### 26 January 2021
{: #vpc-jan2621}
{: release-note}

New region
:   The Osaka region endpoint is now in service at `https://jp-osa.iaas.cloud.ibm.com`. For more information, see [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region). See also [Endpoint URLs](/apidocs/vpc#endpoint-url) in the {{site.data.keyword.vpc_short}} API.

### 11 January 2021
{: #vpc-jan1121}
{: release-note}

Customer-managed encryption (GA)
:   Customer-managed encryption, which supports deleting or disabling customer root keys and provides new statuses, is now available in the Washington DC (WDC) region. All VPC service regions now support this feature.

## December 2020
{: #vpc-dec20}

### 22 December 2020
{: #vpc-dec2220}
{: release-note}

Customer-managed encryption (GA)
:   For Block Storage volumes and encrypted custom images, deleting or disabling a customer root key (CRK) is now managed by these VPC services. When you delete a root key, the resources become unusable for normal operations. A new `unusable` status and reason code `encryption_key_deleted` or `encryption_key_disabled` has been added to the API for `GET / volumes` and `GET / image` methods. These statuses also appear in the CLI and UI. For more information, see [Disabling root keys](/docs/vpc?topic=vpc-vpc-encryption-managing#byok-disable-root-keys) and [Deleting root keys](/docs/vpc?topic=vpc-vpc-encryption-managing#byok-delete-root-keys). For information on key states and resource statuses, see [User actions that impact root key states and resource status](/docs/vpc?topic=vpc-vpc-encryption-managing#byok-root-key-states).

:   The Washington D.C. multi-zone region will be enabled in January 2021. This feature is available in all other multi-zone regions.


### 18 December 2020
{: #vpc-dec1820}
{: release-note}

Bring you own license (Beta)
:   You can now bring your own license (BYOL) when you import a custom image to {{site.data.keyword.vpc_short}}. This is a Beta feature that is available for evaluation and testing purposes. Contact your IBM Sales representative if you are interested in getting access. For more information, see [Bring your own license (Beta)](/docs/vpc?topic=vpc-byol-vpc-about).

### 17 December 2020
{: #vpc-dec1720}
{: release-note}

Checksum (SHA256) for imported images (Beta)
:   Now when you import a custom image, you can view the checksum that's generated for the image when it is imported to {{site.data.keyword.vpc_short}}. If you generate a checksum locally for your image before importing it, you can compare the two checksums to ensure that they are identical. For more information, see [Validating a custom image after importing (Beta)](/docs/vpc?topic=vpc-managing-images#validate-custom).

UI enhancements
:   Default boot volume names are now appended with a millisecond timestamp.

### 11 December 2020
{: #vpc-dec1120}
{: release-note}

VPN logging and auditing
:   The ability to monitor and audit your VPNs has been added to VPN for VPC. For more information, see [Using IBM Log Analysis to view VPN logs](/docs/vpc?topic=vpc-using-log-analysis-to-view-vpn-logs).

### 01 December 2020
{: #vpc-dec0120}
{: release-note}

New SDK
:   The [Node SDK](/apidocs/vpc?code=node) is now generally available.

## November 2020
{: #vpc-nov20}

### 20 November 2020
{: #vpc-nov2020}
{: release-note}

Support for ingress routing
:   Ingress routing is included as part of custom routing tables, released on 30 October 2020. Ingress routing enables you to customize routes on incoming traffic to a VPC from traffic sources external to the VPC's availability zone (IBM Cloud Direct Link, IBM Cloud Transit Gateway, or another availability zone in the same VPC). For more information, see [About routing tables and routes](/docs/vpc?topic=vpc-about-custom-routes).

Support for datapath log forwarding with Log Analysis
:   Datapath log forwarding with {{site.data.keyword.la_full_notm}} is now available for IBM Cloud Application Load Balancer for VPC. Data and health check logs are valuable for debugging, analysis, and maintenance purposes. With the datapath logging feature enabled, your load balancer forwards these logs to your account's {{site.data.keyword.la_full_notm}} dashboard. For more information, see [Datapath log forwarding with Log Analysis](/docs/vpc?topic=vpc-datapath-logging#datapath-logging).

UI enhancements
:   You can now provision a VPC from the within the New virtual server for VPC page.

### 12 November 2020
{: #vpc-nov1220}
{: release-note}

Route-based virtual private network (VPN) gateways for VPC
:   Use route-based VPN for VPC gateways to manage large, on-premises or cloud-based networks that require the ability to statically route network and connectivity over a secure, encrypted connection. VPN for VPC provides UI, CLI, and API support in all MZRs. For more information, see [About VPN gateways](/docs/vpc?topic=vpc-using-vpn).

UI enhancements:
:   You can now provision virtual server instances without first creating a VPC. Your virtual server instance is created in a default VPC.
:   The refresh data option is removed from all details pages. Instead, users can refresh by using the browser refresh.

### 06 November 2020
{: #vpc-nov0620}
{: release-note}

Proxy protocol support for IBM Cloud Application Load Balancer for VPC (ALB)
:   Proxy protocol provides a way to carry client information across proxies by appending it to the traffic your load balancer sends to the back-end servers. It also allows you to use listeners if incoming traffic contains proxy protocol information set by an intermediate proxy in between the client and your load balancer. See [Enabling proxy protocol](/docs/vpc?topic=vpc-advanced-traffic-management#proxy-protocol-enablement) for details.

### 02 November 2020
{: #vpc-nov0220}
{: release-note}

Custom routing tables and routes (GA)
:   {{site.data.keyword.cloud_notm}} Custom Routes for VPC enables you to configure and control the routing behavior of traffic within your VPC. This functionality provides the ability to explicitly manage traffic between and among subnets within a VPC; thereby, supporting network topologies that incorporate the use of virtual appliances, such as firewalls. This service also allows {{site.data.keyword.cloud_notm}} to continue to develop and deliver advanced features and capabilities for our {{site.data.keyword.cloud_notm}} services. For more information, see [About routing tables and routes](/docs/vpc?topic=vpc-about-custom-routes).

IP spoofing (GA)
:   IP spoofing allows users to enable or disable the IP spoofing check on virtual server instances. This facilitates the traffic flow configured with custom routes functionality. For more information, see [About IP spoofing](/docs/vpc?topic=vpc-ip-spoofing-about).

## October 2020
{: #vpc-oct20}

### 30 October 2020
{: #vpc-oct3020}
{: release-note}

Virtual private endpoint gateways (GA)
:   {{site.data.keyword.cloud_notm}} Virtual Private Endpoints (VPE) for VPC is now generally available. This service enables you to connect to supported {{site.data.keyword.cloud_notm}} services from your VPC network by using the IP addresses of your choosing, allocated from a subnet within your VPC. For more information, see [About virtual private endpoint gateways](/docs/vpc?topic=vpc-about-vpe).

### 1 October 2020
{: #vpc-oct0120}
{: release-note}

Encrypted images (GA)
:   Support for encrypting and importing a custom image is now generally available. For more information, see [Creating an encrypted custom image](/docs/vpc?topic=vpc-create-encrypted-custom-image).

UI enhancements
:   Improved name validation when an existing resource name is specified for a new resource

:   New way to view and select instance profiles in a side window when you provision an instance

:   Enhanced security group details page to include attached network interfaces, with a link to manage the interfaces

## September 2020
{: #vpc-sep20}

### 24 September 2020
{: #vpc-sep2420}
{: release-note}

New SDK
:   The [Java SDK](/apidocs/vpc?code=java) is now generally available.

### 04 September 2020
{: #vpc-sep0420}
{: release-note}

Network load balancer (GA)
:   The {{site.data.keyword.cloud_notm}} Network load balancer (NLB) for VPC is now generally available. Use the network load balancer to distribute traffic among multiple server instances within the same region of your VPC. For more information, see [About IBM Cloud Network Load Balancer for VPC](/docs/vpc?topic=vpc-network-load-balancers).

### 01 September 2020
{: #vpc-sep0120}
{: release-note}

New region
:   The Sydney region endpoint is now in service at `https://au-syd.iaas.cloud.ibm.com`. For more information, see [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region). See also [Endpoint URLs](/apidocs/vpc#endpoint-url) in the {{site.data.keyword.vpc_short}} API.

## August 2020
{: #vpc-aug20}

### 27 August 2020
{: #vpc-aug2720}
{: release-note}

Large profiles (GA):
:   The following two 48-core profiles are now generally available:

    * cx2-48x96
    * mx2-48x384

   For more information, see [Profiles](/docs/vpc?topic=vpc-profiles).

UI enhancements
:   New design for the VPC Overview page and generation switcher
:   Updated load balancer page to include auto scale enablement

### 24 August 2020
{: #vpc-aug2420}
{: release-note}

Auto scale (GA)
:   Auto scale is now generally available. Use auto scale to improve performance and costs by dynamically creating virtual server instances to meet the demands of your environment. For more information, see [Creating an instance group for auto scaling](/docs/vpc?topic=vpc-creating-auto-scale-instance-group).

### 12 August 2020
{: #vpc-aug1220}
{: release-note}

New image support
:   {{site.data.keyword.redhat_full}} Enterprise Linux 8 is now available in all regions.

### 07 August 2020
{: #vpc-aug0720}
{: release-note}

Virtual private endpoints (Beta)
:   Endpoint gateways for {{site.data.keyword.cloud_notm}} VPC are now available in a limited, allow-listed beta. Use virtual private endpoints (VPE) to connect to supported {{site.data.keyword.cloud_notm}} services from your VPC network by using the IP addresses of your choosing, which is allocated from a subnet within your VPC. For more information, see [About Virtual Private Endpoints for VPC (Beta)](/docs/vpc?topic=vpc-about-vpe).

UI enhancements
:   Improved name validation on provisioning pages
:   Eliminated polling on data tables
:   Enhanced data tables

## July 2020
{: #vpc-jul20}

### 30 July 2020
{: #vpc-jul3020}
{: release-note}

Larger volume capacity for Block Storage for VPC (Beta)
:   Provision volumes with capacities greater than 2 TB and up to 16 TB, depending on the profile you selected. See [Expanded Capacity IOPS Tiers (Beta)](/docs/vpc?topic=vpc-block-storage-profiles#tiers).

Expanding Block Storage for VPC volume capacity
:   Expand the size of new Block Storage volumes that you create and attach to a virtual server instance on Gen 2 Compute resources. Indicate capacity in GB increments up to 16 TB, depending on your volume profile limits. For more information, see [Expanding Block Storage volume capacity (Beta)](/docs/vpc?topic=vpc-expanding-block-storage-volumes).

Encrypted images (Beta)
:   Import an encrypted custom image with beta support for the feature. For more information, see [Creating an encrypted custom image (Beta)](/docs/vpc?topic=vpc-create-encrypted-custom-image).

New SDK
:   The [Python SDK](/apidocs/vpc?code=python) is now generally available.

### 23 July 2020
{: #vpc-jul2320}
{: release-note}

Customer-managed encryption for Block Storage for VPC (GA)
:   Customer-managed encryption is now available for protecting boot and data volumes on Gen 2 compute resources. Import your own root keys to the cloud or create a key using Key Protect or Hyper Protect Crypto Services. Then, use your key to secure your data. For more information, see [Customer-managed encryption](/docs/vpc?topic=vpc-vpc-encryption-about#vpc-customer-managed-encryption).

Flow logs for VPC (GA)
:   FLow logs for {{site.data.keyword.cloud_notm}} VPC are now generally available. This service enables the collection, storage, and presentation of information about IP traffic flowing to and from network interfaces within a VPC. For more information, see [About IBM Cloud Flow Logs for VPC](/docs/vpc?topic=vpc-flow-logs).

### 16 July 2020
{: #vpc-jul1620}
{: release-note}

New region
:   The Tokyo region endpoint is now in service at `https://jp-tok.iaas.cloud.ibm.com`. For more information, see [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region).

"Add to estimate" capability updates
:   Added support for itemized virtual server pricing in the Add to estimate capability.

### 03 July 2020
{: #vpc-jul0320}
{: release-note}

Network load balancer (Beta)
:   Network load balancers are available in a limited beta. Use network load balancers to distribute traffic among multiple server instances within the same region of your VPC. For more information, see [Load balancers overview](/docs/vpc?topic=vpc-nlb-vs-elb) and [About network load balancers](/docs/vpc?topic=vpc-network-load-balancers).

VPN for VPC update
:   Access VPN monitoring metrics by using [Monitoring VPN for VPC metrics](/docs/vpc?topic=vpc-sysdig-monitoring-metrics).

## June 2020
{: #vpc-jun20}

### 26 June 2020
{: #vpc-jun2620}
{: release-note}

Dedicated hosts (Beta)
:   In a limited beta, use dedicated hosts to carve out a single-tenant compute node. For more information, see [Creating dedicated hosts and groups (Beta)](/docs/vpc?topic=vpc-creating-dedicated-hosts-instances).

### 19 June 2020
{: #vpc-jun1920}
{: release-note}

Updated custom images information
:   A new [Planning for custom images](/docs/vpc?topic=vpc-planning-custom-images) checklist is available. The procedure for migrating a virtual server instance from classic infrastructure to {{site.data.keyword.cloud_notm}} VPC is enhanced. For more information, see [Migrating a virtual server from the classic infrastructure](/docs/vpc?topic=vpc-migrate-vsi-to-vpc).

UI Enhancements
:   Added pagination for the security groups list table

:   On the VPN Provision page, select a subnet from a table or create subnets

:   New "upgrade pending" button if a user account is pending upgrade

New SDK
:   The [Go SDK](/apidocs/vpc?code=go) is now generally available.

### 02 June 2020
{: #vpc-jun0220}
{: release-note}

IBM Cloud Virtual Servers for VPC on POWER service is deprecated
:   As of 02 June 2020, you cannot provision new instances. Any instance that is still provisioned as of 22 August 2020 will be deleted. For more information, see the [End of Service Announcement for Virtual Servers for VPC on POWER](https://www.ibm.com/cloud/blog/announcements/end-of-service-announcement-for-virtual-servers-for-vpc-on-power).

## May 2020
{: #vpc-may20}

### 21 May 2020
{: #vpc-may2120}
{: release-note}

Auto scale for VPC (Beta)
:   In this limited beta, use auto scale to improve performance and costs by dynamically creating virtual server instances to meet the demands of your environment. For more information, see [Creating an instance group for auto scaling (Beta)](/docs/vpc?topic=vpc-creating-auto-scale-instance-group).

### 15 May 2020
{: #vpc-may1520}
{: release-note}

Load balancer for VPC update
:   Back-end encryption (HTTPS for back-end pool) is now supported. See [Using load balancers for VPC](/docs/vpc?topic=vpc-load-balancers) for details.

### 1 May 2020
{: #vpc-may0120}
{: release-note}

Customer-managed encryption (Beta)
:   Customer-managed encryption (BYOK) is available in beta. Bring your own encryption keys and store the keys in Key Protect or Hyper Protect Crypto Services within VPC. Use BYOK to encrypt your VPC-enabled Block Storage at the volume level by using your own keys. For more information, see [Creating virtual server instances with customer-managed encryption (Beta)](/docs/vpc?topic=vpc-creating-instances-byok).

Flow logs (Beta)
:   Flow logs are now available in beta. Use flow logs to collect, store, and present the Internet Protocol (IP) traffic flowing to and from networks within your VPC. For more information, see [About flow logs (Beta)](/docs/vpc?topic=vpc-flow-logs).

UI enhancement
:   Create a new subnet directly from the page where you create a new instance.

## April 2020
{: #vpc-apr20}

### 22 April 2020
{: #vpc-apr2220}
{: release-note}

New Frankfurt region
:   The Frankfurt region endpoint (eu-de) is now in service at `http://eu-de.iaas.cloud.ibm.com`. For more information, see [Endpoint URLs](/apidocs/vpc#endpoint-url) in the {{site.data.keyword.vpc_short}} API. See also [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region).

### 17 April 2020
{: #vpc-apr1720}
{: release-note}

Documentation correction
:   {{site.data.keyword.cloud_notm}} interprets volume capacity units in gibibytes, but the API documentation used gigabytes. This issue is now resolved in the documentation.

### 03 April 2020
{: #vpc-apr0320}
{: release-note}

Load balancer for VPC update
:   Access load balancer monitoring metrics (throughput, active connections, connection rate) using [IBM Cloud Monitoring](/docs/vpc?topic=vpc-monitoring-metrics).

   The following cipher suites are supported for load balancer HTTPS listeners:

   - `TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384`
   - `TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256`
   - `TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256`
   - `TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384`
   - `TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256`
   - `TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256`

## March 2020
{: #vpc-mar20}

### 27 March 2020
{: #vpc-mar2720}
{: release-note}

{{site.data.keyword.mon_full_notm}} monitoring
:   Monitor virtual server instances using {{site.data.keyword.mon_full_notm}}. Use the new **Add monitoring** button on the instance's **Monitoring** page to provision an instance of the monitoring service. If a monitoring instance is already provisioned for the region, use the **Launch monitoring** button to view metrics associated with the instance. For more information, see [Monitoring metrics](/docs/vpc?topic=vpc-sysdig-monitoring-metrics).

Updated styling
:   VPC pages in {{site.data.keyword.IBM_notm}} console now use [Carbon 10](https://www.carbondesignsystem.com/){: external}, the IBM open source design system, which improves consistency and quality.

### 09 March 2020
{: #vpc-mar0920}
{: release-note}

IBM virtual servers for VPC on POWER
:   POWER-based instances are now generally available. For more information, see the following resource:

   - [Profiles](/docs/vpc?topic=vpc-profiles)

### 02 March 2020
{: #vpc-mar0220}
{: release-note}

New London region
:   The London region endpoint (eu-gb) is now in service at `http://eu-gb.iaas.cloud.ibm.com`. For more information, see [Endpoint URLs](/apidocs/vpc#endpoint-url) in the {{site.data.keyword.vpc_short}} API. See also [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region).

UI enhancement
:   A new public gateway details page is available. For more information about public gateways, see [external connectivity](/docs/vpc?topic=vpc-about-networking-for-vpc#external-connectivity).

## February 2020
{: #vpc-feb20}

### 14 February 2020
{: #vpc-feb1420}
{: release-note}

New VPC network services (GA)
:   The following VPC network services are now generally available:

   - **Virtual private network (VPN):** Use VPN to set up an IPsec site-to-site tunnel between your VPC and your on-premises private network or another VPC. For details, see [Using VPN](/docs/vpc?topic=vpc-using-vpn).
   - **Load balancers:** Create public and private load balancers to distribute traffic among multiple server instances within the same region of your VPC. For details, see [Using load balancers](/docs/vpc?topic=vpc-load-balancers).

### 13 February 2020
{: #vpc-feb1320}
{: release-note}

Red Hat Enterprise Linux (RHEL) and Windows stock images are now available
:   Provision an instance that uses an RHEL image or a Windows&reg; image in the Dallas region. For more information, see [Images](/docs/vpc?topic=vpc-about-images).

### 10 February 2020
{: #vpc-feb1020}
{: release-note}

API change notification
:   We have temporarily suspended API support for creating new instances from an existing boot volume. For more information, see t[API change log](/docs/vpc?topic=vpc-api-change-log).

### 03 February 2020
{: #vpc-feb0320}
{: release-note}

IBM virtual servers for VPC on POWER (Beta)
:   The beta is now open to anyone interested, no signup necessary. For more information, see the following resources:

   * [Profiles](/docs/vpc?topic=vpc-profiles)

Red Hat Enterprise Linux (RHEL) and Windows stock images are now available
:   Provision an instance that uses an RHEL image or a Windows&reg; image in the Washington DC region. For more information, see [Images](/docs/vpc?topic=vpc-about-images).

UI enhancements
:   The modals for provisioning and attaching a public gateway and for creating an SSH key are now replaced with a redesigned side pane.

## January 2020
{: #vpc-jan20}

### 10 January 2020
{: #vpc-jan1020}
{: release-note}

New Washington DC region
:   The Washington DC region endpoint (us-east) is now in service at `http://us-east.iaas.cloud.ibm.com`. For more information, see [Endpoint URLs](/apidocs/vpc#endpoint-url) in the {{site.data.keyword.vpc_short}} API. See also [Creating a VPC in a different region](/docs/vpc?topic=vpc-creating-a-vpc-in-a-different-region).

CLI plug-in release 0.5.10
:   For more information, see [VPC CLI reference](/docs/vpc?topic=vpc-infrastructure-cli-plugin-vpc-reference).
    * You now have an Example section in command help for creating and updating commands. Example: `ibmcloud is help instance-create`, `ibmcloud is help instance-update`, or `ibmcloud is help volume-create`.
    * Use the _resource group filter_ in list commands. Example: `ibmcloud is vpcs --resource-group-name Littleton`.
    * JSON output format support for the `ibmcloud is target --json` command.
    * `ipv4` and `primary-network-interface` options for `instance-create`. Options help specify the primary private IP for the primary network interface when you create an instance.

## December 2019
{: #vpc-dec19}

### 09 December 2019
{: #vpc-dec0919}
{: release-note}

IBM virtual servers for VPC on POWER (Beta)
:   Create POWER-based instances for all virtual server families, including the addition of the GPU family (for POWER only). For more information, see [Profiles](/docs/vpc?topic=vpc-profiles).

UI enhancement
:   On the VPC details page, a new section is available to view source IP addresses for any cloud service endpoints you enabled. For more information, see [Service endpoints](/docs/vpc?topic=vpc-service-endpoints-for-vpc).

CLI plug-in release 0.5.9
:   Target a specific resource group by using the '[-g YOUR_GROUP]' command option. If you specify the target resource group by using the `ibmcloud target [-g YOUR_GROUP]`command, the output displays only VPC resources inside of the specified resource group. This update also introduces enhancements to some of the commands for `get` and `list`, showing more detail for your VPC, instances, and instance profiles. For more information, see [VPC CLI reference](/docs/vpc?topic=vpc-infrastructure-cli-plugin-vpc-reference).

### 02 December 2019
{: #vpc-dec0219}
{: release-note}

Access control lists
:   Use an access control list (ACL) to control all incoming and outgoing traffic in {{site.data.keyword.vpc_full}}. For more information, see [Setting up network ACLs](/docs/vpc?topic=vpc-using-acls).

## November 2019
{: #vpc-nov19}

### 14 November 2019
{: #vpc-nov1419}
{: release-note}

VPC layout
:   View resources that are associated with a VPC in the {{site.data.keyword.cloud_notm}} console. For more information, see [Viewing resources associated with a VPC](/docs/vpc?topic=vpc-creating-a-vpc-using-the-ibm-cloud-console#vpc-layout).

### 07 November 2019
{: #vpc-nov0719}
{: release-note}

Load balancer (Beta)
:   Use the {{site.data.keyword.cloud}} Load balancer for VPC service to distribute traffic among multiple server instances within the same region of your VPC. For more information, see [Using load balancers (Beta)](/docs/vpc?topic=vpc-load-balancers).

VPN (Beta)
:   Use the {{site.data.keyword.cloud}} VPN for VPC service to securely connect your VPC to another private network. For more information, see [Using VPN (Beta)](/docs/vpc?topic=vpc-using-vpn).

## October 2019
{: #vpc-oct19}

### 31 October 2019
{: #vpc-oct3119}
{: release-note}

Classic access
:   Set up access from a VPC to your {{site.data.keyword.cloud}} Classic infrastructure, including Direct Link connectivity. For more information, see [Setting up access to classic infrastructure](/docs/vpc?topic=vpc-setting-up-access-to-classic-infrastructure).

Advanced routing
:   Control the flow of network traffic in your VPC by configuring VPC routes. For more information, see [About routing tables and routes](/docs/vpc?topic=vpc-about-custom-routes).

## June 2019
{: #vpc-june19}

### 04 June 2019
{: #vpc-jun-0419}
{: release-note}

Introducing {{site.data.keyword.vpc_short}}
:   {{site.data.keyword.vpc_full}} is now generally available in the Dallas, Frankfurt, and Tokyo regions. For more information, see [{{site.data.keyword.vpc_short}}](https://www.ibm.com/cloud/blog/introducing-ibm-cloud-virtual-private-cloud).{: external}
