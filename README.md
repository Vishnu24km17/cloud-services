# cloud-services
# AWS Translator service


Amazon Translate uses advanced neural machine translation technology to provide high-quality and accurate translations between different languages. It supports a wide range of language pairs, including popular languages such as English, Spanish, French, German, Chinese, Japanese, and many more

This code is an AWS Lambda function that translates the text content of a file stored in an S3 bucket. It uses the AWS Translate service and the boto3 library to perform the translation.

When triggered by an event, the function retrieves the file from the S3 bucket and reads its content line by line. Each non-empty line is translated from an unknown source language to Simplified Chinese ('zh-cn'). The translated lines are stored in a variable.

After processing all the lines, the translated content is uploaded back to the same S3 bucket with the same file name. Finally, a "Done" message is printed to indicate the completion of the translation process.

In summary, this code automates the translation of text files in an S3 bucket from an unknown language to Simplified Chinese using AWS Lambda and the AWS Translate service.

# Azure Cognitive Services OCR API: Image-to-Text Conversion
Azure Cognitive Services Computer Vision is a cloud-based service provided by Microsoft that enables developers to incorporate advanced image analysis capabilities into their applications. Specifically, the Computer Vision service offers powerful functionality for performing Optical Character Recognition (OCR) to convert text within images into machine-readable text.

This code demonstrates the usage of the Azure Cognitive Services Computer Vision API to extract text from an image specified by its URL. It establishes a connection to the API using the provided API key and endpoint. The code then initiates a read operation on the image and waits for the operation to complete. Once the operation is finished, the code retrieves the result and extracts the text lines from it. Finally, the extracted text lines are printed. This code provides a simplified and efficient way to perform optical character recognition on images and extract textual information using the Computer Vision API.




