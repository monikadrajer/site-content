#### Rules (rubrics)

*   The rules were created in a combined effort between the ONC, HL7, vendors, and developers. They are meant to be continually improved. The rules provide a basis for determining where best-practices can be implemented, control the underlying purpose of the application, and allow for a final score and report to be provided. A full set of the the rules used, their related sections, and the XPath to their elements can be found [here](/scorecard/resources/LOINC.csv).

#### Scoring Criteria

*   Each C-CDA document is scored and graded for a set of enhanced interoperability rules developed by HL7. A higher score (grade) means that information is coded with appropriate structure and semantics and hence has a better chance of interoperating with disparate systems. The maximum score is 100 points and the grades are:
    * A+ (more than 94 points)
    * A- (90 to 94 points)
    * B+ (85 to 89 points)
    * B- (80 to 84 points)
    * C (70 to 79 points)
    * D (less than 70 points)
    
*   Points lost/gained are dynamic and are dependent on the number of elements the document has at each rubric level. Each rule is awarded a maximum point of 1 and minimum point of 0. Each rule will be scored based on the number of elements passing in each section. 
    * At Rubric Level:
        * As an example: A given section has 20 effectiveTime elements, out of which 6 are failing. This is scored 14/20=0.7, and a total of 6 issues are displayed.
    * At Section Level:
        * The Scorecard averages the total percentage calculated for each rule and converts it to a grade which is displayed in the UI.
    * At Document Level:
        * The final score is calculated by the total number of elements passed divided by the total number of elements scored (across all rules in the document) and given a percentage. The grade is derived from this result based on the scoring criteria.
        
*   Additional Guidance to Interpret the Scorecard Results and Achieve Higher Grades
    * Scorecard Grade:
        * The Scorecard grade is a quantitative assessment of the data quality of the submitted document. A higher grade indicates that HL7 best practices for C-CDA implementation are being followed by the organization and has higher probability of being interoperable with other organizations. The grades are derived from the scores as follows: A+ ( > 94), A- ( 90 to 94), B+ (85 to 89), B- (80 to 84), C (70 to 79) and D (< 70).
    * Scorecard Issues:
        * A Scorecard Issue identifies data within the document which can be represented in a better way using HL7 best practices for C-CDA. This column should have numbers as close to zero as possible. The issues are counted for each occurrence of unimplemented best practice. For example, if a Vital Sign measurement is not using the appropriate UCUM units then each such occurrence would be flagged as an issue. A provider should work with their health IT vendor to better understand the source for why a best practice may not be implemented and then determine if it can be implemented in the future. Note: Scorecard Issues will be listed as 'N/A' for a clinical domain, when there is no data for the domain or if there are conformance or certification feedback results.
    * Conformance Errors:
        * A Conformance Error implies that the document is non-compliant with the HL7 C-CDA IG requirements. This column should have zeros ideally. Providers should work with their health IT vendor to rectify the errors.
    * Certification Feedback:
        * A Certification Feedback result identifies areas where the generated documents are not compliant with the requirements of 2015 Edition Certification. Ideally, this column should have all zeros.Most of these results fall into incorrect use of vocabularies and terminologies. Although not as severe as a Conformance Error, providers should work with their health IT vendor to address feedback provided to improve interoperable use of structured data between systems.
