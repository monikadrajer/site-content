# C-CDA R2.1/R1.1/MU2 Release Notes:

The **SITE C-CDA R2.1 Validator Release for Aug 1st 2017**, based on the [July 25th 2017 MDHT Release](https://github.com/mdht/mdht-models/releases/tag/v3.0.0.20170725_Consol2), contains the following fixes:

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer no longer causes an error requiring conformance to the Mental Status Organizer (V3). All past issues with the structure of Mental Status Observation (V3), Mental Status Organizer (V3), and Result Observation should be resolved.

*   Other fixes and updates:
    *   DS4P objectives are fully operational

**Known Issues in the release that impact users:**

*   Sending a non-DS4P document for DS4P validation (using a DS4P objective) returns a service error. Until this is resolved, please only test documents with DS4P data when selecting a DS4P objective.

***

# Prior Releases:

# C-CDA R2.1/R1.1/MU2 Release Notes:

The **SITE C-CDA R2.1 Validator Release for June 26th 2017**, based on the [June 22nd 2017 MDHT Release](https://github.com/mdht/mdht-models/releases/tag/v3.0.0.20170622_Consol2), contains the following fixes:

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   Fixed 'CALLBCK' typeCode identification in Consultation Note (R2.1) participant

**Known Issues in the release that impact users:**

*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

The **SITE C-CDA R2.1 Validator Release for May 30th 2017**, based on the [May 24th 2017 MDHT Release](https://github.com/mdht/mdht-models/releases/tag/v3.0.0.20170524_Consol2), contains the following fixes:

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   As a result of an issue noticed in Immunization Medication Information/manufacturedMaterial/code, Vaccine Administered Value Set no longer throws an error for the valid code '166'

**Known Issues in the release that impact users:**

*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

The **SITE C-CDA R2.1 Validator Release for March 27th 2017**, based on the [March 23rd 2017 MDHT Release](https://github.com/mdht/mdht-models/releases/tag/v2.6.3.20170323_Consol2), contains the following fixes:

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   See ERRATA 596 relax/revert

*   Other fixes and updates:
    *   Performance improvements

*   The following ERRATA were incorporated:
    *   596 relax/revert
    *   ERRATA 596 relax/revert
        *   Relax Errata 596 in R1.1 Smoking Status Observation effectiveTime. Changed error to warning for use of TS attributes.

**Known Issues in the release that impact users:**

*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

***

# C-CDA R2.1 Release Notes:

The **SITE C-CDA R2.1 Validator Release for December 20th 2016**, based on the [December 13th 2016 MDHT Release](https://github.com/mdht/mdht-models/releases/tag/v2.5.22.20161213_Consol2), contains the following fixes:

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   See ERRATA 1220 update

*   Other fixes and updates:
    *   The Criticality Observation entry template [observation: identifier urn:oid:2.16.840.1.113883.10.20.22.4.145 (open)] is now enforced as per the latest C-CDA R2.1 IG requirements. Previously this new template was not being validated.
    *   Adjusting for CONF:1198-8738s 'such that it' clause, a warning versus an error is now displayed when when typeCodes other than LOC are used in EncounterActivities/participant/Service Delivery Location (previously an error for CONF:1198-8740, which follows 8378)

*   The following ERRATA were incorporated:
    *   710, 747, 792, 806, 808, 872, 964, 986, 1018, 1054, 1220 Update
    *   ERRATA 710
        *   Allergy - Intolerance Observation and Substance or Device Allergy - Intolerance Observation now include a SHOULD requirement for Criticality Observation and a SHOULD NOT requirement for Severity Observation
    *   ERRATA 747
        *   The USRH Patient address codeSystem in the Country valueSet was updated from the incorrect OID of 2.16.840.1.113883.3.88.12.80.63 (which matches the valueSet OID) to the correct OID of 1.0.3166.1
    *   ERRATA 792
        *   The code attributes in Family History Organizer subject administrativeGenderCode and Tobacco Use value are no longer treated as mandatory/nullFlavor is allowed
    *   ERRATA 806
        *   USRH languageCode and patient/languageCommunication/languageCode are selected from the most up-to-date version of ValueSet Language urn:oid:2.16.840.1.113883.1.11.11526 DYNAMIC
    *   ERRATA 808
        *   Reverts the name attribute in the USRH Patient from Person Name to the US Realm Patient Name (PTN.US.FIELDED) type
    *   ERRATA 872
        *   The Criticality Observation/@code terminology requirement was updated from "NEW-LOINC-CRITICALITY" to “82606-5” Allergy or intolerance criticality. The codeSystem remains the same (LOINC).
    *   ERRATA 964
        *   Vital Sign Observation code/@code has different requirements due to the following Vital Sign Result update: Add 29463-7 Body weight and remove 3141-9 Body weight Measured.
    *   ERRATA 986
        *   Vital Sign Observation code terminology was updated to match the latest data for the (HITSP) Vital Sign Result (Type) Value Set from VSAC
    *   ERRATA 1018
        *   A typeCode of type REFR is now specified for all Nutrition Recommendation entryRelationships
    *   ERRATA 1054
        *   Allows the use of nullFlavor on Procedure Activity Procedure targetSiteCode code by removing the mandatory binding
    *   ERRATA 1220 Update
        *   Errata 1220 is identified in the related conformance rule based error messages as DSTU:1220 instead of DSTU:NEW as it is now official errata post implementation

**Known Issues in the release that impact users:**

*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

***

# C-CDA R1.1 Release Notes:

The **SITE C-CDA R1.1 Validator Release for September 2016**, based on the [August 19th 2016 MDHT Release](https://github.com/mdht/mdht-models/releases/tag/v2.5.18.20160819_Consol1), contains the following fix:

*  Reverted Administrative Gender (HL7 V3) value set code UNK to UN

**Known Issues in the release that impact users:**

*  None

***

**Defects fixed in the SITE C-CDA R2.1 Validator Release for November 17th 2016 (November 15th 2016 MDHT Build):**

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   See ETT related ERRATA 1220
    *   The code C38313 Vaginal Route of Administration is now allowed in the Medication Route FDA Value Set 2.16.840.1.113883.3.88.12.3221.8.7 DYNAMIC. This fix is in response to an error using the code in Medication Activity/routeCode (CONF:1098-7514).

*   Other fixes and updates:
    *   None

*   The following ERRATA were incorporated:
    *   1220
    *   ERRATA 1220 (identified in conformance rules as DSTU:NEW as it wasn't official errata yet when it was implemented):
        *   The Vital Sign Observation (V2) interpretationCode requirement is now selected from ValueSet Observation Interpretation (HL7) 2.16.840.1.113883.1.11.78 DYNAMIC instead of the STATIC version 2014-09-01\. In relation to an ETT issue, due to this change, the code HH 'Critical high' is now allowed.

**Known Issues in the release that impact users:**

*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

**Defects fixed in the SITE C-CDA R2.1 Validator Release for October 31st 2016 and hotfixed on November 7th 2016 (November 15th 2016 MDHT Build):**

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   See ETT related errata 1047
    *   Added missing C38290 'OTHER' code to the Medication Route FDA urn:oid:2.16.840.1.113883.3.88.12.3221.8.7 ValueSet which resolves a noted routeCode issue in Immunization Activity
    *   The COMP entryRelationship in Immunization Activity sub-requirements (Substance Administered Act CONF:1198-31514 and inversionInd CONF:1198-31512) are now treated as warnings instead of errors due to the 'such that it' clause causing the parent 'SHOULD' severity to override the child 'SHALL' severities

*   Other fixes and updates:
    *   Updated Medication Activity administrationUnitCode terminology (CONF:1098-7519) from Medication Product Form Value Set 2.16.840.1.113883.3.88.12.3221.8.11 to AdministrationUnitDoseForm 2.16.840.1.113762.1.4.1021.30
    *   Participants in the header which are not of type IND are no longer enforcing CONF:1198-10006\. This issue was previously causing an error on unrelated participants of type VRF in the HL7 provided C-CDA_R2_Care_Plan.xml.
    *   The Birth Sex Template value element now enforces required terminology (ValueSet ONC Administrative Sex urn:oid:2.16.840.1.113762.1.4.1 STATIC)
        *   An HL7 unofficial errata in the Birth Sex Observation proposal and the Companion Guide associates ONC Administrative Sex (2.16.840.1.113762.1.4.1) value set with AdministrativeSex (2.16.840.1.113883.18.2) code system instead of AdministrativeGender (2.16.840.1.113883.5.1). The validator has been updated/reverted to use AdministrativeGender.
    *   All R2.1 errata are now identified within their respective returned conformance message by the following format: 'DSTU:comment#'
    *   USRH/author/time/@value minimum length (CONF:81-10127) is enforced along with the other relevant US Realm Date and Time (DTM.US.FIELDED) requirements for the attribute (CONF:81-10128, 10129, and 10130)

*   The following ERRATA were incorporated:
    *   867, 963 (latest HL7 update), 1047
    *   ERRATA 867:
        *   Author Participation is no longer required in Goal Observation. CONF:1098-30995 was changed from a SHALL to a SHOULD severity
    *   ERRATA 963:
        *   The Result Observation (V3) interpretationCode requirement is now selected from ValueSet Observation Interpretation (HL7) 2.16.840.1.113883.1.11.78 DYNAMIC instead of the R2.1 AUG 2015 IG-listed version of 2014-09-01 (or the prior errata comment update to an unknown STATIC version)
    *   ERRATA 1047:
        *   The @moodCode value set in Planned Encounter (V2) was updated from Planned moodCode (Act/Encounter/Procedure STATIC 2011-09-30 to STATIC 2014-09-01, which allows the use of the APT code

**Known Issues in the release that impact users:**

*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

**Defects fixed in the SITE C-CDA R2.1 Validator Release for September 2016 (August 16th 2016 MDHT Build):**

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   See ETT related errata 1017 and 1045 (implementation requested or errata created via discussion in ETT forum)
    *   Fixed typeCode identification issue for performers in Continuity Of Care Document level validations

*   The following ERRATA were incorporated:
    *   1017, 1038, 1045
    *   ERRATA 1017:
        *   The severity for the id in Risk Concern Act (CONF:1198-32223) was updated from 1..1 to 1..*
    *   ERRATA 1038:
        *   Comment Activity now uses the Author Participation template as opposed to an author with more specific requirements. In addition, the severity has been updated from MAY to SHOULD.
            *   New rule:
                *   SHOULD contain zero or one [0..1] Author Participation (identifier: urn:oid:2.16.840.1.113883.10.20.22.4.119) (CONF:NEW, DSTU:1038)
    *   ERRATA 1045:
        *   Adds multiple rules which, among other things, allows additional effectiveTime elements in Planned Medication Activity (such as one to record frequency) as long as one of them is of type IVL_TS or TS

**Known Issues in the release that impact users:**

*   US Realm Header/author/time/@value minimum length is not enforced
*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

**Defects fixed in the SITE C-CDA R2.1 Validator Release for August 2016 (July 25th 2016 MDHT Build):**

*   The following defects identified in Google Groups for the TTT or ETT were corrected:
    *   See errata 820 (implementation requested by ETT user issue)
    *   See errata 963 (created in response to ETT user issue)
    *   The Caregiver Characteristics value/@code requirement text for CONF:14600 was changed to read value/@code instead of the incorrect code/@code
    *   The requirements for a Patient Referral Act with an entryRelationship with a typeCode equal to SUBJ are no longer applied to all of the entryRelationships within the act
    *   Reverted Administrative Gender (HL7 V3) valueSet code UNK to UN
    *   A Mental Status Organizer (V3) can now wrap a Mental Status Observation (V3) as long as the R1.1 template Cognitive Status Result Observation is not defined in the XML
    *   The implementation of Medical Equipment Organizer for CONF:1098-32380 now allows for the existence of both a Non-Medicinal Supply Activity (V2) and a Procedure Activity Procedure (V2). The validator still requires at least one but allows for both.
    *   Planned Supply (V2) no longer enforces rules '1098-' 32092, 32093, or 32096 unless a relevant product or participant exists
    *   Fixed typeCode identification issues for participant and performer types in the Transfer Summary document
    *   Fixed documentationOf/serviceEvent/performer typeCode identification issues for Operative Note (V3) and Procedure Note (V3) as well as the root-level participant for Procedure Note (V3)

*   Other fixes and updates:
    *   Whether set explicitly or by default, Vital Sign Observation no longer fires an error for a value element with a valid unit attribute equal to 1
    *   Author Participation / assignedAuthor / representedOrganization no longer requires a classCode equal to ORG. The outdated R2.0 requirement (CONF:1098-31477) was removed.
    *   The Birth Sex Observation template (2.16.840.1.113883.10.20.22.4.200:2016-06-01) is now recognized and enforced. It is currently implemented in the Social History Section as such:
        *   MAY contain zero or more [0..*] entry (CONF:1198-NEW) such that it
            *   SHALL contain exactly one [1..1] Birth Sex Observation (identifier: urn:hl7ii:2.16.840.1.113883.10.20.22.4.200:2016-06-01) (CONF:1198-NEW)

*   The following ERRATA were incorporated:
    *   820, 963, 995, 1015
    *   ERRATA 820:
        *   For backwards compatibility purposes, the Discharge Medication (V2) entry was versioned to Discharge Medication (V3) with the following notable changes:
            *   The extension was updated from 2014-06-09 to 2016-03-01
            *   The root-level code requirement was updated from 75311-1 to 10183-2 and 75311-1 was added instead as a required translation
    *   ERRATA 963:
        *   The Result Observation (V3) interpretationCode requirement is now selected from a recently updated version of ValueSet Observation Interpretation (HL7) which contains a new set of codes
    *   ERRATA 995:
        *   The R2.1 version of Immunization Medication Information / manufacturedMaterial / lotNumberText was reverted to a SHOULD instead of a SHALL severity
    *   ERRATA 1015:
        *   In reference to the id located in Continuity of Care Document (CCD) (V3) / documentationOf / serviceEvent / performer / assignedEntity:
            *   If the assignedEntity is an assignedPerson:
                *   Multiple id elements with identifiers which differ from the NPI are valid as long as at least one of the id elements has a root equal to 2.16.840.1.113883.4.6 National Provider Identifier (CONF:1198-32484), or, a valid nullFlavor or nullFlavor and extension combination is provided
                *   The requirement for the NPI specifically is a SHOULD instead of a SHALL

**Known Issues in the release that impact users:**

*   US Realm Header/author/time/@value minimum length is not enforced
*   Using a Mental Status Organizer (V3) with a Mental Status Observation (V3) while simultaneously defining the R1.1 template Cognitive Status Result Organizer causes an error requiring conformance to the Mental Status Organizer (V3). To resolve this issue, either remove the R1.1 template II, or, place the observation directly in the Mental Status Section. Note: A future release will allow the R1.1 template II.

***

**Defects fixed in the March 23rd 2016 MDHT Build:**

*   The following defects identified in google groups were corrected:
    *   In Procedure Activity Act, CONFs 7736 and 7737 no longer fire errors inaccurately which require the addr and telecom elements to exist when the representedOrganization element is not present.
    *   Documents sent in for validation without a v3 namespace, although illegal, can now return some schema related results as well as a relevant error message.
    *   Added codes 150 and 163 to Vaccine Administered Value Set 2.16.840.1.113883.3.88.12.80.22.
    *   Updated Administrative Gender (HL7 V3) valueSet code UN to UNK.

*   Other fixes and updates:
    *   The Unstructured Document Template ID was updated from 2.16.840.1.113883.10.20.21.1.10 to 2.16.840.1.113883.10.20.22.1.10.
    *   Loosened CONF:9929 terminology requirements by adding the missing IG specified HL7 Discharge Disposition codeSystem as an option for sdtc:dischargeDispositionCode.
    *   Message generation issues in US Realm Header for MU2 validation (including languageCommunication) have been resolved and now produce clear non-repeating output.
    *   The Discharge Summary constraints for CONF:10055 and CONF:9928 are handled correctly now. Note: This fix will only be noticed when running document-level validation (non-specific C-CDA).
    *   MedicationActivity/administrationUnitCode is now validating that codes are selected from the Medication Product Form 2.16.840.1.113883.3.88.12.3221.8.11 valueSet and that the codeSystem is NCI Thesaurus 2.16.840.1.113883.3.26.1.1.

*   The following ERRATA were incorporated:
    *   240 update, 381, 506, 596, 596 20160311 update
    *   ERRATA 240 update:
        *   Updated NUBC UB-04 FL17-Patient Status valueSet OID to 2.16.840.1.113883.3.88.12.80.33 with a codeSystem reference of 2.16.840.1.113883.6.301.5.
    *   ERRATA 381:
        *   AllergyObservation/value allows SNOMED-CT and new codes and is less constrained than previously. Substance-Reactant for Intolerance 2.16.840.1.113762.1.4.1010.1 allows a broader range of code systems.
    *   ERRATA 506:
        *   Precondition for Substance Administration now inherits directly from criterion instead of precondition. This change affects structure requirements within Medication Activity and Immunization Activity.
    *   ERRATA 596:
        *   Smoking Status effectiveTime is restricted to the TS data type and therefore no longer requires a low.
    *   ERRATA 596 20160311 update:
        *   The Smoking Status Observation and Tobacco Use templates are now fully aligned with their C-CDA R2 counterparts with the exception of the extension, id element requirement, and a backwards compatibility change to the codes. For code, ASSERTION is still allowed in R1.1 in addition to the new unique LOINC codes.

**Known Issues in the release that impact users:**

*  None
