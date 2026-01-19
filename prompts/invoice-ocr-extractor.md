curl --location --request POST 'https://api.ocr.space/parse/image' \
--header 'apikey: [YOUR_API_KEY]' \
--form 'file=@"[BINARY_FIELD_NAME]"'

# NOTES:
# 1. [YOUR_API_KEY]: Replace this with your personal API key obtained from https://ocr.space/ocrapi.
#    This is required for authentication via the Header parameter.
#
# 2. [BINARY_FIELD_NAME]: Replace this with the name of the binary property coming from the previous node.
#    In n8n, this is typically 'data', 'attachment_0', or 'file'.
#    This name must match the "Input Data Field Name" in your HTTP Request node.
#
# 3. Import Instructions: 
#    - Copy the command above.
#    - In n8n, add an "HTTP Request" node.
#    - Click on "Import cURL" and paste this command to auto-configure the node.
