# Azure Availability Set Deployment and Verification

Date: October 15, 2026

Status: Deployment, placement verification, and VM cleanup completed. Screenshot upload pending.

## Objective

Create an availability set with two fault domains and two update domains, deploy two VMs into it, and verify their assigned domains using the Azure portal.

## Lab Environment

| Component | Configuration |
|---|---|
| Cloud platform | Microsoft Azure |
| Resource group | `Luera-Labs` |
| Region | West US 2 |
| Availability set | `LueraAS` |
| Fault domains | 2 |
| Update domains | 2 |
| Managed | Yes |
| VMs | `lueraVM1`, `lueraVM2` |
| Deployment method | Azure portal |

## Deployment

1. Created `LueraAS` with two fault domains and two update domains.
2. Confirmed successful deployment and verified the configuration on the availability set overview.
3. Deployed `lueraVM1` and `lueraVM2` into `LueraAS`.
4. Verified that both VMs were running and recorded their domain assignments.

Configuration screenshot: pending upload to `screenshots/01-availability-set-configuration.jpg`.

## Troubleshooting: Missing Availability Set Option

The newer VM creation layout did not show Availability set in the Availability options dropdown. Standard security and West US 2 were selected, but the option was still absent.

Switched to the original VM creation layout using the option provided in the portal. Availability set became available, allowing selection of `LueraAS`. No CLI was used.

This documents the behavior encountered during this lab; it does not establish a platform-wide cause or limitation.

## Verified Results

| VM | Observed status | Fault domain | Update domain |
|---|---|---|---|
| `lueraVM1` | Running | 0 | 0 |
| `lueraVM2` | Running | 1 | 1 |

Confirmed that the two VMs were assigned to separate fault domains and update domains.

Placement screenshot: pending upload to `screenshots/02-availability-set-two-vms.png`.

## Lessons Learned and Limitations

- Verified actual VM domain assignments rather than assuming placement.
- Switching to the original portal layout resolved the missing selection option in this lab.
- Captured configuration, placement, and cleanup evidence before deleting the VMs.
- This lab verified deployment and placement only. Hardware failure, planned platform maintenance, application redundancy, and automatic failover were not tested.

## Cleanup

Deleted `lueraVM1` and `lueraVM2` after placement verification. Confirmed that `LueraAS` showed zero VMs afterward. Retained the availability set.

Deletion of associated disks, network interfaces, and public IP addresses was not verified.

Cleanup screenshot: pending upload to `screenshots/03-availability-set-cleanup.png`.

## Screenshot Status

The images have not been uploaded to this repository. Upload only sanitized copies. Inline image references will be added after the files are present to avoid broken images.
