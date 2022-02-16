# sigrok_emmc_decoder
Created from sigrok_sdcard_sd decoder, a sample emmc decoder for sigrok

## eMMC Protocol
Currently, the decoder is created based on eMMC protocol Ver 5.1 without HS400 or DDR support, nor does it have data decoding. It supports command decoding.
CMD is defined using eMMC protocol chapter 6.10.4 and 6.12

## Changes since the fork
1. The decoder was updated to run in a more recent version of PulseView, using sdcard_sd as template.
2. Updated the command decoding to cover all the commands and responses from the eMMC v5.1 spec.
3. Fixed up some discrepancies, updated mismatching fields in commands and responses and performed some cleanup.
4. Minor touch ups, like decoding the device CURRENT_STATE field in the R1 response.

## TODOs
1. Find out how the Application-specific commands (i.e. ACMDs) are defined (currently just copied them over from the sdcard_sd decoder).
