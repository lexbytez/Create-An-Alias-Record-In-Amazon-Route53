# Createing-An-Alias-Record-In-Amazon-Route53
After hosting the static website from the previous task  your team lead realized the s3 endpoint was inadequate. Consequently, it was requested that you set up an Alias record in Amazon Route53 for the S3 Endpoint and make the website secure by serving its content over https

Lex Byte



Project Description

After hosting the static website from the previous task https://app.techchak.com/projects/140?view=builder, your team lead realized the s3 endpoint was inadequate. Consequently, it was requested that you set up an Alias record in Amazon Route53 for the S3 Endpoint and make the website secure by serving its content over https

Step one

Head to AWS CONSOLE

Create an S3 Bucket, make sure to allow pubic access when setting up

Upload website source code to bucket

Under created bucket go to properties and enable static website hosting

Under objects, choose all an actions(Make public using ACL)this is to allow public access to hosted files
![1](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/98435c0f-8f63-4b54-a154-453c3b51e5ef)
![2](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/314e3a45-420d-4f9e-98a9-a3aa69406ebf)
![3](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/bc651645-fdb3-4f67-85e3-98bf059ddc9f)
![4](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/bc5d22d0-51a8-47c5-adb9-f184d45df068)
Step Two

Got a domain name for the project from namecheap.com

Head to Route53 in your Aws console

Create a hosted zone with same domain name gotten and make it public hosted zone

Next create record, Record type IPv4 address

Click on Alias, choose option to route to S3 Endpoint.

Choose region your bucket is hosted in, and choose routing policy as simple

Create the record and save
![1](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/90d671a0-cacb-413b-ace1-3b449535f99e)
![2](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/1c1a73db-db8e-459e-ba9d-a58cbddbba8c)
![3](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/3e2111af-2533-4335-908e-1a7846aae985)
![4](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/4a24ba09-60b0-4462-aa16-25d3d200c4c2)
![5](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/a2edbde6-1507-49d5-b8d9-c55ee633798c)
Step Three

Head to namecheap, and click on manage

Go to nameservers setting, choose Custom DNS

Under the Nameservers 1 &2 Update to nameservers gotten from Route53 hosted zone records we created and save

Once saved, it should bring and update it might take up to 48 hours to take affect

After waiting for an hour the domain name was checked and its up and running
![8](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/1e77e6d0-fa2e-46b0-9cf6-5010d978a660)
![9](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/94fe3ef1-a320-4778-a080-0b73e8fdaeb3)
![10](https://github.com/lexbytez/Createing-An-Alias-Record-In-Amazon-Route53/assets/128375535/ba934da2-b9f0-4490-bf9f-1740828b3fec)

