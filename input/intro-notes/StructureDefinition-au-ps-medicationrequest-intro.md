{% include comparison-note-boilerplate.md %}

### Profile specific implementation guidance
- See the [Medicine Information](https://build.fhir.org/ig/hl7au/au-fhir-core/medicine-information.html) page in AU Core for guidance on how medicinal product identification can be structured in FHIR conformant to AU Patient Summary.
- When recording "self-prescribed" medication, `MedicationRequest.requester` references the Patient or RelatedPerson as the prescriber.
- MedicationRequest resources can represent a medication using either a code with `MedicationRequest.medicationCodeableConcept`, or reference a [Medication](http://hl7.org/fhir/R4/medication.html) resource with `MedicationRequest.medicationReference`.
  - When referencing a Medication resource, it is preferred the resource is [contained](http://hl7.org/fhir/R4/references.html#contained) but it may be an external resource


<div class="stu-note">
Conversion to derive from AU Core instead of AU Base is delayed until AU PS Encounter is converted due to build errors when publishing if this referenced profile does not derive from AU Core.
</div>