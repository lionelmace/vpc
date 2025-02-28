---

copyright:
  years: 2022, 2023
lastupdated: "2023-09-29"

keywords: Backup for VPC, backup service, backup plan, backup policy, restore, restore volume, restore data, view backup lists,

subcollection: vpc

---

{{site.data.keyword.attribute-definition-list}}

# Viewing backup jobs
{: #backup-view-policy-jobs}

When backup snapshots are being created or deleted by a backup policy, you can view the backup job status. Use the UI, CLI, or API to list all backup jobs for a policy and view job details.
{: shortdesc}

## View backup jobs in the UI
{: #backup-view-jobs-ui}
{: ui}

List all backup jobs. Select a backup job and review its details.

### View a list of backup jobs in the UI
{: #backup-view-jobs-list-ui}

From the backup policy details page, you can list all backup jobs for that policy. The jobs are listed with the oldest one first. Backup jobs show all backups that were created by the backup policy for the selected region.

1. In the [{{site.data.keyword.cloud_notm}} console](/login){: external}, go to the **menu ![menu icon](../../icons/icon_hamburger.svg) > VPC Infrastructure > Storage > Backup policies**.

2. Click the **Backup jobs** tab. Table 1 describes the information on the Backup jobs page.

| Field | Description |
|-------|-------------|
| Job ID | It's the auto-generated ID of the backup job. |
| Job status | It's the status of the backup job, either `running`, `completed`, or `failed`. |
| Plan | The backup plan that triggered the backup. Hover over the plan name for a summary of the plan. |
| Job type | When a backup is being created, it shows `creation`. When a backup is being deleted, it shows `retention`.|
| Job started | Date and time of when the job began. |
| Job completed | Date and time of when the job was finished. |
| Snapshot | The snapshot (backup) that was created when the backup job finishes. Click the name to see the details in the side panel. |
| Source | Source volume from which the backup was created. Click the volume name to see its details. |
{: caption="Table 1. Information provided by the list of backup jobs for the backup policy" caption-side="bottom"}

### View snapshots that were created by a backup job in the UI
{: #backup-view-snap-backup-ui}

From the list of backup jobs, click the name of a snapshot. A side panel provides snapshot details (Table 2).

| Field | Description |
|-------|-------------|
| Status | The status of the snapshot, such as _Stable_. For a list of snapshot statuses, see [Snapshot statuses](/docs/vpc?topic=vpc-snapshots-vpc-manage&interface=ui#snapshots-vpc-status). |
| Name | The name of the backup policy that created the snapshot. You can change the backup policy settings by clicking the pencil icon. For more information, see [Managing backup policies](/docs/vpc?topic=vpc-backup-service-manage). |
| Tags |  User tags inherited from the source volume when the snapshot was created. Click the pencil icon to more user tags.|
| ID | GUID of the snapshot. |
| Bootable | It indicates whether the snapshot was created from a boot volume. |
| CRN | Cloud resource name of the snapshot. |
| Created | The date and time of when that the snapshot resource creation process started. |
| Captured | The date and time of when this snapshot was taken. If the field is empty, then the snapshot is not yet captured or the snapshot was created before this feature was introduced (January 2022). |
| Size | Size in GBs of the snapshot, it is inherited from the source volume. |
| Source Volume | Source volume from which the first snapshot was taken. Click the link for volume details. If the volume was deleted, the name appears without a link. |
| Encryption | Either provider-managed or customer-managed. |
{: caption="Table 2. Snapshot details side panel" caption-side="bottom"}

## View backup jobs from the CLI
{: #backup-view-jobs-cli}
{: cli}

You can view a list of backup jobs by specifying the ID or name of the backup policy. You can also see details of a backup job with the ID of the backup job.

### View a list of backup jobs from the CLI
{: #backup-view-jobs-list-cli}

Run the `backup-policy-jobs` command to view the backup jobs for your backup snapshots. Status indicates when backup snapshots are being created, failed completion, or succeeded completion.

```text
ibmcloud is backup-policy-jobs POLICY [--volume VOLUME] [--snapshot SNAPSHOT] [--snapshot-crn SNAPSHOT_CRN] [--status failed | running | succeeded] [--plan PLAN] [--output JSON] [-q, --quiet]
```
{: pre}

In the first example, the name of the backup policy is used to list the jobs of that backup policy.

```sh
cloudshell:~$ ibmcloud is backup-policy-jobs new-policy-23
Listing jobs of backup policy new-policy-23 under account Test Account as user test.user@ibm.com...
ID                                          Auto delete   Auto delete after   Completed at                Created at                  Job type   Status   
r138-25828175-2b51-4247-ba01-79c538f68282   true          15                  2023-02-23T20:12:37+00:00   2023-02-23T20:12:14+00:00   creation   succeeded   
r138-57028109-4702-443a-891b-31cac565546c   true          15                  2023-02-22T20:12:44+00:00   2023-02-22T20:12:25+00:00   creation   succeeded   
r138-d25c915c-3166-436d-b289-68d222297510   true          15                  2023-02-22T15:27:43+00:00   2023-02-22T15:27:20+00:00   creation   succeeded
```
{: screen}

In the second example, the policy is identified by its ID, and the JSON output option is used.

```json
cloudshell:~$ ibmcloud is backup-policy-jobs r138-0521986d-963c-4c18-992d-d6a7a99d115f --output JSON
[
    {
        "auto_delete": true,
        "auto_delete_after": 15,
        "backup_policy_plan": {
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/plans/r138-6f4f08ba-e0bb-470f-bbfb-f3a22aebbfa9",
            "id": "r138-6f4f08ba-e0bb-470f-bbfb-f3a22aebbfa9",
            "name": "my-policy-plan-b",
            "resource_type": "backup_policy_plan"
        },
        "completed_at": "2023-02-23T20:12:37.000Z",
        "created_at": "2023-02-23T20:12:14.000Z",
        "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/jobs/r138-25828175-2b51-4247-ba01-79c538f68282",
        "id": "r138-25828175-2b51-4247-ba01-79c538f68282",
        "job_type": "creation",
        "resource_type": "backup_policy_job",
        "source": {
            "crn": "crn:v1:bluemix:public:is:eu-de-2:a/a123456::volume:r010-18ee3ad3-0b7e-4c3a-ba92-226073696049",
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/volumes/r010-18ee3ad3-0b7e-4c3a-ba92-226073696049",
            "id": "r010-18ee3ad3-0b7e-4c3a-ba92-226073696049",
            "name": "fra-vsi-boot-1645484638000"
        },
        "source_volume": {
            "crn": null,
            "href": null,
            "id": null,
            "name": null
        },
        "status": "succeeded",
        "status_reasons": [],
        "target_snapshot": null,
        "target_snapshots": [
            {
                "crn": "crn:v1:bluemix:public:is:eu-de:a/a123456::snapshot:r138-d9ec292d-c638-46dd-bc4d-d9eb500d2925",
                "href": "https://eu-de.iaas.cloud.ibm.com/v1/snapshots/r138-d9ec292d-c638-46dd-bc4d-d9eb500d2925",
                "id": "r138-d9ec292d-c638-46dd-bc4d-d9eb500d2925",
                "name": "my-policy-plan-b-b2a849936b7c-4200",
                "resource_type": "snapshot"
            }
        ]
    },
    {
        "auto_delete": true,
        "auto_delete_after": 15,
        "backup_policy_plan": {
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/plans/r138-6f4f08ba-e0bb-470f-bbfb-f3a22aebbfa9",
            "id": "r138-6f4f08ba-e0bb-470f-bbfb-f3a22aebbfa9",
            "name": "my-policy-plan-b",
            "resource_type": "backup_policy_plan"
        },
        "completed_at": "2023-02-22T20:12:44.000Z",
        "created_at": "2023-02-22T20:12:25.000Z",
        "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/jobs/r138-57028109-4702-443a-891b-31cac565546c",
        "id": "r138-57028109-4702-443a-891b-31cac565546c",
        "job_type": "creation",
        "resource_type": "backup_policy_job",
        "source": {
            "crn": "crn:v1:bluemix:public:is:eu-de-2:a/a123456::volume:r010-df8ffd90-f2e5-470b-83d7-76e64995a1aa",
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/volumes/r010-df8ffd90-f2e5-470b-83d7-76e64995a1aa",
            "id": "r010-df8ffd90-f2e5-470b-83d7-76e64995a1aa",
            "name": "my-block-vol-test1"
        },
        "source_volume": {
            "crn": null,
            "href": null,
            "id": null,
            "name": null
        },
        "status": "succeeded",
        "status_reasons": [],
        "target_snapshot": null,
        "target_snapshots": [
            {
                "crn": "crn:v1:bluemix:public:is:eu-de:a/a123456::snapshot:r138-27010e09-565d-4852-a21f-fae663cc2720",
                "href": "https://eu-de.iaas.cloud.ibm.com/v1/snapshots/r138-27010e09-565d-4852-a21f-fae663cc2720",
                "id": "r138-27010e09-565d-4852-a21f-fae663cc2720",
                "name": "my-policy-plan-c-69547459d912-4916",
                "resource_type": "snapshot"
            }
        ]
    },
    {
        "auto_delete": true,
        "auto_delete_after": 15,
        "backup_policy_plan": {
            "deleted": {
                "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
            },
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/plans/r138-2129a79a-5629-4069-bf79-7bb0af3b0bd3",
            "id": "r138-2129a79a-5629-4069-bf79-7bb0af3b0bd3",
            "name": "-deleted-7bb0af3b0bd3",
            "resource_type": "backup_policy_plan"
        },
        "completed_at": "2023-02-22T15:27:43.000Z",
        "created_at": "2023-02-22T15:27:20.000Z",
        "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/jobs/r138-d25c915c-3166-436d-b289-68d222297510",
        "id": "r138-d25c915c-3166-436d-b289-68d222297510",
        "job_type": "creation",
        "resource_type": "backup_policy_job",
        "source": {
            "crn": "crn:v1:bluemix:public:is:eu-de-2:a/a123456::volume:r010-df8ffd90-f2e5-470b-83d7-76e64995a1aa",
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/volumes/r010-df8ffd90-f2e5-470b-83d7-76e64995a1aa",
            "id": "r010-df8ffd90-f2e5-470b-83d7-76e64995a1aa",
            "name": "my-block-vol-test1"
        },
        "source_volume": {
            "crn": null,
            "href": null,
            "id": null,
            "name": null
        },
        "status": "succeeded",
        "status_reasons": [],
        "target_snapshot": null,
        "target_snapshots": [
            {
                "crn": "crn:v1:bluemix:public:is:eu-de:a/a123456::snapshot:r138-0290995a-9867-4066-98b4-cb2ebfcaf237",
                "href": "https://eu-de.iaas.cloud.ibm.com/v1/snapshots/r138-0290995a-9867-4066-98b4-cb2ebfcaf237",
                "id": "r138-0290995a-9867-4066-98b4-cb2ebfcaf237",
                "name": "my-policy-plan-a-35b95419d283-41bf",
                "resource_type": "snapshot"
            }
        ]
    }
```
{: screen}

For more information about available command options, see [`ibmcloud is backup-policy-jobs`](/docs/vpc?topic=vpc-vpc-reference#backup-policy-jobs).

### View details of a backup job from the CLI
{: #backup-view-jobs-details-cli}

Run the `backup-policy-jobs` command and specify the ID of the backup policy and backup job to see the job details. Alternatively, you can specify the backup policy name.

```text
ibmcloud is backup-policy-job POLICY JOB_ID [--output JSON] [-q, --quiet]
```
{: pre}

The following example shows the output when you run the command by using the policy name and the job ID as arguments, and the `--output JSON` option.

```json
cloudshell:~$ ibmcloud is backup-policy-job new-policy-23 r138-25828175-2b51-4247-ba01-79c538f68282 --output JSON
{
    "auto_delete": true,
    "auto_delete_after": 15,
    "backup_policy_plan": {
        "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/plans/r138-6f4f08ba-e0bb-470f-bbfb-f3a22aebbfa9",
        "id": "r138-6f4f08ba-e0bb-470f-bbfb-f3a22aebbfa9",
        "name": "my-policy-plan-b",
        "resource_type": "backup_policy_plan"
    },
    "completed_at": "2023-02-23T20:12:37.000Z",
    "created_at": "2023-02-23T20:12:14.000Z",
    "href": "https://eu-de.iaas.cloud.ibm.com/v1/backup_policies/r138-0521986d-963c-4c18-992d-d6a7a99d115f/jobs/r138-25828175-2b51-4247-ba01-79c538f68282",
    "id": "r138-25828175-2b51-4247-ba01-79c538f68282",
    "job_type": "creation",
    "resource_type": "backup_policy_job",
    "source": {
        "crn": "crn:v1:bluemix:public:is:eu-de-2:a/a123456::volume:r010-18ee3ad3-0b7e-4c3a-ba92-226073696049",
        "href": "https://eu-de.iaas.cloud.ibm.com/v1/volumes/r010-18ee3ad3-0b7e-4c3a-ba92-226073696049",
        "id": "r010-18ee3ad3-0b7e-4c3a-ba92-226073696049",
        "name": "fra-vsi-boot-1645484638000"
    },
    "source_volume": {
        "crn": null,
        "href": null,
        "id": null,
        "name": null
    },
    "status": "succeeded",
    "status_reasons": [],
    "target_snapshot": null,
    "target_snapshots": [
        {
            "crn": "crn:v1:bluemix:public:is:eu-de:a/a123456::snapshot:r138-d9ec292d-c638-46dd-bc4d-d9eb500d2925",
            "href": "https://eu-de.iaas.cloud.ibm.com/v1/snapshots/r138-d9ec292d-c638-46dd-bc4d-d9eb500d2925",
            "id": "r138-d9ec292d-c638-46dd-bc4d-d9eb500d2925",
            "name": "my-policy-plan-b-b2a849936b7c-4200",
            "resource_type": "snapshot"
        }
    ]
```
{: screen}

For more information about available command options, see [`ibmcloud is backup-policy-jobs`](/docs/vpc?topic=vpc-vpc-reference#backup-policy-jobs).

## View backup jobs with the API
{: #backup-view-jobs-api}
{: api}

View a list of backup jobs or details of a single backup job with the API.

### View a list of backup jobs with the API
{: #backup-view-jobs-list-api}

Make a `GET /backup_policies/{backup_policy_id}/jobs` request to list all backup jobs of a backup policy.

```sh
curl -X GET\
"$vpc_api_endpoint/v1/backup_policies/{backup_policy_id}/jobs?version=2022-06-22&generation=2"\
   -H "Authorization: $iam_token"
```
{: codeblock}

A successful response looks like the following example.

```json
{
  "first": {
    "href": "https://us-south.iaas.cloud.ibm.com/v1/backup_policies/7241e2a8-601f-11ea-8503-000c29475bed/jobs?limit=20"
  },
  "jobs": [
    {
      "auto_delete": true,
      "auto_delete_after": 90,
      "backup_policy_plan": {
        "deleted": {
          "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
        },
        "href": "https://us-south.iaas.cloud.ibm.com/v1/backup_policies/0fe9e5d8-0a4d-4818-96ec-e99708644a58/plans/4cf9171a-0043-4434-8727-15b53dbc374c",
        "id": "4cf9171a-0043-4434-8727-15b53dbc374c",
        "name": "my-policy-plan",
        "resource_type": "backup_policy_plan"
      },
      "completed_at": "2022-06-23T13:37:11.549Z",
      "created_at": "2022-06-23T13:37:11.549Z",
      "href": "https://us-south.iaas.cloud.ibm.com/v1/backup_policies/0fe9e5d8-0a4d-4818-96ec-e99708644a58/jobs/4cf9171a-0043-4434-8727-15b53dbc374c",
      "id": "4cf9171a-0043-4434-8727-15b53dbc374c",
      "job_type": "creation",
      "resource_type": "backup_policy_job",
      "source_volume": {
        "crn": "crn:v1:bluemix:public:is:us-south-1:a/123456::volume:1a6b7274-678d-4dfb-8981-c71dd9d4daa5",
        "deleted": {
          "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
        },
        "href": "https://us-south.iaas.cloud.ibm.com/v1/volumes/1a6b7274-678d-4dfb-8981-c71dd9d4daa5",
        "id": "1a6b7274-678d-4dfb-8981-c71dd9d4daa5",
        "name": "my-volume"
      },
      "status": "failed",
      "status_reasons": [
        {
          "code": "source_volume_busy",
          "message": "string",
          "more_info": "https://cloud.ibm.com/docs/__TBD__"
        }
      ],
      "target_snapshot": {
        "crn": "crn:v1:bluemix:public:is:us-south:a/123456::snapshot:f6bfa329-0e36-433f-a3bb-0df632e79263",
        "deleted": {
          "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
        },
        "href": "https://us-south.iaas.cloud.ibm.com/v1/snapshots/f6bfa329-0e36-433f-a3bb-0df632e79263",
        "id": "f6bfa329-0e36-433f-a3bb-0df632e79263",
        "name": "my-snapshot",
        "resource_type": "snapshot"
      }
    }
  ],
  "limit": 20,
  "next": {
    "href": "https://us-south.iaas.cloud.ibm.com/v1/backup_policies/7241e2a8-601f-11ea-8503-000c29475bed/jobss?start=9d5a91a3e2cbd233b5a5b33436855ed1&limit=20"
  },
  "total_count": 132
}
```
{: codeblock}

### View details of a backup job with the API
{: #backup-view-jobs-details-api}

Make a `GET /backup_policies/{backup_policy_id}/jobs/{backup_job_id}` request to view details of a backup job, which is specified by ID.

```sh
curl -X GET\
"$vpc_api_endpoint/v1/backup_policies/{backup_policy_id}/jobs{backup_job_id}?version=2022-06-22&generation=2"\
   -H "Authorization: $iam_token"
```
{: codeblock}

A successful response looks like the following example.

```json
{
  "auto_delete": true,
  "auto_delete_after": 90,
  "backup_policy_plan": {
    "deleted": {
      "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
    },
    "href": "https://us-south.iaas.cloud.ibm.com/v1/backup_policies/0fe9e5d8-0a4d-4818-96ec-e99708644a58/plans/4cf9171a-0043-4434-8727-15b53dbc374c",
    "id": "4cf9171a-0043-4434-8727-15b53dbc374c",
    "name": "my-policy-plan",
    "resource_type": "backup_policy_plan"
  },
  "completed_at": "2022-06-30T01:58:32.163Z",
  "created_at": "2022-06-30T01:58:32.163Z",
  "href": "https://us-south.iaas.cloud.ibm.com/v1/backup_policies/0fe9e5d8-0a4d-4818-96ec-e99708644a58/jobs/4cf9171a-0043-4434-8727-15b53dbc374c",
  "id": "4cf9171a-0043-4434-8727-15b53dbc374c",
  "job_type": "creation",
  "resource_type": "backup_policy_job",
  "source_volume": {
    "crn": "crn:v1:bluemix:public:is:us-south-1:a/123456::volume:1a6b7274-678d-4dfb-8981-c71dd9d4daa5",
    "deleted": {
      "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
    },
    "href": "https://us-south.iaas.cloud.ibm.com/v1/volumes/1a6b7274-678d-4dfb-8981-c71dd9d4daa5",
    "id": "1a6b7274-678d-4dfb-8981-c71dd9d4daa5",
    "name": "my-volume"
  },
  "status": "failed",
  "status_reasons": [
    {
      "code": "source_volume_busy",
      "message": "string",
      "more_info": "https://cloud.ibm.com/docs/..."
    }
  ],
  "target_snapshot": {
    "crn": "crn:v1:bluemix:public:is:us-south:a/123456::snapshot:f6bfa329-0e36-433f-a3bb-0df632e79263",
    "deleted": {
      "more_info": "https://cloud.ibm.com/apidocs/vpc#deleted-resources"
    },
    "href": "https://us-south.iaas.cloud.ibm.com/v1/snapshots/f6bfa329-0e36-433f-a3bb-0df632e79263",
    "id": "f6bfa329-0e36-433f-a3bb-0df632e79263",
    "name": "my-snapshot",
    "resource_type": "snapshot"
  }
}
```
{: codeblock}

### Backup job statuses and reason codes
{: #backup-jobs-status}

When you view details of a backup job by making a `GET /backup_policies/{backup_policy_id}/jobs/{backup_job_id}` request, the `status` property indicates whether the job `failed`, is `running`, or `succeeded`. The API also provides status reasons with the following codes:

* `internal_error`: the code indicates an internal error. Contact IBM support if your see this code.
* `snapshot_pending`: the code indicates that a backup snapshot in the `pending` [snapshot lifecycle state](/docs/vpc?topic=vpc-snapshots-vpc-manage&interface=ui#snapshots-vpc-status) cannot be deleted.
* `snapshot_volume_limit`: the code indicates that the [snapshot limit](/docs/vpc?topic=vpc-snapshots-vpc-faqs&interface=ui#faq-snapshot-3) for the source volume is reached.
* `source_volume_busy`: the code indicates that the source volume is busy after multiple retries.


## View backup jobs with Terraform
{: #backup-view-jobs-terraform}
{: terraform}

To use Terraform, download the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in. For more information, see [Getting started with Terraform](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started).
{: requirement}

VPC infrastructure services use a regional specific endpoint, which targets to `us-south` by default. If your VPC is created in another region, make sure to target the right region in the provider block in the `provider.tf` file.

See the following example of targeting a region other than the default `us-south`.

```terraform
provider "ibm" {
  region = "eu-de"
}
```
{: screen}

### View a list of backup jobs with Terraform
{: #backup-view-jobs-list-terraform}

Import the list of a collection of backup jobs as a read-only data source.

```terraform
data "ibm_is_backup_policy_jobs" "example" {
  backup_policy_id = ibm_is_backup_policy.example.id
}
```
{: codeblock}

For more information about the arguments and attributes, see [ibm_is_backup_policy_jobs](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/ibm_is_backup_policy_jobs){: external}.

### View details of a backup job with Terraform
{: #backup-view-jobs-details-terraform}

Import the details of a backup job as a read-only data source. 

```terraform
data "ibm_is_backup_policy_job" "example" {
    backup_policy_id = ibm_is_backup_policy.example.id
    identifier = "r138-25828175-2b51-4247-ba01-79c538f68282"
}
```
{: codeblock}

For more information about the arguments and attributes, see [ibm_is_backup_policy_job](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/ibm_is_backup_policy_job){: external}.

## Next steps
{: #backup-jobs-next-steps}

* [Apply tags to your resources for backups](/docs/vpc?topic=vpc-backup-use-policies).
* [Create more backup policies](/docs/vpc?topic=vpc-backup-policy-create&interface=ui).
* [Restore a volume from a backup snapshot](/docs/vpc?topic=vpc-baas-vpc-restore).
