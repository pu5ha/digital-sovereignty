
| Feature                    |  [[Signal]]  | [[Session]] | [[SimpleX Chat]] | [[Briar]] |
| -------------------------- | :----------: | :---------: | :--------------: | :-------: |
| End-to-end encryption      |      ✅       |      ✅      |        ✅         |     ✅     |
| Forward secrecy            |      ✅       |     ⚠️      |        ✅         |     ✅     |
| Post-compromise security   |      ✅       |      ❌      |        ✅         |     ✅     |
| Metadata protection        |      ⚠️      |      ✅      |        ✅         |     ✅     |
| Open source client         |      ✅       |      ✅      |        ✅         |     ✅     |
| Open source server         |      ✅       |      ✅      |        ✅         |    N/A    |
| Decentralized / Federated  |      ❌       |      ✅      |        ⚠️        |     ✅     |
| Onion routing              |      ❌       |      ✅      |        ❌         |     ✅     |
| No phone number required   |      ❌       |      ✅      |        ✅         |     ✅     |
| Anonymous signup           |      ❌       |      ✅      |        ✅         |     ✅     |
| Permanent user identifiers | Phone number | Session ID  |       None       |   None    |
| Multi-device support       |      ✅       |     ⚠️      |        ⚠️        |     ❌     |
| Offline messaging          |      ❌       |      ❌      |        ❌         |     ✅     |
| Advertisements             |      ❌       |      ❌      |        ❌         |     ❌     |
| Cost                       |     Free     |    Free     |       Free       |   Free    |

---

## Trust model

|Application|Primary trust assumption|
|---|---|
|[[Signal]]|Trust Signal's servers to deliver messages while minimizing stored metadata.|
|[[Session]]|Trust a decentralized network of relay nodes to forward encrypted messages.|
|[[SimpleX Chat]]|Trust the relay operators you choose to forward encrypted messages without learning who is communicating.|
|[[Briar]]|Communicate directly with peers over Tor or local networks without centralized messaging servers.|

---

## Best for...

|Goal|Recommendation|
|---|---|
|Everyday messaging|[[Signal]]|
|Maximum anonymity|[[SimpleX Chat]]|
|Hiding communication metadata|[[Session]] or [[SimpleX Chat]]|
|Censorship resistance|[[Briar]]|
|Working during Internet shutdowns|[[Briar]]|
|Easiest onboarding|[[Signal]]|
|No phone number|[[Session]], [[SimpleX Chat]], or [[Briar]]|
|Largest user base|[[Signal]]|
|Talking with non-technical friends|[[Signal]]|
