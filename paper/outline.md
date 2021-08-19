## Proof of sourcecode confidentiality for Android applications using hardware backed security.

* Chapter 1: Introduction
    * Address the problem of code protection
    * Contribution :
        * Analyse software based solutions existing solutions (Dynamic code delivery, approve.it ..etc)
        * Model existing hardware backed attestation
        * Propose model for code protection that ensure: (App integrity, Device integrity, Protected Code integrity, Persistent of device integrity).
    * Paper outline
* Chapter 2: Background and Related work
    * Android infrastructure
        * Bootloader
        * Android OS (System apps vs normal apps)
        * TEE  (Keystore and Keymaster)
        * Remote attestation
    * Related work
        * Existing code protections methods 
            * (Address why the solutions are no loner usable): software based only
        * Known issues with remote attestation 
            * (Address bypassing safetynet software measurements)  
            * The rest of attestation methods receive less research attention.
* Chapter 3: Analysis of existing solutions
    * Dynamic code devilry (Google)
    * Approve.it ??
    * What we need to code protections (key management, hardware root of trust ..etc)
* Chapter 4: Modeling existing remote attestation
    * We chose modeling over source code review because the source code are not available publicly for some services.
    * Threat model: We consider an adversary able to:
        * (Rooting) Tamper the device (via unlocking the bootloader.
        * (Repak) Able to repack an application, change software based measurements.
        * (Netowrk adevsery)
        * (Memory corruptions vulnerabilities): out of the scope because they are difficult to detect).
    * Modeling
    * Discuss protocols modeling
    * Discuss founded issues:
        * Key attestation lack of freshness. It can be achievable using key attestation challenge with remote server. Current timestamp come from understated source software based. (Currentes)
        * Knox v2 vulnerable to relay attack.
        * Persistent of integrity is not ensured  in Knox v3, Knox v2, and Safetynet without using the keystore. In safety (key attestation version), the developer cannot ensure the existing of attested key which results in the same issue.
        * It is debatable if unlocking the bootloader will  wipe all data partition, according to Google it is. But different vendors use different bootloader implementation. We propose a unified solution in android SDK to ensure this feature by patching Keystore and Keymaster as follow: (delete keys per n where n is number of boot), delete keys when boot state changed. The proposed changes are theoretically achievable and do not require major changes based on our review for the sourcecode reference of Keystore and Keymaster.  Changes are addressed in the Appendix section.
        * is Code protection needed ?
* Chapter 5: (Evaluation) Code protection using remote attestation 
    * Which remote attestation ensure all the four proprieties. We propose the model based on it. We prove the model work in compromise network as well.
* Chapter 6: Discussion and results
* Chapter 7: Conclusion and future work

