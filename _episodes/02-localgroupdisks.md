---
title: "LOCALGROUPDISK"
teaching: 0
exercises: 0
questions:
- "How can I store my grid outputs?"
objectives:
- "Learn how to use LOCALGROUPDISKs."
keypoints:
- "With the proper grid roles, you can use US disk storage for your rucio datasets."
---

Go to the [LCG VOMS page](https://lcg-voms2.cern.ch:8443/voms/atlas):

![image info](./../fig/voms_screenshot.png)

In the "Your groups and roles" section, request membership for the `/atlas/usatlas` role.  It may take a few days to be approved, but once it is then you have access to grid storage in the US!  This means you can store your datasets in US LOCALGROUPDISK endpoints.  This is nice, because:

1. otherwise your user data on the grid will be deleted fairly soon after you make it (on the assumption that you've downloaded it to local storage already).  On the other hand, if it's in a LOCALGROUPDISK, it never expires.
2. the Shared Tier-3's can read data directly from their own LOCALGROUPDISKs, without needing to download the data manually.

Once you have that role, the next step is to request that your favorite datasets be replicated on a LOCALGROUPDISK.  Navigate to the R2D2 page: [https://rucio-ui.cern.ch/r2d2](https://rucio-ui.cern.ch/r2d2/request)

- Log in with your X509 certificate:
![image info](./../fig/rucio_1.png)

- Find the datasets you'd like to replicate.  
![image info](./../fig/rucio_2.png)

- Choose which LOCALGROUPDISK you want to use.
-- `BNL-OSG2_LOCALGROUPDISK` is the right endpoint for BNL.  `BNL-OSG2_SCRATCHDISK` can be used if you only need the data to be there for a few days or a week.
-- `SLACXRD_DATADISK`, `SLACXRD_LOCALGROUPDISK` and `SLACXRD_SCRATCHDISK` are all possible endpoints for SLAC.
![image info](./../fig/rucio_3.png)

- Make sure to set the lifetime -- leave blank for data that shouldn't expire!
![image info](./../fig/rucio_4.png)

- Submit your request
![image info](./../fig/rucio_5.png)

- ...  and now the rule exists!  It may take a day or so for the transfer to occur, depending on how big the dataset is.
![image info](./../fig/rucio_6.png)

{% include links.md %}

