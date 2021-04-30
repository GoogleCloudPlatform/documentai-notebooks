# Document AI Notebooks 

This repository contains several [Jupyter notebooks][notebooks] 
to be used with the Cloud [Document AI Platform][docai]. Use the general notebooks
to process any form type or the specialized notebooks for any of the solutions such
as [Procurement DocAI][pdai] or [Lending DocAI][ldai]. These notebooks help you get
started with extracting data from your documents whether you're bring your own form types
or using one of our specialized parsers for invoices, receipts, tax forms and more.

![gif](resources/screenshots/invoice-notebook.gif)

## Prerequisites 

You must have your own GCP project with billing enabled and have working knowledge of the following products:

* [Google Cloud Storage][gcs]
* Google Document AI [Concepts][basics] and [Processors][processors]
* (Optional) [AI Platform Notebooks][notebooks]

### Set Up Steps

1. Set up your GCP project for Document AI following the [Setup Guide][set_up].
1. Enable the 'Document AI API' in your project in the Document AI [Platform][platform].
1. [Create][create_notebook] or use an existing instance of AI Platform Notebook with Python 3 using the default configurations.
1. In the notebook, go to **Git** > **Clone a Repository** and paste the repository URL.
1. Install the required libraries in the notebook terminal `python -m pip install -r requirements.txt`

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
[pdai]: https://cloud.google.com/solutions/procurement-doc-ai/
[ldai]: https://cloud.google.com/solutions/lending-doc-ai/
[docai_basics]: https://cloud.google.com/document-ai/docs/basics
[processors]: https://cloud.google.com/document-ai/docs/processor-overview
[set_up]: https://cloud.google.com/document-ai/docs/setup
[platform]: https://console.cloud.google.com/ai/document-ai
[create_processor]: https://cloud.google.com/document-ai/docs/create-processor
[create_notebook]: https://cloud.google.com/ai-platform/notebooks/docs/create-new
[gcs]: https://cloud.google.com/storage
[basics]: https://cloud.google.com/document-ai/docs/basics
