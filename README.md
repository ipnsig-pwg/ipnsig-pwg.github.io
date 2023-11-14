# Bundle Protocol Implementations

This document tries to list the various features of Bundle Protocol(BP) ([RFC5050](https://www.rfc-editor.org/rfc/rfc5050.txt), [RFC9171](https://www.rfc-editor.org/rfc/rfc9171.txt)) implementations, based on the [Delay and Disruptive Tolerant Networking concept](https://www.rfc-editor.org/rfc/rfc4838.txt). Current work on the Bundle Protocol Suite is done in the [IETF DTN working group](https://datatracker.ietf.org/wg/dtn/documents/) and [CCSDS DTN working group](https://cwe.ccsds.org/sis/default.aspx#_SIS-DTN).

This page content is based on reading documentation or information from the developers. When a cell is empty, it means not verified or unknown, maybe not implemented but not confirmed (to be not implemented). There is no guarantee of accuracy. This list is not a comprehensive list of all BP implementations. The criteria to be on this public list is that the software source code is available or a public page listing the features of the software can be referenced. 

If you have modifications/additions to suggest, please send a PR or write an issue at the [source github repo](https://github.com/ipnsig-pwg/ipnsig-pwg.github.io) or [send email](mailto:marc.blanchet@viagenie.ca).

| Feature/Stack | Subfeature | [ION](https://sourceforge.net/projects/ion-dtn/) [ION-Core](https://github.com/nasa-jpl/ion-core) | [IONE](https://sourceforge.net/projects/ione/) | [HDTN](https://github.com/nasa/HDTN/wiki/HDTN-Implementation-Features) | [uD3TN](https://gitlab.com/d3tn/ud3tn) | [DTNME](https://github.com/nasa/DTNME) | [BPLib/CFS](https://github.com/nasa/bplib) | [Unibo](https://gitlab.com/unibo-dtn/) | [IBR](https://github.com/ibrdtn/ibrdtn) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [BPv6](https://www.rfc-editor.org/rfc/rfc5050) | | Y | Y | Y | Y | Y | Y | N | Y |
|  | [TCPCLv3](https://www.rfc-editor.org/rfc/rfc7242) | Y | Y | Y | Y | Y | | N | Y |
|  | [UDPCL](https://www.rfc-editor.org/rfc/rfc7122) | Y | Y | Y | N | Y |  | N | Y |
|  | [LTPv1](https://www.rfc-editor.org/rfc/rfc5326) | Y | Y | Y | N | Y |  | N | N |
|  | [BPSEC](https://www.rfc-editor.org/rfc/rfc6257) | Y | Y | N | N | N |  | N | Y |
|  | Custody BPv6 | Y | Y | Y | N | Y |  | N | |
| [BPv7](https://www.rfc-editor.org/rfc/rfc9171) | | Y | Y | Y | Y | Y | Y | Y | N |
|  | [TCPCLv3](https://www.rfc-editor.org/rfc/rfc7242) | Y | Y | Y | Y | Y |  | Y | N |
|  | [TCPCLv4](https://www.rfc-editor.org/rfc/rfc9174) | Y | Y | Y | [N](https://gitlab.com/d3tn/ud3tn/-/issues/40) | Y |  | N | N |
|  | [UDPCL](https://datatracker.ietf.org/doc/draft-sipos-dtn-udpcl/) | Y | Y | Y | N | Y | | N | N |
|  | [LTPv1](https://www.rfc-editor.org/rfc/rfc5326) | Y | Y | Y | N | Y |  | Y | N |
|  | [BPSEC](https://www.rfc-editor.org/rfc/rfc9172) | Y | Y | Y | N | N |  | N | N | 
| | Custody (with [BIBE](https://datatracker.ietf.org/doc/draft-ietf-dtn-bibect/)) | Y | Y | N |  | Y |  | N | N |
| | [RTP](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwjrn92gvJaCAxXxFFkFHXY5A1QQFnoECAwQAQ&url=https%3A%2F%2Fcwe.ccsds.org%2Fsis%2Fdocs%2FSIS-MIA%2FDraft%2520Documents%2FRTP%2520over%2520DTN%2520for%2520Video%2F766x3r0_JPM_RID_Answer_TEMP.doc&usg=AOvVaw3YVH8gKoTvgPLxiUC7PgPq&opi=89978449) | N | N | Y | N |  |  | N | N |
| [CGR](https://datatracker.ietf.org/doc/html/draft-burleigh-dtnrg-cgr), [SABR](https://public.ccsds.org/Pubs/734x3b1.pdf) | | Y | Y | Y | N | N |  | Y | Y |
| [CCSDS SPP](https://public.ccsds.org/Pubs/133x0b2e1.pdf) | | N | N | N | Y |N |  | N | N |
| [Bundle Streaming Service Protocol](https://public.ccsds.org/Pubs/730x2g1.pdf) | | Y | Y | N | N | N |  | N | N |
| [Asynchronous Message Service](https://public.ccsds.org/Pubs/735x1b1.pdf) | | Y | Y | N | N | N |  | N | N |
| IPv6 (for CLAs) | | N | Y | N | Y | N |  | Y | Y |
| [IPND](https://datatracker.ietf.org/doc/draft-johnson-dtn-ipnd/) | | Y | Y | N | N | N |  | N | Y |
| [CFDP](https://public.ccsds.org/Pubs/727x0b5.pdf) | | Y | Y | N | N | Y |  | N | N |
| Primary Language | | C | C | C++ | C | C++ | C | C++ | C++ |

## Notes
- DTNME: as of 20231102, many claimed features such as BPv7 are not in the master branch but in [v1.2.0_Beta branch](https://github.com/nasa/DTNME/tree/v1.2.0_Beta).
- IBR: from Lars Wolf: "as with some other university projects, it happens that the software gets outdated and is not well maintained any more."

## Additional Implementations
There are additional BP implementations that are not listed here, because either there are unknown to this site maintainer or because their specifications are not public. The latter includes: ESA, JAXA.

## Acknowledgments
Thanks to Scott Burleigh(ION, IONE), Scott Johnson(IONE), Felix Walter(uD3TN), Joshua Deaton(DTNME), HDTN team, Carlo Caini(Unibo), Lorenzo Persampieri(Unibo), Lars Wolf(IBR) for providing information on their implementations.

## Last Version of this page
[See last commit](https://github.com/ipnsig-pwg/ipnsig-pwg.github.io/commits/main)
