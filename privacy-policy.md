# Privacy Policy

_Last Updated: 25th Nov, 2024_

## Introduction

Thank you for choosing **Inreer**, a Chrome extension designed to analyze resume and job compatibility on LinkedIn. This Privacy Policy explains how user data is collected, processed, and stored to ensure transparency and trust.

## Data Collection and Usage

### **Resume Data**
- Your resume data is used exclusively to analyze job compatibility.
- Resume data is transmitted temporarily to an **AWS Lambda Function**, which processes the data in combination with job descriptions. This processing determines a compatibility score using the **Gemini API**.
- After the analysis is complete, results are sent back to the extension. No resume data or analysis results are stored on AWS Lambda servers or any external servers. All data is stored locally on your browser.

### **Job Data**
- Job descriptions and related data are scraped from LinkedIn job pages to perform compatibility analysis. Like resume data, job data is temporarily transmitted to the AWS Lambda Function for processing and is not stored on any server.

### **Local Storage**
- All resume data and analysis results, including compatibility scores and insights, are stored locally on the user's browser in **IndexedDB**. This ensures data remains on the client-side, giving users full control.

## Permissions Required

To function effectively, the extension requires the following permissions:

1. **SidePanel**:  
   Enables the display of the side panel, which serves as the central interface for managing resumes and viewing compatibility reports.

2. **Tabs**:  
   Allows monitoring of active tabs to ensure the content script is injected only on LinkedIn job-related pages (`linkedin.com/jobs/*`) when users navigate between tabs.

3. **Storage**:  
   Facilitates real-time updates of analysis reports by enabling communication between the content script and side panel. This ensures that the side panel reflects the latest compatibility results.

4. **Host Permissions**:  
   Provides access to LinkedIn job-related pages (`linkedin.com/jobs/*`) to extract job descriptions and related data for analysis.

5. **Scripting**:  
   Permits the injection of content scripts into LinkedIn job-related pages to scrape data and enable interaction with page content.

## Data Sharing
Resume and job data are shared only with the AWS Lambda Function and Gemini API for temporary processing. No data is shared with third parties outside the scope of analysis.

## Changes to This Policy

We may update this Privacy Policy periodically to reflect changes in the extension or to address new legal or operational requirements. Updates will be posted in this repository, with the latest update date displayed at the top.

## Contact

For inquiries or concerns regarding this Privacy Policy, please open an issue in this repository or reach out to **hasin.z.dev@gmail.com**.
