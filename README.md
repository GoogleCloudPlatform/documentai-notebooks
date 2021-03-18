# Document AI Notebooks 

This repository contains several [Google AI Platform notebooks][notebooks] 
to be used with the Cloud [Document AI Platform][docai].

![gif](resources/screenshots/invoice-notebook.gif)

## Prerequisites 

You must have your own GCP project with billing enabled and have working knowledge of the following products:

* [Google Cloud Storage][https://cloud.google.com/storage]
* Google Document AI [Concepts][basics] and [Processors][processors]
* (Optional) [AI Platform Notebooks][notebooks]

### Set Up Steps

1. Set up your GCP project for Document AI following the [Setup Guide][set_up].
1. Enable the 'Document AI API' in your project in the Document AI [Platform][platform].
1. [Create][create_notebook] or use an existing instance of AI Platform Notebook with Python 3 using the default configurations.

Please note Colab and Jupyter notebooks are also work with these samples. However, additional authentication will be required for service accounts.

## Instructions

1. Identify which form type or utility you would like to run through a processor.
2. Create your processor using the [instructions][create_processor].
3. Copy your processor id.
![processorId](resources/screenshots/FormParserID.png)
4. Update the PROCESSOR_ID, PROJECT_ID and REGION variables in the notebook.

```
PROJECT_ID = "YOUR_PROJECT_ID_HERE"
LOCATION = "LOCATION"  # Format is 'us' or 'eu'
PROCESSOR_ID = "PROCESSOR_ID"  # Create processor in Cloud Console
```
Please note, the location must match the one assigned to the processor. 

5. Run the notebook. 

[notebooks]: https://cloud.google.com/ai-platform-notebooks
[docai]: https://cloud.google.com/document-ai/docs/
[docai_basics]: https://cloud.google.com/document-ai/docs/basics
[processors]: https://cloud.google.com/document-ai/docs/processor-overview
[set_up]: https://cloud.google.com/document-ai/docs/setup
[platform]: https://console.cloud.google.com/ai/document-ai
[create_processor]: https://cloud.google.com/document-ai/docs/create-processor
[create_notebook]: https://cloud.google.com/ai-platform/notebooks/docs/create-new
[gcs]: https://cloud.google.com/storage
[basics]: https://cloud.google.com/document-ai/docs/basics
