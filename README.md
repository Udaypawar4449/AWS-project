# AWS-project

Hosting a Static Website on AWS S3 using the Management Console

1.	Login to AWS Console:
•	Navigate to AWS Console.
•	Sign in with your AWS account credentials.

2.	Create an S3 Bucket:
•	Go to the S3 service in the AWS Management Console.
•	Click on the "Create bucket" button.
•	Enter a unique and meaningful name for your bucket.
•	Choose the AWS region for your bucket.
•	Click "Create."

3.	Upload Website Files:
•	Open the newly created bucket.
•	Click on the "Upload" button.
•	Select and upload your website files (e.g., HTML, CSS, JS).
•	Ensure that the files are publicly accessible.

4.	Set Bucket Properties:
•	In the bucket properties, select the "Static website hosting" card.
•	Choose the "Use this bucket to host a website" option.
•	Set the "Index document" to index.html or the main page of your website.
•	Click "Save changes."

5.	Configure Bucket Permissions:
•	In the bucket properties, go to the "Permissions" tab.
•	Update the bucket policy to allow public access to your website. You can use the following example policy:
json code:
{
 "Version": "2012-10-17",
 "Statement": [
 {
 "Effect": "Allow",
 "Principal": "*",
 "Action": "s3:GetObject",
 "Resource": "arn:aws:s3::: udayaws.com /*" 
}
 ]
    } 
•	Replace udayaws.com with the name of your bucket.
•	Click "Save changes."

6.	Access your Website:
•	After saving the changes, you'll see the endpoint URL under the "Static website hosting" card.
•	Open the provided endpoint URL in a web browser to access your static website.

7.	Optional: Configure Custom Domain (if applicable):
•	If you have a custom domain, you can configure it by following the instructions provided in the "Custom Domain" section on the "Static website hosting" card.
Note:
Remember to replace placeholder values like ‘udayaws.com’ with your actual bucket name.

Cleanup (if needed):
If you want to remove the static website hosting configuration, you can:
1.	Navigate to the bucket properties > "Static website hosting."
2.	Choose the "Disabled" option for hosting.
3.	Update or remove the bucket policy in the "Permissions" tab to restrict or revoke public access.

