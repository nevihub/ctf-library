# Number Bases — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/8964d7b06a234684abffade642838140 (login required)_

## Technique

Identify the encoding from its indicators: 0x prefix means hex, trailing = means base64, digits limited to 0/1 means binary. Decode each with CyberChef or CLI tools (xxd -r -p, base64 -d). Molly's value is doubly encoded: decode the binary first to get a base64 string, then decode the base64 to plaintext.
