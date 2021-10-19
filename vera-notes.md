## **Container Scanning**

### Scan container

```bash
┌──(roan㉿kali)-[~/Documents/veracode/nodegoat]
└─$ srcclr --profile="roan-kali-testing" scan --container nodegoat-web-1                                                                            130 ⨯
WARNING: Veracode SCA agent has not validated support of kali version 2021.3
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Veracode SCA container scanning engine ready
running container analyzer 'Npm' on container 'nodegoat-web-1' ( with image 'nodegoat_web:latest' )
running container analyzer 'Apk' on container 'nodegoat-web-1' ( with image 'nodegoat_web:latest' )
Scanning completed
Matching evidence...
Evidence matching complete

Summary Report
Scan ID                                        c83a64ff-5c62-4e63-bae4-5e4c5be4d8be
Scan Date & Time                               Oct 19 2021 10:03AM SAST
Account type                                   ENTERPRISE
Scan engine                                    3.7.59 (latest 3.7.59)
Analysis time                                  11 seconds
User                                           roan
Project                                        nodegoat_web:latest
Package Manager(s)                             Container

Open-Source Libraries
Total Libraries                                411
Direct Libraries                               7
Transitive Libraries                           404
Vulnerable Libraries                           2

Security
With Vulnerable Methods                        0
High Risk Vulnerabilities                      3
Medium Risk Vulnerabilities                    2
Low Risk Vulnerabilities                       0

Vulnerabilities - Public Data
CVE-2021-3807                                  High Risk       Regular Expression Denial Of Service (ReDoS)     ansi-regex 3.0.0
CVE-2021-3807                                  High Risk       Regular Expression Denial Of Service (ReDoS)     ansi-regex 4.1.0
CVE-2021-3807                                  High Risk       Regular Expression Denial Of Service (ReDoS)     ansi-regex 2.1.1

Vulnerabilities - Premium Data
NO-CVE                                         Medium Risk     Insecure Cipher                                  request 2.88.0
NO-CVE                                         Medium Risk     Prototype Pollution                              request 2.88.0

Licenses
Unique Library Licenses                        13
Libraries Using GPL                            5
Libraries With High Risk License               5
Libraries With Medium Risk License             0
Libraries With Low Risk License                408
Libraries With Multiple Licenses               7
Libraries With Unassessable License            0
Libraries With Unrecognizable License          6

Issues
Issue ID    Issue Type          Severity    Description                                                    Library Name & Version In Use
92555011    Vulnerability       7.8         CVE-2021-3807: Regular Expression Denial Of Service (ReDoS)    ansi-regex 2.1.1
92555012    Vulnerability       7.8         CVE-2021-3807: Regular Expression Denial Of Service (ReDoS)    ansi-regex 3.0.0
92555013    Vulnerability       7.8         CVE-2021-3807: Regular Expression Denial Of Service (ReDoS)    ansi-regex 4.1.0
92555014    Vulnerability       5.0         NO-CVE: Prototype Pollution                                    request 2.88.0
92555015    Vulnerability       4.3         NO-CVE: Insecure Cipher                                        request 2.88.0
92555016    Outdated Library    3.0         Latest version at scan: 8.1.0                                  npm 6.14.15
92555017    License             9.0         Library has High-Risk License                                  alpine-baselayout:3.11 3.2.0-r3
92555018    License             9.0         Library has High-Risk License                                  apk-tools:3.11 2.10.8-r0
92555019    License             9.0         Library has High-Risk License                                  ssl_client:3.11 1.31.1-r10


Full Report Details                            https://sca.analysiscenter.veracode.com/teams/E77HARd/scans/30391330
```

### Scan image

