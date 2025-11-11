# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**

<img width="1920" height="1200" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/ddb90b36-c1ea-4fad-a0a4-089a936c6db2" />
<br>
<img width="1920" height="1200" alt="Screenshot (89)" src="https://github.com/user-attachments/assets/fbdfbde1-4c9b-4877-92ac-245a91ed15f0" />


**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
