# Azure AI Translator Document Translation Script

## Overview
This script enables users to translate documents using Azure AI Translator. It supports multiple formats: PDF, DOC, DOCX, and TXT. The translation language is set via an environment variable, making it flexible and easy to change.

## Prerequisites
To use this script, you need:
1. An active Azure subscription.
2. A Translator resource in Azure.
3. A Storage account in Azure.

## Setup
1. **Clone the Repository**: Copy the code from this GitHub repository to your local machine.
2. **Environment File**: Create a `.env` file in your project directory. Add all necessary keys and values, including Azure credentials, storage account details, and the target translation language.
3. **Upload to Source Container**: Upload your file to the source container in your Azure Storage account.
4. **Run the Script**: Execute the script locally on your machine. The script will read the target language from the `.env` file.
5. **Check Output**: The translated file will be saved locally and also uploaded to the target container in Azure.

## `.env` File Example
Here's an example structure for the `.env` file:

AZURE_DOCUMENT_TRANSLATION_ENDPOINT="https://[your-path].cognitiveservices.azure.com/"  
AZURE_DOCUMENT_TRANSLATION_KEY="[your-key]"  
AZURE_STORAGE_SOURCE_ENDPOINT="https://[storage-account-name].blob.core.windows.net/"  
AZURE_STORAGE_ACCOUNT_NAME="[your-storage-account-name]"  
AZURE_STORAGE_SOURCE_KEY="[your-key]"  
AZURE_TRANSLATE_TARGET_LANGUAGE="[target-language-code]"  
AZURE_STORAGE_SOURCE_CONTAINER_NAME="source"  
AZURE_STORAGE_TARGET_CONTAINER_NAME="target"  
AZURE_DOCUMENT_NAME="[file-name-with-extension]"



Replace the placeholders with your actual Azure details and desired settings.

## Note on Large Files
For large files, it's advisable to split them into smaller segments before translation for efficiency.
