# rules-owasp-asvs
Semgrep rules corresponding to the OWASP ASVS standard

### Structure of the Semgrep rule
```
rules:
- id: asvs-java-v6-crypto-insecure-algorithm
  severity: WARNING
  languages:
  - java
  metadata:
    asvs:
      section: "V6 Stored Cryptography Verification Requirements"
      control_id: "6.2.5 Insecure Algorithm"
      control_url: "https://github.com/OWASP/ASVS/blob/master/4.0/en/0x14-V6-Cryptography.md#v62-algorithms"
      version: "4"
    references:
    - ...useful links to learn more...
  message: |
     specifically why rule was triggered and suggested fix
  patterns:
    ...
```
### Structure of the rule directories
```
python/
  flask/
    v5_validation_sanitization_encoding/
    v6_cryptography/
  django/
    v5_validation_sanitization_encoding/
    v6_cryptography/

java/
  spring/
    v5_validation_sanitization_encoding/
    v6_cryptography/
```
### Structure of the rule name
```language/vN_description/6.2.5/short_description_{a|b}.yml```
