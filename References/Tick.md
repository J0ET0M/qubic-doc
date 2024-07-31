# Qubic and the Tick
A tick in Qubic is one vote from one Computor for a given Tick.

The Tick mainly consists of:
- [ComputorIndex](Computorindex.md)
- [Epoch](Epoch.md)
- tick number
- timestamp

And also the following cryptographic fields:

```c++
unsigned long long prevResourceTestingDigest;
unsigned long long saltedResourceTestingDigest;

m256i prevSpectrumDigest;
m256i prevUniverseDigest;
m256i prevComputerDigest;
m256i saltedSpectrumDigest;
m256i saltedUniverseDigest;
m256i saltedComputerDigest;

m256i transactionDigest;
m256i expectedNextTickTransactionDigest;

unsigned char signature[SIGNATURE_SIZE];
``` 


## prevResourceTestingDigest
the link to the previous resource testing digest. the resource testing digest is a hash of the sequentially processed ai training solutions.

## saltedResourceTestingDigest

## prevSpectrumDigest

## prevUniverseDigest

## saltedSpectrumDigest

## saltedUniverseDigest

## saltedComputerDigest

## transactionDigest

## expectedNextTickTransactionDigest

## signature