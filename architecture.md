# ArtLedger Data Standard

## Module Actions
### Entity Identity
### Object Identity
### Certificate of Authenticity
#### Create
#### Provide
#### Transfer
<!-- Artist,contract NFT each separate
 NFT is the pointer, construct proof of authenticity
no ownership per Hunter
-->
#### Claim
#### Renew
#### Revoke


#### Recoverability
#### Attest
<!-- Append to the provenenance DAG, where exhibited, loaned-->
### Ship
### Transfer Ownership
<!-- DAG of ownership so artist and gallery gets percentage of secondary sales 
-->
<!-- Fractional Ownership -->
### Underwrite
### Valuation

## Roles
### Creator
### Appraiser
### Insurer
### Shipper
### Curator
### Collector
#### Owner (current)
#### Purchaser (future)
### Regulator
#### National
#### Regional
## Data Types

| Data Type | Description | Limits | Universality |
|----|----|----|----|
| boolean | Logical binary choice| Yes/No, True/False, 0/1| Yes |
| timestamp | Date-Time Value| ISO 8601 Format | High |
| uint |  32-bit unsigned integer| [0,4294967295] | High |
| string |  8-bit character sequence| each bit limited to [0,255], 8-bits for higher universality | High |
<!-- alice only has byte slices -->
## Data Structures
### Identity
<!-- hash string -->

### String Wrapper

## Fields
### Certificate of Authenticity
| Variable Name| Descriptive Name | Data Type or Structure| Future |
|----|----|----|----|
|printer|Printer|Identity||
|address|Address of record for COA| String Wrapper||
|phone|Phone of record for COA|unit||
|artist|Artist creator of work|Identity||
|title|Title of work|string||
|collaborationPeriod|Period of collaboration|[timestamp,timestamp]||
|standarddate| Standard Date|timestamp||
|cancellationdate| Cancellation Date|timestamp||
|signeddate| Date Signed|timestamp||
|medium| Medium|string|selection from media types|
|size| Size in H-W-Edge format|(uint, uint, uint)||
|signaturelocation| Signature Location |string|format TBD|
|processingandproofing| Processing and proofing |string|format TBD|
|editionprinting| Edition printing |string|format TBD|
|Collaboration and supervision|Collaboration and supervision|Identity|Collection of identity per collaborator|

#### Proof Types
Edition
Artist’s Proofs
Trial Proofs
Color Trial Proofs
Right to Print Proof
Printer’s Proof
Cancellation Proof
Other Proofs
Attestation: Date Artist Date Printer