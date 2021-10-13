# dhee-transliteration-api-client

# Dhee.AI Transliteration REST API

The transliteration API of Dhee.AI helps you to change the script of an input text to a different one. This is ideal for reading names, addresses, etc in a desired language, in spite of the source text being in a different language (or script, to be particular).

The API is to be used via REST calls, as per the specifications below:

## Request Format

URL
https://runtime.dhee.ai/akshar/{projectId}/transcribe
METHOD
POST
Authentication
Basic, with apiKey & secret
Parameters
text, targetLanguage, entityType

text : The text to be transcribed.
targetLanguage : language to which text should be transcribed
entityType : The type of the text. Possible values are NAME, ADDRESS, OTHERS


Request Headers

Content-Type
application/x-www-form-urlencoded
authorization
Basic [Token = base64 encoded apiKey:secret]


## Response Format
The output response body will be a JSON of the following format -

{
	result:”{transliterated text} OR {error message in case success=false}”,
	success : “true|false”
}

