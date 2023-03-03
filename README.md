# Android Remote attestation models 

The proof results of all the protocols are avalaible at the end of each protocol file.

To run the procotols:
1. Install tamarin (https://tamarin-prover.github.io/)
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