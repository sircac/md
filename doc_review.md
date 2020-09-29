
#  Document Title

Short introduction.

[TOC]

##  Topic

Content.

##  See also

* https://link-to-more-info


## Dorothea's notes

Here

### mail #1

Here

### mail #2

```text
Dear Daniele, dear Agustin,  
  
apologies for being very late with this, stuck in PMT and DOM testing.  
  
I forward my message from 28 August for the steps required. The actual calibration/testing has changed some as routines were updated.  
  
Some comments still:  
  
- A first sanity check of data can be done by using e.g. JRunAnalyser (check rates/ToTs).  
- For the HV tuning we will need L0 runs (this changed with respect to the documentation) and at least 5 minutes at each HV step  
- The HV calibration script is almost finished and also available in Jpp, only the automatized upload of the HV settings is still under discussion/missing  
- For the inter-DOM time calibration a new simplified script exists by Alex C., we for now skip the intra-DOM time calibration in the dark room; most important item is here to ensure that for each DOM we have at least one Laser signal;  
- For the nanobeacon we are lacking a standard evaluation software for now, Camiel is working on it. The runs to be taken are hoped to be useful for nanobeacon HV tuning  
- For the acoustic devices (piezo/hydrophone) testing there exists a new routine for the check in the git repository below  
- For the compass check Bryan developed a new test routine, which immediately provides feedback on the functioning, the routine is also in the git repository below  
  
https://git.km3net.de/calibration/du-dark-room-testing  
  
I can only offer Friday for a discussion in person (vidyo), let me know,  
cheers,  
Dorothea
```

### mail's #3

```text
Dear Paolo,  
  
since DU 39 has priority I would like to help ensuring that we don't have any hiccups in the procedures and see how/if I can help in preparing.  
  
To my understanding you still need to take data for the following:  
  
1) HV tuning (as the replacement DOM needs to be tuned) -> 15 x 8 minutes L0 data = 120 minutes)  
2) laser runs (time calibration) -> 10 minutes L0 & 10 minutes L1 = 20 minutes  
3) nanobeacon runs -> 30 x 3 minutes L0 data = 90 minutes  
4) compass check -> included in any run  
5) piezo check -> included in any run >5min with acoustic emitters on  
  
Please note that we will need L0 data for the HV tuning (for DU 38 we have only L1 data, which provides far too little statistics and in addition a bias), we will adjust the descriptions accordingly.  
  
Let me know if I can help with anything.  
  
cheers,  
Dorothea
```

&darr;

```test
I saw in the elog about the DAQ/software setup in Catania that we use jpp12 at the site:  
  
[https://elog.km3net.de/DU+Integration/737](https://elog.km3net.de/DU+Integration/737)  
  
Is this determined via the pairing with the CU version or can we there move to a newer Jpp version?  
  
In terms of tests and calibration of the data taken at the test site we will use newer Jpp versions, but of course those tests anyway will then be performed in Lyon, where we have those versions available.  
  
Thanks for your help,  
  
cheers,  
Dorothea  
-----------------------------------------------  
  
**Software**

-   CU-Server
    -   Jpp: 12.1.0
    -   CU: 9.0.21215.8765
-   DAQ-Server
    -   Jpp: 12.1.0
    -   CU: 9.0.21215.8765
```


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk1MzQzMzUxMSwtMTI1Njc1Mjc3NCwtMj
A3MzMxOTk3OV19
-->