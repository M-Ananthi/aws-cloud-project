# aws-cloud-project
# Static Website Hosting on AWS S3

This project demonstrates how to host a static website using Amazon S3. 
It includes configuring an S3 bucket, uploading website files, enabling static web hosting, and making the site publicly accessible.

---

## Project Overview
This project shows how to deploy a simple static website (HTML, CSS, JS) on AWS using S3. It covers:
- Creating an S3 bucket
- Uploading website files
- Enabling static website hosting
- Setting bucket permissions
- Testing the website URL

---

## Technologies Used
- **Amazon S3**
- **AWS Console**
- **HTML, CSS, JavaScript**

---

## Folder Structure
aws-cloud-project
├── index.html
└── screenshots/


## 🛠 Steps to Deploy on AWS S3

### 1. Create an S3 Bucket
- Go to AWS S3 console  
- Click **Create bucket**  
- Bucket name must be **unique**  
- Disable **Block all public access**  
- Enable **ACLs** if required  

### 2. Upload Website Files
- Upload `index.html`, CSS, JS and image files  
- Keep the file paths same as your project folder

### 3. Enable Static Website Hosting
- Go to **Properties** tab  
- Scroll to **Static Website Hosting**  
- Enable it  
- Set:
  - Index document: `index.html`
  - Error document: `error.html` (optional)

### 4. Make Website Public
Go to **Permissions → Bucket Policy** and add public access policy:

Replace `your-bucket-name` with your bucket's name.
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::static-demo-s3-bucket/*"
    }
  ]
}

### Get the Website URL
Go to:
**S3 → Bucket → Properties → Static Website Hosting**

Copy the **Endpoint URL** and open it in your browser.

---

## Example Output
Your hosted website will be accessible publicly using the S3 website endpoint like:
http://static-demo-s3-bucket.s3-website-ap-south-1.amazonaws.com

---

## Features
- Fully static website hosting
- No server management
- Scalable and cost-effective
- Supports HTML/CSS/JS

---

## Contact
For any queries or improvements, feel free to reach out.
**Author:** Ananthi M

---

## License
This project is licensed under the **MIT License**.

