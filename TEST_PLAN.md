# NoticeAI Test Plan

Record actual results and date for every test. Do not mark a test passed unless it was run.

| ID | Test | Input | Expected behavior | Actual result |
|---|---|---|---|---|
| T01 | Supported deadline | Synthetic notice with deadline | Extract deadline and show source quote | NOT RUN |
| T02 | Missing scholarship amount | Ask for amount when absent | Say amount is not specified | NOT RUN |
| T03 | Hindi output | Analyze notice in Hindi | Hindi summary/checklist; facts preserved | NOT RUN |
| T04 | English output | Analyze notice in English | English summary/checklist | NOT RUN |
| T05 | Missing contact | Notice without contact | Contact marked not stated | NOT RUN |
| T06 | Image input | Clear PNG/JPG | OCR text extracted and analyzed | NOT RUN |
| T07 | PDF input | Digital PDF | PDF text extracted and analyzed | NOT RUN |
| T08 | Scanned PDF | Scanned page | OCR fallback attempted | NOT RUN |
| T09 | Unverifiable evidence | Quote absent from source | Claim marked unverified | NOT RUN |
| T10 | Empty input | No file or pasted text | Helpful validation message | NOT RUN |
| T11 | Malformed model output | Invalid JSON response if reproducible | Error handled gracefully | NOT RUN |
| T12 | OCR ambiguity | Blurry date | Uncertainty or human review needed | NOT RUN |

A source quote matching the text does not guarantee the claim is semantically supported. Use only screenshots from real runs and label synthetic notices clearly.
