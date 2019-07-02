
```
{
    "Version":"2012-10-17"
    "Statement":[
        {
            "Resource":"arn:aws:s3:::iambuck",
            "Effect":"allow",
            "Action":"s3:*"

        }
    ]
}
```
Policy simulator

```
{
   "Version":"2012-10-17",
   "Statement":[
      {
         "Effect":"Allow",
         "Action":"ec2:Describe*",
         "Resource":"*"
      },
      {
         "Effect":"Allow",
         "Action":[
            "ec2:StartInstances",
            "ec2:StopInstances",
            "ec2:RebootInstances"
         ],
         "Resource":[
            "arn:aws:ec2:us-east-1:111122223333:instance/*"
         ],
         "Condition":{
            "StringEquals":{
               "ec2:ResourceTag/Owner":"Bob"
            }
         }
      }
   ]
}
```