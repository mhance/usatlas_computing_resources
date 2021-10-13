---
title: "US-ATLAS Shared Tier-3's"
teaching: 2
exercises: 0
questions:
- "What computing resources does US-ATLAS offer?"
objectives:
- "Understand what US-ATLAS provides."
keypoints:
- "US-ATLAS can't do your analysis, but it can help."
---

In this episode, we'll introduce the concept of a "Shared Tier-3", and how you can use it.

# Computing Centers in ATLAS

ATLAS has "tiered" computing facilities:

- Tier-0: CERN-hosted resources that perform first-pass processing of detector data.  Used for calibrations and initial event reconstruction.  Users do not run jobs here.
- Tier-1: Several Tier-1's located throughout the world; in the US, we have a Tier-1 at Brookhaven National Lab.  Large facilities used for grid computing.  Used for both production jobs and user jobs.  No interactive access for users.
- Tier-2: Many Tier-2's located throughout the world, several in the US.  From the user point of view, these are indistinguishable from Tier-1's.
- Tier-3: Equivalent of institutional clusters.  Usually there is no grid access, and users need to be granted permission to access them.  They provide interactive access in addition to local batch clusters and storage.  (Similar to `lxplus` at CERN.)

Our focus will be on the Tier-3's, which are most effectively used for processing flat ntuples:

![image info](./../fig/analysis_workflow.png)

{% include links.md %}

