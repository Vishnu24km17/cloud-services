# cloud-services
# AWS Translator service


Amazon Translate uses advanced neural machine translation technology to provide high-quality and accurate translations between different languages. It supports a wide range of language pairs, including popular languages such as English, Spanish, French, German, Chinese, Japanese, and many more

This code is an AWS Lambda function that translates the text content of a file stored in an S3 bucket. It uses the AWS Translate service and the boto3 library to perform the translation.

When triggered by an event, the function retrieves the file from the S3 bucket and reads its content line by line. Each non-empty line is translated from an unknown source language to Simplified Chinese ('zh-cn'). The translated lines are stored in a variable.

After processing all the lines, the translated content is uploaded back to the same S3 bucket with the same file name. Finally, a "Done" message is printed to indicate the completion of the translation process.

In summary, this code automates the translation of text files in an S3 bucket from an unknown language to Simplified Chinese using AWS Lambda and the AWS Translate service.
