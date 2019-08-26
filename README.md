A BWA fork for automatically expanding *BioSeqZip* collapsed sequences
=======================================================================
This repository contains a fork of the [BWA](https://github.com/lh3/bwa) mapper (v0.7.17). It works exactly as the original BWA tool, but it was hacked for automatically expanding SAM/BAM records after the mapping phase.

Notice that this works properly **ONLY** if the input file was previously collapsed with BioSeqZip as long as all read headers are supposed to have the BioSeqZip format (`BIOSEQZIP|ID:<id>|CN:<count>`). Moreover, as long as this is just a demo, proving the effectiveness of including the expansion step in the analysis pipeline, **ONLY** the *mem* BWA algorithm was hacked.

## Prerequisites
This fork has exactly the same prerequisites of the original BWA v0.7.17 tool.

## Install from source
The BioSeqZip-BWA tool can be installed executing the following commands:

```
# Download the repository
git clone https://github.com/lh3/bwa.git bsz_bwa

# Enter the build directory
cd bsz_bwa/build

# Build the tool
make

# Install the binaries
cp bwa /usr/local/bin
```

## Contact
* Gianvito Urgese `gianvito.urgese@polito.it`
* Emanuele Parisi `emanuele.parisi@polito.it`
