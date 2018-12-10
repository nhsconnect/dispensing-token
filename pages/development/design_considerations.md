---
title: Design Considerations
keywords:
tags: [development]
sidebar: overview_sidebar
permalink: design_considerations.html
summary: "Description of the design considerations within the EPS"
---


## Stationery ##

New pre-printed stationery to support the EPS is used and circulated to pharmacy for use in  EPS Release 2. The stationery uses the formal title *FP10DT0407*.

Dispensing Doctors will also be required to print a dispensing token in certain circumstances and as they already use the FP10SS stationery for prescribing, that stationery can be used in the place of the FP10DT stationery.

## Use of NHS Number ##
The use of a patient’s NHS Number is mandated when using the EPS therefore the NHS Number must be printed on the dispensing token in all cases.

## Address Formatting ##
Address lines within the national Demographics Service are recorded as 5 address lines plus a postcode. All address lines must be printed on the token.
The GP’s address is printed as 3 address lines plus a postcode. Implementers are advised to use the first 3 address lines and ignore additional address lines if these exist.
The address of a non-GP prescriber is printed over 2 address lines. Implementers are advised to use the first 2 address lines and ignore additional address lines if these exist.

## Prescription Identifiers ##
The dispensing token is required to contain the Prescription Identifier in a machine-readable barcode format and as a human readable character string. The token stationery allows the Prescription Identifier to be printed vertically within the right hand column.
For EPS Release 2, the Prescription Identifier is an 18 character string with additional hyphen characters to separate the string into 3 x 6 character blocks.
Example Prescription Identifier: `83C40E-A23856-00123C`d
