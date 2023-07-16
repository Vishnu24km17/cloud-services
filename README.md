# cloud-services
# AWS Translator service


Amazon Translate uses advanced neural machine translation technology to provide high-quality and accurate translations between different languages. It supports a wide range of language pairs, including popular languages such as English, Spanish, French, German, Chinese, Japanese, and many more

 The translate_text function takes two parameters: text (the text to be translated) and lang_code (the target language code). It uses the translate.translate_text method from the boto3 library to perform the translation. The source language is set to 'auto', which means it will automatically detect the source language of the text.

The lambda_handler function is the entry point for the Lambda function. It takes two parameters: event (the event data that triggered the Lambda function) and context (the runtime information of the Lambda function).

The file_name and bucketName variables are extracted from the event parameter, which contains information about the S3 object that triggered the Lambda function.

The outfile variable is created to specify the output file location in the S3 bucket.

The s3_client.get_object method is used to retrieve the S3 object from the specified bucket and key (file name).

The content of the file is read line by line using the splitlines method, and each line is decoded from bytes to a UTF-8 encoded string.

If a line is not empty, it is passed to the translate_text function to get the translated version in the target language ('zh-cn' for Simplified Chinese).

The translated line is printed and appended to the final_document_array variable, along with two newline characters for formatting.

After processing all the lines, the final_document_array is uploaded back to the S3 bucket using the s3_client.put_object method.

The message "Done" is printed to indicate the completion of the script.
