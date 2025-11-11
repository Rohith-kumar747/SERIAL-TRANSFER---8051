# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**
```
#include<reg51.h> void main(void)
{
TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;
SCON=0X50; TR1=1;
while(1)
{ SBUF='X';
while(TI==0); TI=0;
}
}
```

**(ii)	Serial port to Transfer a Message**
```
#include<reg51.h> void main(void)
{
unsigned char msg[]="SYBAU"; unsigned char i;
TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;
SCON=0X50; TR1=1;
for (i=0; i<17;i++)
{
SBUF= msg[i]; while(TI==0); TI=0;
}
while(1);
}
```
 
**OUTPUT:**
**(i)	Serial port transfer a character A**

<img width="1920" height="1140" alt="Screenshot 2025-11-11 082602" src="https://github.com/user-attachments/assets/170c1de1-599f-40d3-8d59-74a3d69af121" />

**(ii)	Serial port to Transfer a Message**

<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/42bed1ea-cfeb-46c8-b4fa-ff982c182aff" />

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
