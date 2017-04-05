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

#### Rules (rubrics)

*   The rules were created in a combined effort between the ONC, HL7, vendors, and developers. They are meant to be continually improved. The rules provide a basis for determining where best-practices can be implemented, control the underlying purpose of the application, and allow for a final score and report to be provided. A full set of the the rules used, their related sections, and the XPath to their elements can be found here:
    * http://www.insert-a-local-or-external-link-to-download-the-spreadsheet-here.com
