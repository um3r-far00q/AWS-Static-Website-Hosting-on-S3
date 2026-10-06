# AWS S3 Static Website Hosting: Beach Wave Conditions

## Objective
Successfully deployed a highly available static website displaying local beach wave conditions using Amazon S3.

## Implementation Steps

*   **Asset Upload:** Uploaded the core website files to an S3 bucket named `website-bucket-2917a580-c0c2`, including `index.html`, `styles.css`, and `main.js`.
    
  <img width="3114" height="1376" alt="Gemini_Generated_Image_uhupdpuhupdpuhup" src="https://github.com/user-attachments/assets/730a8313-4265-4ffd-8dd8-9002c5ce7ef5" />






*   **Public Access Configuration:** Navigated to the Permissions tab and confirmed that the "Block all public access" setting was turned off.
    
     <img width="3288" height="1280" alt="Gemini_Generated_Image_11hlcw11hlcw11hl" src="https://github.com/user-attachments/assets/35754278-4c70-4c66-ab01-d4003bb79c59" />



*   **IAM Bucket Policy:** As you can see it has default json policy granting the `s3:GetObject` action to ensure all items in the bucket were publicly readable.
    
     <img width="2752" height="1536" alt="Gemini_Generated_Image_pkoqtopkoqtopkoq" src="https://github.com/user-attachments/assets/20bb79b8-d21f-4d4b-889d-1ed9a4ab4984" />


*   **Static Hosting Setup:** Enabled "Static website hosting" in the bucket properties. Configured the index document as `index.html` and the error document as `error.html` to perfectly match the uploaded object names.
    
    <img width="2728" height="1536" alt="Gemini_Generated_Image_hsp4nthsp4nthsp4" src="https://github.com/user-attachments/assets/8c1e22a2-cb37-4e30-ae3e-7ced54216a5e" />



*   **Verification:** Accessed the generated AWS bucket website endpoint to verify the HTML and CSS rendered correctly on the live web.
    
   <img width="2752" height="1536" alt="Gemini_Generated_Image_lxxabxlxxabxlxxa" src="https://github.com/user-attachments/assets/e2d206b9-a965-450e-bba8-2c5f30ca14b7" />





## Key Learnings & Security Concepts

*   **Default Privacy:** I learned that AWS S3 buckets are completely private by default. Making a site public requires a deliberate two-step process: disabling the account-level public access block and explicitly writing a resource-based policy to allow read access.
*   **Endpoint Routing:** Understanding how to properly route the bucket's root URL to a specific object (like `index.html`) is critical for the website endpoint to function without throwing a 403 Forbidden or 404 Not Found error.
