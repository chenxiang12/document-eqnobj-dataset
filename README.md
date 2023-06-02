# document-eqnobj-dataset
This dataset is used to train CNN model to detect malicious document with formula editors exploits, such as CVE-2017-11882, CVE-2018-0802 and CVE-2018-0798.

* 01-train_oleEqnB  
4078 benign Equation Ole Objects comes from Internet and my lab
* 02-train_oleEqnM  
1173 malicious Equation Ole Objects comes from 1798 malicious RTF files in Virustotal
* 03-test_oleEqnB  
1323 benign Equation Ole Objects comes from Internet
* 04-test_oleEqnM  
312 malicious Equation Ole Objects comes from Virustotal directly
* 05-test_oleEqnMPurify  
312 adversarial sample comes from 04-test_oleEqnM by erasing malicious commands in the object
* 06-test_oleEqnMCloak  
312 adversarial sample comes from 04-test_oleEqnM by adding formula elements in the object 
* 07-test_oleEqnB_matrix  
614 benign Equation Ole Objects comes from Internet, many of them are matrix
* 08-test_oleEqnM_wps  
3 malicious Equation Ole Objects exploit WPS vulnerability
* images  
Contain images for all the objects above. The size of image is 72*64 = 4608. If the object's size less than 4608, appending \x00 bytes to it when converted to image. If the object's size above 4608, just use the first 4608 bytes when converted to image.
* model.html  
The code of model and data processing 
* result.xlsx  
Some test result
