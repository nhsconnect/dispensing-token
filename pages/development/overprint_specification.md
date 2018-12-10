---
title: Overprint Specification
keywords:
tags: [development]
sidebar: overview_sidebar
permalink: overprint_specification.html
summary: "Requirements for the content and layout of the EPS dispensing token"
---

## Dispenser Name, Address and Code (top left) ##
The dispensary name, address and code must be printed when the dispensing token is used for the purposes of capturing a patient / representative declaration for charge or charge exemption.

The dispensary name, address and code must not be printed when the dispensing token is printed and given to the patient to allow them to visit a different dispensary for their medication with the prescription being returned to the EPS. As no dispensing event has occurred, this information about the dispensary cannot be printed at this time.

When the dispensary details are printed:

  - The dispensary name and address printed must be the same as used on the BSA submission document
  - The dispensary name must be printed on the top line of this areas
  - The font should be Arial [bold] 7.5pt and left justified
  - There should be a one line gap between the dispensary name and the start of the dispensary address.
  - The address should be printed over 3 address lines
  - The postcode must be printed below the last address line
  - The community pharmacy 5 character organisation code must be printed below the postcode. For dispensing doctors this will be a 6 digit code
  - The name, address and code must not impinge on the patient details

## Patient Details ##

### Age and DoB ###
![Age and DoB](images/token_patient_detail_age.png)

The age and date of birth must be printed as a numeric in the appropriate area under the relevant field name.

The date must be printed in the format `dd/mm/yyyy`.

The font should be Arial [bold] 7.5pt and centred horizontally.

Vertically the details should be positioned below the relevant heading (within 4mm).

### Title, Forename, Surname, Address & NHS Number ###
![Title, Forename, Surname, Address & NHS Number](images/token_patient_detail.png)

The patient name, address and NHS number must be printed in the top right hand box.

The font should be Arial [bold] 7.5pt.

There should be a blank line between the name and the first line of the address.

The address must be printed on no more than five address lines.

The postcode should appear on the same line as the last address line and should be left aligned with the NHS number.

There should be a blank line between the last line of the address and the NHS number.

The NHS number should be right justified and there should be 5mm between the last character and the edge of the prescription.

*Notes*
  1. The use of capital letters is not mandatory.
  2. The format of the patient name should be agreed between the user and the system supplier.
  3. If the patient name and/or address details do not fit into the designated field, a set of ‘rules’ should be agreed between the user and the system supplier which must not involve the wrapping of text.

## Endorsements Area (left-hand side) ##

No overprinting requirements.

*Notes*
  * The dispensing token is not used to support the dispensing reimbursement process therefore no endorsements are required to be printed
  * Note that prescriber endorsements must be printed, see the Prescribed Medication area.

## Prescribed Medication ##
![Prescribed Medication area](images/token_line_item.png)
### Token Description ###
The FP10DT stationery is pre-printed with the token description at the top of this area.

If FP10SS stationery is being used by a dispensing doctor then the text `DISPENSING TOKEN` must be printed at the top of this area. The text must be right aligned and there should be a 5mm gap between the last character and the edge of the box.

For repeat dispensing prescriptions the text `Repeat Dispensing Issue X of Y` should be printed at the top of the area, where X is the current issue number and Y is the total number of authorised issues.

### Prescribed Medications Items ###
{% include note.html content="This section is based on the BNF section *Prescription Writing – Computer-issued prescriptions*, containing recommendations from the Joint GP Information Technology Committee." %}
All text should be Arial [bold] 7.5 to 10pt. The size of the font may be adjusted to ensure the text will fit on to the correct number of lines.

There must be a one line gap between the Token Description and the prescribed medication item details.

The prescribed medication items text should be left aligned with a 5mm gap between the first and last character and the edge of the box.

For each prescribed medication item, the following must be printed:

  * Dictionary of Medicines and Devices (dm+d) Product Name
    - The dm+d product name is made up of drug, strength and formulation e.g. `Aspirin 300mg Tablets`
  * Prescriber Endorsements 􏰀
  * Quantity
    - Quantity should not be contained in brackets
  * Dosage/Frequency

The medication item description, prescriber endorsements and quantity should be printed on the same line, wrapping onto a second line if required.

Where the medication item is a Schedule 2 or 3 controlled drug then the quantity must be printed in both figures and words. The quantity in words is contained within the “originalText” element for the prescribed item. It is common practice on paper CD prescriptions to display the quantity in words within parentheses. A complete quantity expressed in words and figures would be:
`28 (twenty eight) capsule`

The dosage/frequency instructions should be printed on a separate line to medication item description and quantity.

