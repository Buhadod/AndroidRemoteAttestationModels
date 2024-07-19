# Symbolic modelling of remote attestation protocols for device and app integrity on Android

These protocols part of the paper : Symbolic modelling of remote attestation protocols for device and app integrity on Android

Aldoseri, A., Chothia, T., Moreira-Sanchez, J., & Oswald, D. (2023). Symbolic verification for device and application integrity remote attestation protocols on Android. In Proceedings of AsiaCCS 2023.

## To cite the paper
```
@incollection{aldoseri2023symbolic,
  title={Symbolic verification for device and application integrity remote attestation protocols on Android},
  author={Aldoseri, Abdulla and Chothia, Tom and Moreira-Sanchez, Jose and Oswald, David},
  booktitle={Proceedings of AsiaCCS 2023},
  year={2023}
}
```

## Paper at Google scholar:
https://scholar.google.com/citations?view_op=view_citation&hl=en&user=sDQEs7wAAAAJ&citation_for_view=sDQEs7wAAAAJ:ufrVoPGSRksC

## About the protocols
The proof results of all the protocols are avalaible at the end of each protocol file.

To run the procotols:
1. Install tamarin (https://tamarin-prover.github.io/) (version 1.6)
2. open the directory and run the following command

```
tamarin-prover interactive . --interface=*4 -p=8200
```

This will open the protocols in the interactive mode on the browser. You should access them via http://localhost:8200 if port 8200 is used. 
You can use the command line based as well as follows:

```
tamarin-prover <filename> --prove=<lemma name>
```

tamarin-prover KnoxV2.sapic --prove=DeviceIntegrity
tamarin-prover KnoxV3.sapic --prove=DeviceAndAppIntegrity
tamarin-prover SafetyNetHW.sapic --prove=DeviceAndAppIntegrity
