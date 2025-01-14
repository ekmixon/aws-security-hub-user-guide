# AWS Config resources required for CIS controls<a name="securityhub-standards-cis-config-resources"></a>

To run security checks for the enabled controls on your environment's resources, Security Hub either runs through the exact audit steps prescribed for the checks in [Securing Amazon Web Services](https://www.cisecurity.org/benchmark/amazon_web_services/) or uses specific AWS Config managed rules\.

If you don't enable all resources in AWS Config, a finding is generated for the control [2\.5 – Ensure AWS Config is enabled](securityhub-cis-controls.md#securityhub-cis-controls-2.5)\. For other CIS controls, for Security Hub to accurately report findings, you must enable recording for the following resources in AWS Config\.
+ `AWS::CloudTrail::Trail`
+ `AWS::EC2::SecurityGroup`
+ `AWS::EC2::VPC`
+ `AWS::IAM::Policy`
+ `AWS::IAM::User`
+ `AWS::KMS::Key`
+ `AWS::S3::Bucket`

If a finding is generated by a security check that is based on an AWS Config rule, the finding details include a **Rules** link to open the associated AWS Config rule\. To navigate to the AWS Config rule, you must also have an IAM permission in the selected account to navigate to AWS Config\.