Additional instructions for the dispenser pertinent to the prescribed medication item should be printed on a separate line below the dosage/frequency. Note this does not include the repeat medication information provided within `<medication>` tags or specific patient information provided within `<patientInfo>` tags.

There must be a one line gap between the medication item details and the medication item separator.

Each medication item should be separated by a solid or hashed horizontal line or similar separator.

Any remaining lines between last prescribed medication item and the bottom of the box should be printed with an ‘X’ character, or similar, centre aligned within the box.

## Date ##
![Dispensing date](images/token_signature.png)

The date the prescription was dispensed must be printed in the format `dd/mm/yyyy`.

The font should be Arial [bold] 7.5pt and centred horizontally.

## Signature Area ##
![Signature Area](images/token_signature.png)

The FP10DT stationery signature area is pre-printed and no additional information must be printed in this area.

If the FP10SS stationery is being used, the following text must be printed within the signature area: `DISPENSING TOKEN - Not to be used as a prescription, even if signed by an authorised prescriber.`

## Right Hand Column ##

### Prescription Identifier Barcode ###
The prescription identifier must be printed in this area.

The barcode must be a 1 dimensional (1D) Code 128 barcode.

The barcode must be printed vertically.

The dimensions of the barcode must be within the following tolerances:

  * Width &ge; 8mm and &le; 12mm
  * Height &ge; 55mm and &le; 68mm

![Barcode size](images/barcode_size.png)

Where possible, the maximum dimensions should always be adhered to.

![Barcode position](images/barcode_margin.png)

The barcode must be positioned vertically at least 8mm from the top and bottom of the box in which it appears.

The barcode must be positioned horizontally at least 1mm from the left and 6mm from the right hand edge of the form area.

The barcode must be printed directly onto the form (i.e. not an adhesive label).

### Prescription Identifier ###
The prescription identifier must be printed vertically as a human readable text string within the right hand column.

The font of the prescription identifier should be at least Arial [bold] 7.5pt.

The prescription identifier must be positioned vertically at least 8mm from the top and bottom of the box in which it appears.

The prescription identifier must be positioned at least 1mm from the right of the bar code.

## Prescriber Address Box ##

![Prescriber Address Box](images/token_prescriber_detail.png)

The prescriber details printed in this area will vary depending on the prescriber type and employer.

The prescriber name must be printed on the top line of the address box.

There should be a one line gap between the prescriber name and the start of the prescriber address.

The font should be Arial [bold] 7.5pt and left justified, except Prescribing Code, Postcode, the Practice ODS Code and Commissioner's ODS Code.

The postcode (Arial [bold] 7.5pt) should appear on the same line as address line 3 (GP prescribers), line 2 (non GP prescribers) but should be left aligned with the Prescribing Code, the Practice Code and Commissioners ODS Code (as appropriate).

There does not need to be a 5mm gap between the last character of the postcode and the edge of the box.

The Commissioners ODS Code should appear on the same line as the Commissioners name but should be left aligned with the Prescribing Code, the Practice Code and the Postcode.

### Font and Position ###
The font should be Arial [bold] 12pt.

The Prescriber Code should be printed on the same line as the prescriber name.

The text must be positioned towards the right of the box.

The Prescribing code, Commissioners ODS code (e.g. a CCG organisation code), practice code and postcode should be left aligned with each other.

There must be a 5mm gap between the last character of the longest data item and the edge of the box.

### GP Address Layout ###
This includes locum GPs and trainee doctors
```
DR A JONES                          PRESCRIBER CODE
GP ADDRESS LINE 1
GP ADDRESS LINE 2
GP ADDRESS LINE 3                   POST CODE               
TELEPHONE NUMBER
COMMISSIONERS NAME                  COMMISSIONERS CODE
```
### Practice Employed Non-GP Prescriber Address Layout ###
```
MRS A JONES                         PRESCRIBER CODE
GP SENIOR PARTNER NAME              PRACTICE CODE
GP ADDRESS LINE 1
GP ADDRESS LINE 2                   POST CODE
TELEPHONE NUMBER
COMMISSIONERS NAME                  COMMISSIONERS CODE
```
### Non-Practice Employed Non-GP Prescriber Address Layout ###
```
MRS A JONES                         PRESCRIBER CODE
COMMISSIONERS NAME                  COMMISSIONERS CODE
*PATIENT’S PRACTICE CODE*           PRACTICE CODE
COMMISSIONERS ADDRESS LINE 1
COMMISSIONERS ADDRESS LINE 2        POST CODE
*PRESCRIBER CONTACT NUMBER*         TEL NUMBER
```
{% include note.html content="Elements shown in \*asterisks\* must appear verbatim, minus asterisks" %}
