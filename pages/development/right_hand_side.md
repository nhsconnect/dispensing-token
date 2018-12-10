---
title: Dispensing Token Right Hand Side
keywords:
tags: [development]
sidebar: overview_sidebar
permalink: right_hand_side.html
summary: "Requirements for the content of the detachable right hand side of the dispensing token"
---
Both the FP10SS and FP10DT stationery have a plain right hand side. This area could be used to meet requirements to make clinical information available to the patient where required.

![Token Right Hand Side](images/token_rhs.png)

The patient name, address, postcode, date of birth and NHS number must be printed at the top.

The prescribing organisation name and address must be printed at the top, clearly distinct from the patient demographic information printed.

Authorised repeat medication provided within `<medication>` tags must be printed.

Specific patient information provided within `<patientInfo>` tags must be printed.

Where multiple pages of right-hand side information are printed then at a minimum, the patient name and date of birth, plus the prescribing organisation name, must be printed at the top of each subsequent page.

The current page number and total number of pages must be printed at the bottom.

When a dispensing token is printed purely to support local dispensing processes and therefore not required for either a patient exemption/payment declaration or to make information available to the patient, i.e. their repeat medications re-order form, then printing a right hand side on the token can be optional. This would prevent unnecessary pages printed if the patient has many authorised repeat medications.
