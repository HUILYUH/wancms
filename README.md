# wancms
## Vulnerability Name:
### wancms there is denial of service (DOS) in all verification codes of all systems.
## Vulnerability version number: 
### hand tour multimodal transport platform system V2.0, H5 intermodal platform system V1.0, page tour intermodal platform system V5.0, OA management system V1.0
## Vulnerability:
### high risk
## Vulnerability Description:
### DoS is the abbreviation of Denial of Service, that is, denial of service. Its purpose is to make computers or networks unable to provide normal services. DoS attack refers to the defect of intentional attack of network protocol or the brutally depleted resources of the attacked object by barbarous means. The purpose is to make the target computer or network unable to provide normal service or resource access, so that the target system service system stops responding and even collapsing.
## Loophole URL:
### http://demo.wancms.com/index.php?g=api&m=checkcode&a=index&code_len=4&font_size=20&width=200&height=35&charset=1234567890
### http://demo.wancms.com/index.php?g=api&m=checkcode&a=index&code_len=4&font_size=15&width=120&height=35&charset=1234567890
## Vulnerability Description:
We come to the front logon with the OA system
http://demo.wancms.com/user/login/forgot_password.html
![exploit](https://github.com/HUILYUH/wancms/blob/master/1.png?raw=true)
Get the verification code address at the right key at the verification code:
http://demo.wancms.com/index.php?g=api&m=checkcode&a=index&code_len=4&font_size=20&width=200&height=35&charset=1234567890
![exploit](https://github.com/HUILYUH/wancms/blob/master/2.png?raw=true)
Open the grab tool burpz, grab the data of the authentication code interface as follows, and send the right button to repeater.
![exploit](https://github.com/HUILYUH/wancms/blob/master/3.png?raw=true)
We can see the font size, length and width related parameters of the verification code, and the return time at the lower right corner is 67millis.
![exploit](https://github.com/HUILYUH/wancms/blob/master/4.png?raw=true)
Next, we increase the values of width or font_size or heigth and find that the right lower corner return time is 6159millis
![exploit](https://github.com/HUILYUH/wancms/blob/master/5.png?raw=true)
The value of the parameter is added again, and it is found that the return time is longer.
![exploit](https://github.com/HUILYUH/wancms/blob/master/6.png?raw=true)
##Suggestions for rectification:
###Delete these parameters in the link, or verify the server side, do not modify these parameters, or use other verification code. mode

