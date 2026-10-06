# AWS S3 Static Website Hosting: Beach Wave Conditions

## Objective
Successfully deployed a highly available static website displaying local beach wave conditions using Amazon S3.

## Implementation Steps

*   **Asset Upload:** Uploaded the core website files to an S3 bucket named `website-bucket-2917a580-c0c2`, including `index.html`, `styles.css`, and `main.js`.
    
    <img width="500" height="250" alt="2" src="https://github.com/user-attachments/assets/c79bdaa5-dcad-4757-bb1d-0f4093b5b08b" />




*   **Public Access Configuration:** Navigated to the Permissions tab and confirmed that the "Block all public access" setting was turned off.
    
     <img width="226" height="88" alt="3" src="https://github.com/user-attachments/assets/e383b3d1-2c3e-4081-8840-0985b241f77b" />


*   **IAM Bucket Policy:** As you can see it has default json policy granting the `s3:GetObject` action to ensure all items in the bucket were publicly readable.
    
     <img width="341" height="192" alt="4" src="https://github.com/user-attachments/assets/2c13ee4a-06b0-4f03-adb9-bd569bc14157" />

*   **Static Hosting Setup:** Enabled "Static website hosting" in the bucket properties. Configured the index document as `index.html` and the error document as `error.html` to perfectly match the uploaded object names.
    
    <img width="341" height="192" alt="6" src="https://github.com/user-attachments/assets/d5276f69-5256-4696-acc8-23d1065cf27c" />


*   **Verification:** Accessed the generated AWS bucket website endpoint to verify the HTML and CSS rendered correctly on the live web.
    
    <img width="463" height="236" alt="image_133023" src="https://github.com/user-attachments/assets/38345e13-a275-4bd7-a131-938bb1b00c03" />




## Key Learnings & Security Concepts

*   **Default Privacy:** I learned that AWS S3 buckets are completely private by default. Making a site public requires a deliberate two-step process: disabling the account-level public access block and explicitly writing a resource-based policy to allow read access.
*   **Endpoint Routing:** Understanding how to properly route the bucket's root URL to a specific object (like `index.html`) is critical for the website endpoint to function without throwing a 403 Forbidden or 404 Not Found error.
