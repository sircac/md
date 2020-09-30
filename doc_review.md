#  KM3NeT Document Review

Notes relative to the documentation for the Dark Room and Test Station procedures.

* [GitHub pages](https://sircac.github.io/md/doc_review.html)
* [GitHub repo](https://github.com/sircac/md)

[TOC]

## GD Documents

[km3net](https://drive.google.com/drive/u/1/folders/0BwpZkFK4qtbyd2k4ZGpPeDlETVE) > [Detector Construction and Operation (DET)](https://drive.google.com/drive/u/1/folders/0B6CcXapUNLNLc1hDek1VNTRXemM) > [Calibration (CALIB)](https://drive.google.com/drive/u/1/folders/0B-oDhZjfBP59d2JrSmV0Z05vdVE):
* [Time calibration](https://drive.google.com/drive/u/1/folders/0B-oDhZjfBP59TUtqTGxMTE9wcG8):
	* [TDR Time Calibration](https://drive.google.com/drive/u/1/folders/1SD0zdDe_zZ-u2POGRsz9S84olIqT4cCH):
		* ![https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/PDF_file_icon.svg/195px-PDF_file_icon.svg.png](https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/PDF_file_icon.svg/195px-PDF_file_icon.svg.png) [KM3NeT_CALIB_2016_005-DU_TimeCalibration_Procedure_MBouwhuis_v3](https://drive.google.com/file/d/0B7wtVGi6XbRXN3A4Z0djSlk5LW8/view)
		* ...
	* [White Rabbit System for MEOC and JB asymmetry](https://drive.google.com/drive/u/1/folders/1SD0zdDe_zZ-u2POGRsz9S84olIqT4cCH):
		* [ARCA JB Calibration Temporary Documents](https://drive.google.com/drive/u/1/folders/1HP4rDWcljWgT7PVNX9qI4qYBcoNMw29P)
		* ...
	* ...
* here:
* ...

##  Test Station

Here.

### GD documentation

Here.

##  Dark Room

Here.

### GD documentation

Here.

* https://link-to-more-info
* [here](https://link-to-more-infowww.google.es)


## Dorothea's notes

Here

### mail #1 (Daniele)
> The status is:
> -   the shore station hardware is the old one used for the calibration of ARCA-DU1, ARCA-DU2 and ARCA-DU3. Both Antonio and Tommaso know it in details.
> -   the two servers (CU and DAQ) have been formatted and re-installed with AIACE by Emidio Giorgio (LNS). (not confirmed if Jpp is the latest 13)
> -   all the "old stuff" (optical fiber splitter, acoustic emitters etc.) are available.
> - jumper(+test box) is damaged, plans about fix it on-going.

&nbsp;

### mail #2 (Dorothea)
> I am updating some of the previous procedures, so that we can have a simplified routine for the testers, who will not necessarily be expected to be experts.  
> Giorgio can best comment on the actions, the details are so far described in this [note](https://drive.google.com/file/d/1st4_wax7nuVBxVamRxYC1LnYRGEiLilJ/view).
> I see the steps to be performed in the testing/calibration as listed below, let me know if you already have comments/questions. 
>  
>  1) Hardware setup (servers&DAQ/lasers/acoustic emitters): I understand that this is already in good hands or is there information missing on the exact setting up (details are provided in the note above)?
>  
>  2) Time calibration of the WRS network: To my understanding a lot of the description in the document covers 1-time measurements, which are not necessary for each DU. The results are so far archived in excel sheets [here](https://drive.google.com/drive/folders/1GauYUdbD73NC1Z7hgcRqZlbxfEpNjQ4u).
>  
>  Assuming lasers & emitters are set up and the dark room and test station prepared for data taking I see the following order of tests and deliverables to be performed by the tester (who is that in Caserta?):
>  
>  3) Create Run setup with nominal HV
>  
>  4) Take 30 minutes of data -> Sanity check of dark rates (either via online monitoring or I can devise an analysis check)
>  
>  5) Create Run setups for HV scan (15 runs with HV within +-56V around nominal). Take HV data as described in Bouke's note (we are still refining the amount of data required and also possibly will here switch to L0 data)
>  
>  6) HV calibration following Bouke's script (procedure is being finalized now with Rodri's help)
**Deliverable:** Summary files and json file with HV settings uploaded to DB
>
> 7) Create run setups with tuned HV for the subsequent runs
> 
> 8) Time calibration using Lasers as described by time calibration document (under revision)
**Deliverable:** Inter-DOM time calibration -> upload as first nominal calibration to DB
>
> 9) Take 31 3-minute nanobeacon runs with L0 data and different nanobeacon voltages (scanning from 5V-12.5V in 0.25V steps)  
**Deliverable:** Good/bad flag for each nanobeacon (+ optimal nanobeacon HV), script for this check is under construction
>
> 10) Take long runs for stability check
> 
> 11) For at least some runs turn the acoustic emitters on, analyze with Carlo's newest script (I will put it to git)  
**Deliverable:** Good/bad flag for each acoustic receiver
>
> 12) Compass measurements: For all runs compass data should be in the DB. A new script by Bryan is available to evaluate those and print a concise summary of the amount of observed failures  
**Deliverable:** Good/bad flag for each compass

&nbsp;

### mail #3 (Dorothea)

> The actual calibration/testing has changed some as routines were updated.  
  Some comments still:  
> - A first sanity check of data can be done by using e.g. JRunAnalyser (check rates/ToTs).  
> - For the HV tuning we will need L0 runs (this changed with respect to the documentation) and at least 5 minutes at each HV step  
> - The HV calibration script is almost finished and also available in Jpp, only the automatized upload of the HV settings is still under discussion/missing  
> - For the inter-DOM time calibration a new simplified script exists by Alex C., we for now skip the intra-DOM time calibration in the dark room; most important item is here to ensure that for each DOM we have at least one Laser signal;  
> - For the nanobeacon we are lacking a standard evaluation software for now, Camiel is working on it. The runs to be taken are hoped to be useful for nanobeacon HV tuning  
> - For the acoustic devices (piezo/hydrophone) testing there exists a new routine for the check in the git repository below  
> - For the compass check Bryan developed a new test routine, which immediately provides feedback on the functioning, the routine is also in [this](https://git.km3net.de/calibration/du-dark-room-testing) git repository 

&nbsp;

### mail #4 (Dorothea)

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


> Last update on [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMzYzNDk4MCw2MjMwNTY0MjUsLTE3ND
g1MjIzMDIsODE0NTA3NDksLTE3NTU4MjYyMzgsLTE5NjU3MjA2
MDUsLTMwNTk2NTEzMSwtMTU1MzA1NTQxNywtMTA5NDU2OTI2NS
wxNTgyNjc0ODM3LC0xMDEyNDE1MjksMTQwNzQ5NTIxNCwtMTMy
Mjk4NjE1MywxNjkwOTQyMTYzLC0xMDIzNDI1MjU3LC0xMjU2Nz
UyNzc0LC0yMDczMzE5OTc5XX0=
-->