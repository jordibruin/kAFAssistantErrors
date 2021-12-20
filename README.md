<!-- markdownlint-configure-file {
  "MD013": {
    "code_blocks": false,
    "tables": false
  },
  "MD033": false,
  "MD041": false
} -->

<div align="center">

# kAFAssistantErrors
  
An overview of errors thrown by kAFAssistant and the Apple SpeechRecognizer 
  
This repo aims to be an overview of the errors that you can run into while using the Speech framework on Apple devices. Since it uses internal frameworks (kAFAssistant) that are not documented I thought it would be nice to have an overview.


[Overview](#overview) •
[Errors](#errors) •
[Links](#links)

</div>

# Overview

Domains
SiriSpeechErrorDomain 
EARErrorDomain

### 0XX errors

3 - Recognition was unsuccessful

### 1XX errors

### 2XX errors

201 - 

203 or 1107 = too much silence (so recognition gets aborted)

203 - Retry / Error

209 - The operation couldn’t be completed. (kAFAssistantErrorDomain error 209.)

[216 - The operation couldn’t be completed.](#216)

### 3XX errors

301 - Recognition request was canceled

### 6XX errors

601 = speech recognition not supported (iPad Air 2 bug)

### 11XX errors

1101 = some other problem I'm not sure about

1103 - no local speech files (for offline speech recognition)

1107 - too much silence (so recognition gets aborted)

1110 - No Speech Detected


# Errors

### 203 - Retry (or just "Error")

Cause:

Triggered after 60 seconds of no sound detected by the Speech Recognizer. It stops the recognition for me afterwards.

Solutions:

Start a new recognitionTask after this error is thrown


### 216
The operation couldn’t be completed.

Cause:

Explanation of why it happens

Solutions:

Explanation of some approaches to solve this





# Links

* [Speech Recognizer Documentation](https://developer.apple.com/documentation/speech)
