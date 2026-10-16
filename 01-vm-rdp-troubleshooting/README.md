# Azure VM Deployment and RDP Troubleshooting

Status: Completed

## Overview and Objectives

In this lab, I created a virtual machine in Microsoft Azure and connected to it from my Mac using Remote Desktop Protocol (RDP). My initial connection attempt was unsuccessful because an existing home firewall rule blocked outbound traffic on port 3389. I updated the firewall policy, validated the connection, and deleted the VM after testing.

Objectives:
- Create a basic Azure virtual machine.
- Establish an RDP connection from a Mac.
- Identify and resolve a firewall restriction affecting connectivity.
- Validate the connection and delete the VM after testing.

## Lab Environment

| Component | Details |
|---|---|
| Cloud platform | Microsoft Azure |
| Virtual machine | `Luera-Labs-VM1` |
| Resource group | `Luera-Labs` |
| Client device | Mac |
| Local network security | Home firewall |
| Connection method | RDP, TCP port 3389 |

## Deployment and Troubleshooting

1. Created a basic Azure virtual machine named `Luera-Labs-VM1` in the `Luera-Labs` resource group.
2. Attempted to connect from my Mac using RDP. The initial connection was unsuccessful.
3. Identified an existing home firewall rule blocking all traffic on port 3389, including outbound RDP connections to the Azure VM.
4. Created an outbound-only allow rule for port 3389. Inbound RDP access to my home network remained blocked.
5. Successfully established an RDP session to the Azure VM after applying the change.

## Results and Lessons Learned

The successful RDP connection after the firewall change confirmed that the outbound restriction had been blocking access.

- My home firewall's outbound policy affected connectivity to the cloud VM.
- In this case, the issue was a local firewall restriction rather than a failed VM deployment.
- Testing immediately after the rule change validated the resolution.

Screenshots were not captured during this lab. The final Azure-side RDP rule configuration and its source restrictions were not recorded.

## Cleanup

Deleted the Azure virtual machine after completing the connection test. Deletion of associated resources, such as disks, network interfaces, or public IP addresses, was not documented.
