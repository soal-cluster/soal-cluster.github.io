---
title: Administration
layout: default
---

# Cluster Policies

This page contains useful information for administrators of the SOAL Cluster, including policies for various situations and troubleshooting help.

## Resource usage limits

Each user account has the following resource limits per cluster node: 

- At most 50 CPUs being utilized, where "utilized" means 80% or more utilization.
- At most 250 processes running.
- At most 70% of the node's RAM being utilized.
- At most 70% of the node's swap memory being utilized.

These limits will be enforced via the following policy (TBD):

1. Run a cron job or check via the Hall Monitor script at a reasonable frequency (e.g. at least every 10 minutes and not more than every 30 minutes) to tabulate resource usage per user.
2. If there's a resource overusage twice in a row, send an email to the user and the user's PI, and send a message in #cluster to the user.
3. If resource overusage is still occurring after 12 hours without any communcation from the user indicating that steps are being taken towards resolving the overusage, the user's processes will be killed.

Users should be careful to use the cluster in a thoughtful manner, especially around conference deadlines.

## Onboarding agreement

All users onboarded (including PIs) must certify in an email to Tim Keely that they have completed the following tasks:

1. Read and understood the cluster onboarding document.
2. Joined the `#cluster` Slack channel and turned on @username notifications for it.
3. Read and agreed to respect the cluster resource usage limits (see above).
4. Read and agreed to the storage discontinuation policy (see below).
5. Filled out the relevant Google Form for cluster user addition (TBD).

## Storage discontinuation policy

After users leave Stanford, their data remains on the cluster. To prevent the cluster storage system from being overfilled, we have the following storage discontinuation policy:

1. Ever user on the cluster must have an associated PI (principal investigator). PIs are typically faculty members. The root PI for PIs is Tim Keely. Tim will track PI and user information in a Google Sheets sheet which is shared with the cluster administrators.
2. PIs should notify Tim Keely via email when users leave the cluster.
4. Every month, Tim will sweep through user login history. When a user has not logged in for 2 years, Tim will notify the user and the user's PI that the data in the user's home directory must be copied to another directory within 6 months. Reminders will be sent every month and for the last 3 weeks of the last month. After 6 months, the user's home directory will be deleted.

## Cluster support group

Every fall, the department should send out an email to recruit volunteers for a cluster support group which can perform the following duties:

- Join an informal "cluster leads" group to help new users in the `#cluster` channel.
- Help develop and maintain cluster documentation on this website and interface between users and CTSC.

The group should use the soal-cluster GitHub organization to collaborate.

## User support priorities

When users encounter issues with the cluster, they should contact the following resources in this order:

1. First contact Tim or another knowledgeable person in the `#cluster` channel on Slack.
2. If your issue still isn't resolved, email Michael Kennedy at `mr.kennedy@stanford.edu`. Michael is the support person from CTSC (Client Technology Solutions and Consulting), the group which is responsible for operating the SOAL CLuster.
3. If your issue still isn't resolved, do ONE (not more than one) of the following: (a) create a ServiceNow ticket [here](https://stanford.service-now.com/it_services?id=sc_cat_item&sys_id=ec490b5f876d3950a7a497d83cbb35c1) (b) call the UIT helpdesk and mention "SOAL Cluster" (c) for emergency/after-hours support, call (858)-888-9634 to speak to a CTSC team member directly.

# Troubleshooting

## Connection troubleshooting

When users encounter issues connecting to SOAL, the following questions are usually helpful in resolving the source of the problem:

1. Are you connected via VPN? If not, connect and try again.
2. Can you ping SOAL? If not, there may be an issue with your connection to the internet.
3. Are you in a restricted country? If so, access to SOAL may be unfortunately blocked.
4. Could the cluster be overused? Try checking the `#cluster` channel to see if messages from the Hall Monitor bot are indicating that some node(s) of the cluster is being overused.

