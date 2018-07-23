# wancms
##Vulnerability Name:
###wancms there is denial of service (DOS) in all verification codes of all systems.
##Vulnerability version number: 
###hand tour multimodal transport platform system V2.0, H5 intermodal platform system V1.0, page tour intermodal platform system V5.0, OA management system V1.0
##Vulnerability:
###high risk
##Vulnerability Description:
###DoS is the abbreviation of Denial of Service, that is, denial of service. Its purpose is to make computers or networks unable to provide normal services. DoS attack refers to the defect of intentional attack of network protocol or the brutally depleted resources of the attacked object by barbarous means. The purpose is to make the target computer or network unable to provide normal service or resource access, so that the target system service system stops responding and even collapsing.
##Loophole URL:
###http://demo.wancms.com/index.php?g=api&m=checkcode&a=index&code_len=4&font_size=20&width=200&height=35&charset=1234567890
###http://demo.wancms.com/index.php?g=api&m=checkcode&a=index&code_len=4&font_size=15&width=120&height=35&charset=1234567890
##Vulnerability Description:


##Suggestions for rectification:
###Delete these parameters in the link, or verify the server side, do not modify these parameters, or use other verification code. mode

