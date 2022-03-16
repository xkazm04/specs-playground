# Knowledge bank

Tree structure with pre-processed data - knowledge to be easily managed and displayed by internal or external users

## Data structure 

JSON hiearchy to dynamically cover multi-level selection tree and develop specific tree branches instead of large flat-structured document

Attribute | Data type | Example
---------|----------|---------
 `id` | uuid | b5d50118-17c7-489d-a7aa-47901d97916a
 `children` | array with objects | nested JSON tree
 `value` | string | What is meaning of life?
 `description` | string | Solution of problem
 `useCaseType` | string (enum) | Input
 `chatbotId` | B3 | C3
 `label` | string | Question
 `reference` | string TBD | URL reference

> Need to implement reference, it could server as integration connector to another apps in addition to chatbotId

### useCaseType
- `input` - option selection to enhance JSON tree
- `code snippet` - code example related with problem solution

## Use case examples
This universal structure could serve for multiple use cases inside Tatum or anywhere else 

### Buidl buddy 
Tool to navigate user inside vast documentation

```json tree
{
  // First level - Select high level category
  "id": "85e72ebf-7fbd-44fb-a911-c3d12aee9aa8",
  "label": "Choose category",
  "useCaseType": "input"
  "value": "",
  "children": [
    {
  // 2nd,3rd,4th level - Specify detailed path, question
      "id": "952ec8bc-fe2a-4b31-bd0e-28b55138214f",
      "label": "Select blockchain",
      "value": "Blockchain",
      "children": [
        {
          "id": "94c975d6-3cc6-4d67-8152-82a178d272a2",
          "label": "Find service",
          "useCaseType": "input"
          "value": "Algorand (ALGO)",
          "children": [
            {
              "id": "f7508077-483d-4633-8a87-3bef650c4153",
              "label": "",
              "useCaseType": "input"
              "value": "Access Algod GET node endpoints",
              "children": [
                {
  // Final level - Define answer, references
                  "id": "bfc187e1-a635-4a43-be2c-46e292f3a913",
                  "label": "",
                  "value": "https://api-eu1.tatum.io/v3/algorand/node/algod/YOUR_API_KEY/v2/blocks/16775567",
                  "children": [],
                  "chatbotID": "1",
                  "description": "Use this endpoint URL as a http-based url to connect directly to the Algorand node provided by Tatum. You can check al available APIs here - https://developer.algorand.org/docs/rest-apis/algod/v2/.",
                  "useCaseType": "code snippet"
                }
              ],
```

## Tooling

## Automation process 
