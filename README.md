# blockchain-based-certificate-verification-and-validation
project
Certificate Verification and Validation using Blockchain
Now-a-days all peoples are opted for education to get good job and they are generating fake certificates to achieve their goals and existing technologies has no support to verify such certificates. So in propose paper we are introducing Blockchain technology which store immutable data and its data cannot by modify in any manner. So while giving certificate to student, admin user will store certificate copy in Blockchain and obtained its digital signature and then generate QR code on that signature and affix that code on student certificate. This certificate can be scanned by other companies or institution to verify and extract details from Blockchain. If QRCODE exists in Blockchain then certificate validation will be successful.
Blockchain is a distributed data storage technology which supports data verification using Hashcode. Blockchain forms a peer to peer network where data store in one peer will get replicated to multiple peer in distributed manner and Blockchain store each data as block and associate each block with unique Hashcode. While storing next record Blockchain will verify previous Hashcode and if all Hashcode matches at all nodes then only it will store new record otherwise data will be considered as tamper so due to this reason its become difficult for anybody to alter Blockchain data and hence called as immutable.  
To avoid certificate forgery we are adding certificate verification mechanism using Blockchain technology and this project consists of 3 modules
1)	Admin: Admin is an education authority which login to system using username and password as ‘admin’ and ‘admin’. After login admin will upload student details and certificate and this details will be uploaded to Blockchain and Blockchain associate each certificate with unique hash code called as digital signature. QRCODE will also be generated on Hashcode and affix on student certificate and this QR CODE can be scanned from mobile to get details from Blockchain and if QR CODE exists in Blockchain then certificate validation successful
2)	Company: company user can signup and login to system and then scan and upload certificate and then application will generate digital signature and matched with those signature stored in Blockchain and if certificate is original then same signature will be generated and authentication will be successful.
3)	Scanner Module: This is a standalone module which will maintain by education institution and companies and using this module they can scan QRCODE to get details from Blockchain
To store data in Blockchain we need to develop SOLIDITY contract which contains functions to STORE and authenticate certificate details. This solidity contract need to be deployed on Ethereum Blockchain and then it will return contract deployed ADDRESS and this address we can specify in PYTHON code to store and access certificate details.
Below is the solidity code developed for this project.
 
In above solidity code we have defined functions to store and access company and certificate details. To deploy above contract in Ethereum we need to follow below steps
1)	Go inside ‘hello-eth/node-modules/.bin’ folder and then double click on ‘runBlockchain.bat’ file to start Ethereum tool and get below screen
2)	 
3)	In above screen we can see Ethereum generate some default ADDRESS and private keys and in above screen type command as ‘truffle migrate’ and press enter key to deploy contract and will get below output
4)	 
5)	In above screen in white colour text we can see ‘Certificate Verification’ contract deployed and we got contract address also and this address we will specify in PYTHON code to access that contract. Now let above screen running. n below screen we are showing PYTHON code with address to access that contract
6)	 
7)	In above screen read red colour comments to know how to call Blockchain contract from python code to store or view data
SCREEN SHOTS
To run project double click on ‘run.bat’ file to start python server and get below output
 
In above screen python FLASK server started and now open browser and enter URL as http://127.0.0.1:5000/index and press enter key to get below page
 
In above screen click on ‘Educational Authority Login’ link to get below login screen
 
In above screen admin is login and after login will get below screen
 
In above screen admin can click on ‘Upload New Certificates’ link to upload certificate
 
In above screen admin is adding student details and then uploading certificate and then press ‘Submit’ button to get below output
 
In above screen student details added and we can see digital signature generated and stored in Blockchain for uploaded certificates and now admin can click on ‘Click Here to Download QR Code image’ button to download QRCODE and get below output
 
In above screen in browser status bar we can see QR code image downloaded and this image student can keep in his mobile. Now admin can click on ‘View Certificates Details’ to view all certificates stored in Blockchain
 
In above screen we can see different certificates of same or new student stored in Blockchain and we can see date and time of upload with digital signature and QR CODE image. Now admin can click on “View Companies Details’ to allow admin to view registered companies
 
In above screen admin can view list of registered companies and now logout and signup new company to perform verification
 
In above screen company is entering signup details and press button to store details in Blockchain and will get below output
 
In above screen we can see company signup task completed and now click on ‘Company Login Here’ link to get below login screen
 
In above screen company is login and after login will get below screen
 
In above screen company can click on ‘Authenticate Certificate’ to upload certificate copy received from student and perform verification
 
In above screen company can upload certificate and get below details if authenticated 
 
In above screen company can view all details of uploaded certificated and in last column we can see authentication successful and similarly they can upload and verify any certificate
 
In above screen I am uploading another certificate and below is the output
 
In above screen we can see Authentication failed for uploaded certificate.
Now company or educational institution can validate certificate by scanning QR code and to do that, just double click on ‘RunWebCam.bat’ file to get below output
 
In above screen click on ‘Start Webcam’ button to start camera and get below output
 
In above webcam from mobile they need to scan QRCODE like below screen
  
In above screen once we show QR code then all details for that QR code certificate will be retrieve from Blockchain and display in above TEXT area. Similarly if we scan wrong CODE then will get below output
 

 
In above screen we got message as Certificate validation failed as QR code does not exists

 

 
