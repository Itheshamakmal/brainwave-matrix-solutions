# brainwave-matrix-solutions
Task 2
# Static Website Hosting on Amazon S3  

## Overview  
This project demonstrates how to host a static website using **Amazon S3**. The website includes simple HTML and CSS files and leverages S3's capabilities for reliable, scalable, and cost-effective hosting.  

## Features  
- **Responsive Design:** Ensures the website looks great on all devices.  
- **High Availability:** Hosted on Amazon S3 for 99.99% durability and uptime.  
- **Secure Access:** Configured Access Control Lists (ACLs) and bucket policies to control public access.  
- **Scalable Hosting:** Capable of handling varying traffic levels without manual intervention.  

## Architecture  
1. **Amazon S3 Bucket:**  
   - Created a bucket named `brainwave-matrix-task-2`.  
   - Enabled **static website hosting** on the bucket.  
2. **Access Control:**  
   - Configured the bucket to allow public access to website files.  
   - Set up bucket policies and ACLs to restrict unwanted access.  
3. **Website Files:**  
   - `index.html`: The main page of the website.  
   - `styles.css`: Stylesheet for the website design.  

## Steps to Recreate  
1. **Create an S3 Bucket:**  
   - Navigate to the S3 console and create a new bucket named `brainwave-matrix-task-2`.  
   - Use the **US East (N. Virginia) (us-east-1)** region.  
2. **Enable Static Website Hosting:**  
   - Go to the bucket's **Properties** tab.  
   - Enable **Static website hosting** and specify `index.html` as the default document.  
3. **Upload Website Files:**  
   - Upload the `index.html` and `styles.css` files to the bucket.  
   - Ensure these files are made public for access.  
4. **Set Bucket Policy:**  
   - Apply a bucket policy to grant read access to all users. Example policy:  
     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Effect": "Allow",
           "Principal": "*",
           "Action": "s3:GetObject",
           "Resource": "arn:aws:s3:::brainwave-matrix-task-2/*"
         }
       ]
     }
     ```  
5. **Access the Website:**  
   - Use the S3 bucket endpoint URL provided in the static hosting settings to access your website.  

## Tools and Technologies  
- **Amazon S3**  
- **HTML/CSS**  

## Learning Outcomes  
- Configuring and managing S3 buckets for hosting.  
- Setting up static website hosting on AWS.  
- Managing bucket policies and ACLs for public access.  
- Understanding how S3 endpoints work for web hosting.  

## Repository  
All the files and configuration steps are available in this repository.  

---  

Feel free to tweak this further or let me know if additional details need to be added!
