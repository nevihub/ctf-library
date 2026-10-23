# CAN Bus — walkthrough summary

_Official Trove guide: https://trove.cyberskyline.com/41570c1e3a974808a838a9f83c2f6d4a (login required)_

## Technique

Export the CAN frames; isolate ID 589 and decode bytes 3-4 as the speed in kph, convert to mph, and aggregate for the unique CAN ID count, the number of speed messages, and the maximum mph.
