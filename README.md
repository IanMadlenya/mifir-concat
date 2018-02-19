## mifir-concat
Library to derive MiFIR CONCAT

This implements a CONCAT derivation algorithm based on EC 2017/590 article 6 of MiFIR, and ESMA's Guidelines for transaction reporting.
Features:
* High speed; Expect >100.000 CONCATs a second on single thread i5 cpu
* Full unicode mapping
* Removal of prefix and titles
* Verified with the tests in the guidelines

## Building and testing
Tested with Go version 1.10
```
  git clone https://github.com/robfordww/mifir-concat.git
  go build
  go test
```

## Usage
  ./mifirconcat < persons_example.txt

or use it by invoking the process and pipe to stdin strings on the following form
```
AT|18870812|Erwin|Schrödinger
```
the process then returns
```
AT18870812ERWINSCHRO
```
