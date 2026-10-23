# Payments — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/b936bd566ae6467098522397e191fa5e (login required)_

## Technique

The log contains SOAP request/response pairs: split them apart, parse the XML into CSV, then sort and count in a spreadsheet to find the transaction count, the largest purchase's transaction ID, and the state with the most purchases.
