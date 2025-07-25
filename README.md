# EditImage Workflow Changelog

This document outlines the recent changes made to the `Edit_Image.json` workflow.

## Summary of Changes

The workflow has been significantly updated to improve its robustness, documentation, and functionality. The key changes include the addition of a comprehensive error handling mechanism, enhanced logging capabilities, improved documentation, and dynamic image naming.

## Detailed Changes

### 1. Error Handling

A new error handling mechanism has been implemented to ensure that the workflow can gracefully handle any issues that may arise during execution. This includes:

- **Error Trigger:** An `Error Trigger` node has been added to catch any errors that occur within the workflow.
- **Telegram Notifications:** A `Send Error Message` node has been configured to send a notification via Telegram when an error occurs. This allows for immediate notification of any issues.
- **Google Sheets Logging:** A `Log Error to Sheet` node has been added to log the error details to a Google Sheet. This provides a historical record of any errors that have occurred, which can be used for later analysis and debugging.

### 2. Enhanced Logging

The `Image Log` node has been updated to log more detailed information about the images being processed. The new fields include:

- `File ID`: The unique identifier for the file in Google Drive.
- `File Name`: The name of the file.
- `Size (Bytes)`: The size of the file in bytes.
- `Owner Email`: The email address of the file owner.
- `Owner Display Name`: The display name of the file owner.
- `Is Shared`: A boolean value indicating whether the file is shared.
- `Viewers Can Copy?`: A boolean value indicating whether viewers can copy the file.
- `Image Resolution`: The resolution of the image.

### 3. Improved Documentation

Several `Sticky Note` nodes have been added to the workflow to provide clear and concise documentation for each step. This makes the workflow much easier to understand and maintain.

### 4. Dynamic Image Naming

The `Upload Image` node now uses a dynamic naming convention for the images it uploads to Google Drive. The new image name is passed as an input to the workflow, which allows for greater flexibility and control over the naming of the output files.

### 5. Updated Credentials

The credentials for the various services used in the workflow (Google Drive, Google Sheets, OpenAI, and Telegram) have been updated to ensure that the workflow has the necessary permissions to access these services.