```bash
──(roan㉿kali)-[~/Documents/veracode/nodegoat]
└─$ srcclr --profile="roan-kali-testing" scan --image fefd78e9381a
WARNING: Veracode SCA agent has not validated support of kali version 2021.3
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Veracode SCA container scanning engine ready
running container analyzer 'Apt' on container 'e884c23cd02c82e27a9fa6ac3de6b4dadb7fc02d441a109539f6a8a28f08af3e' ( with image 'mongo:latest' )
Scanning completed
Matching evidence...
Evidence matching complete

Summary Report
Scan ID                                        7a64d75e-e192-40ff-b0b6-d2582d647ff2
Scan Date & Time                               Oct 19 2021 10:09AM SAST
Account type                                   ENTERPRISE
Scan engine                                    3.7.59 (latest 3.7.59)
Analysis time                                  15 seconds
User                                           roan
Project                                        mongo:latest
Package Manager(s)                             Container

Open-Source Libraries
Total Libraries                                89
Direct Libraries                               89
Transitive Libraries                           0
Vulnerable Libraries                           0

Security
With Vulnerable Methods                        0
High Risk Vulnerabilities                      0
Medium Risk Vulnerabilities                    0
Low Risk Vulnerabilities                       0

Licenses
Unique Library Licenses                        15
Libraries Using GPL                            50
Libraries With High Risk License               86
Libraries With Medium Risk License             1
Libraries With Low Risk License                71
Libraries With Multiple Licenses               34
Libraries With Unassessable License            0
Libraries With Unrecognizable License          43

Issues
Issue ID    Issue Type          Severity    Description                      Library Name & Version In Use
92557024    License             9.0         Library has High-Risk License    base-passwd:focal 3.5.47
92557025    License             9.0         Library has High-Risk License    bzip2:focal 1.0.8-2
92557026    License             9.0         Library has High-Risk License    dpkg:focal 1.19.7ubuntu3
92557027    License             9.0         Library has High-Risk License    fdisk:focal 2.34-0.1ubuntu9.1
92557028    License             9.0         Library has High-Risk License    fdisk:focal 2.34-0.1ubuntu9.1
92557029    License             9.0         Library has High-Risk License    fdisk:focal 2.34-0.1ubuntu9.1
92557030    License             9.0         Library has High-Risk License    fdisk:focal 2.34-0.1ubuntu9.1
92557031    License             9.0         Library has High-Risk License    grep:focal 3.4-1
92557032    License             9.0         Library has High-Risk License    init-system-helpers:focal 1.57
92557033    License             9.0         Library has High-Risk License    libacl1:focal 2.2.53-6
92557034    License             9.0         Library has High-Risk License    libasn1-8-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557735    License             9.0         Library has High-Risk License    libasn1-8-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557736    License             9.0         Library has High-Risk License    libassuan0:focal 2.5.3-7ubuntu2
92557737    License             9.0         Library has High-Risk License    libassuan0:focal 2.5.3-7ubuntu2
92557738    License             9.0         Library has High-Risk License    libassuan0:focal 2.5.3-7ubuntu2
92557739    License             9.0         Library has High-Risk License    libassuan0:focal 2.5.3-7ubuntu2
92557740    License             9.0         Library has High-Risk License    libblkid1:focal 2.34-0.1ubuntu9.1
92557741    License             9.0         Library has High-Risk License    libblkid1:focal 2.34-0.1ubuntu9.1
92557742    License             9.0         Library has High-Risk License    libblkid1:focal 2.34-0.1ubuntu9.1
92557743    License             9.0         Library has High-Risk License    libblkid1:focal 2.34-0.1ubuntu9.1
92557744    License             9.0         Library has High-Risk License    libbz2-1.0:focal 1.0.8-2
92557745    License             9.0         Library has High-Risk License    libfdisk1:focal 2.34-0.1ubuntu9.1
92557746    License             9.0         Library has High-Risk License    libfdisk1:focal 2.34-0.1ubuntu9.1
92557747    License             9.0         Library has High-Risk License    libfdisk1:focal 2.34-0.1ubuntu9.1
92557748    License             9.0         Library has High-Risk License    libfdisk1:focal 2.34-0.1ubuntu9.1
92557749    License             9.0         Library has High-Risk License    libgpg-error0:focal 1.37-1
92557750    License             9.0         Library has High-Risk License    libgpg-error0:focal 1.37-1
92557751    License             9.0         Library has High-Risk License    libgssapi3-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557752    License             9.0         Library has High-Risk License    libgssapi3-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557753    License             9.0         Library has High-Risk License    libhcrypto4-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557754    License             9.0         Library has High-Risk License    libhcrypto4-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557755    License             9.0         Library has High-Risk License    libheimbase1-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557756    License             9.0         Library has High-Risk License    libheimbase1-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557757    License             9.0         Library has High-Risk License    libheimntlm0-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557758    License             9.0         Library has High-Risk License    libheimntlm0-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557759    License             9.0         Library has High-Risk License    libhx509-5-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557760    License             9.0         Library has High-Risk License    libhx509-5-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557761    License             9.0         Library has High-Risk License    libidn2-0:focal 2.2.0-2
92557762    License             9.0         Library has High-Risk License    libidn2-0:focal 2.2.0-2
92557763    License             9.0         Library has High-Risk License    libidn2-0:focal 2.2.0-2
92557764    License             9.0         Library has High-Risk License    libkeyutils1:focal 1.6-6ubuntu1
92557765    License             9.0         Library has High-Risk License    libkrb5-26-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557766    License             9.0         Library has High-Risk License    libkrb5-26-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557767    License             9.0         Library has High-Risk License    liblzma5:focal 5.2.4-1ubuntu1
92557768    License             9.0         Library has High-Risk License    liblzma5:focal 5.2.4-1ubuntu1
92557769    License             9.0         Library has High-Risk License    liblzma5:focal 5.2.4-1ubuntu1
92557770    License             9.0         Library has High-Risk License    libmount1:focal 2.34-0.1ubuntu9.1
92557771    License             9.0         Library has High-Risk License    libmount1:focal 2.34-0.1ubuntu9.1
92557772    License             9.0         Library has High-Risk License    libmount1:focal 2.34-0.1ubuntu9.1
92557773    License             9.0         Library has High-Risk License    libmount1:focal 2.34-0.1ubuntu9.1
92557774    License             9.0         Library has High-Risk License    libnpth0:focal 1.6-1
92557775    License             9.0         Library has High-Risk License    libonig5:focal 6.9.4-1
92557776    License             9.0         Library has High-Risk License    libroken18-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557777    License             9.0         Library has High-Risk License    libroken18-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557778    License             9.0         Library has High-Risk License    libsasl2-2:focal 2.1.27+dfsg-2
92557779    License             9.0         Library has High-Risk License    libsasl2-modules-db:focal 2.1.27+dfsg-2
92557780    License             9.0         Library has High-Risk License    libsmartcols1:focal 2.34-0.1ubuntu9.1
92557781    License             9.0         Library has High-Risk License    libsmartcols1:focal 2.34-0.1ubuntu9.1
92557782    License             9.0         Library has High-Risk License    libsmartcols1:focal 2.34-0.1ubuntu9.1
92557783    License             9.0         Library has High-Risk License    libsmartcols1:focal 2.34-0.1ubuntu9.1
92557784    License             9.0         Library has High-Risk License    libsqlite3-0:focal 3.31.1-4ubuntu0.2
92557785    License             9.0         Library has High-Risk License    libssh-4:focal 0.9.3-2ubuntu2.2
92557786    License             9.0         Library has High-Risk License    libunistring2:focal 0.9.10-2
92557787    License             9.0         Library has High-Risk License    libunistring2:focal 0.9.10-2
92557788    License             9.0         Library has High-Risk License    libunistring2:focal 0.9.10-2
92557789    License             9.0         Library has High-Risk License    libuuid1:focal 2.34-0.1ubuntu9.1
92557790    License             9.0         Library has High-Risk License    libuuid1:focal 2.34-0.1ubuntu9.1
92557791    License             9.0         Library has High-Risk License    libuuid1:focal 2.34-0.1ubuntu9.1
92557792    License             9.0         Library has High-Risk License    libuuid1:focal 2.34-0.1ubuntu9.1
92557793    License             9.0         Library has High-Risk License    libwind0-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557794    License             9.0         Library has High-Risk License    libwind0-heimdal:focal 7.7.0+dfsg-1ubuntu1
92557795    License             9.0         Library has High-Risk License    lsb-base:focal 11.1.0ubuntu2
92557796    License             9.0         Library has High-Risk License    mount:focal 2.34-0.1ubuntu9.1
92557797    License             9.0         Library has High-Risk License    mount:focal 2.34-0.1ubuntu9.1
92557798    License             9.0         Library has High-Risk License    mount:focal 2.34-0.1ubuntu9.1
92557799    License             9.0         Library has High-Risk License    mount:focal 2.34-0.1ubuntu9.1
92557800    License             9.0         Library has High-Risk License    perl-base:focal 5.30.0-9ubuntu0.2
92557801    License             9.0         Library has High-Risk License    perl-base:focal 5.30.0-9ubuntu0.2
92557802    License             9.0         Library has High-Risk License    pinentry-curses:focal 1.1.0-3build1
92557803    License             9.0         Library has High-Risk License    pinentry-curses:focal 1.1.0-3build1
92557804    License             9.0         Library has High-Risk License    sensible-utils:focal 0.0.12+nmu1
92557805    License             9.0         Library has High-Risk License    sysvinit-utils:focal 2.96-2.1ubuntu1
92557806    License             9.0         Library has High-Risk License    util-linux:focal 2.34-0.1ubuntu9.1
92557807    License             9.0         Library has High-Risk License    util-linux:focal 2.34-0.1ubuntu9.1
92557808    License             9.0         Library has High-Risk License    util-linux:focal 2.34-0.1ubuntu9.1
92557809    License             9.0         Library has High-Risk License    util-linux:focal 2.34-0.1ubuntu9.1


Full Report Details                            https://sca.analysiscenter.veracode.com/teams/E77HARd/scans/30391586

```
