﻿# Rest PKI Core changelog

<a name="v1-6-0" />
## 1.6.0 (2021-12-08)

Updates database model: no

### New Features

RPNG-129 Add support for using cloud certificates on signature sessions

### Improvements

RPNG-139 Return more information about the signer's certificate on `SignatureSessionModel`



<a name="v1-5-1" />
## 1.5.1 (2021-11-23)

Updates database model: no

### Bug fixes

RPNG-140 Root password authentication error



<a name="v1-5-0" />
## 1.5.0 (2021-09-30)

Updates database model: **yes**

### New Features

RPNG-132 Add support for CAdES/CMS signatures

RPNG-93 Signature sessions with predefined documents

### Improvements

RPNG-138 Remove validation marks from document previews

RPNG-136 Add valiation marks to PDFs even if using CAdES/CMS signature

RPNG-128 Improve usage of theme assets to allow logos with varying aspect ratios

RPNG-120 Handle invalid/corrupt PDF exception properly

### Bug fixes

RPNG-119 Cached versions of acceptable filename patterns are shown on the management UI

### Client-specific changes

RPNG-130 Flavour ONR



<a name="v1-4-2" />
## 1.4.2 (2021-08-24)

Updates database model: no

### Improvements

RPNG-126 Add background worker count configuration

### Bug fixes

RPNG-125 Segmented upload error



<a name="v1-4-1" />
## 1.4.1 (2021-08-24)

Updates database model: no

### Improvements

RPNG-122 Improve validation notice on documents

RPNG-85 Adjustments to document key input

### Bug fixes

RPNG-124 Errors under high demand

RPNG-123 Retries of signature background processing always fail if a certain amont of time has elapsed



<a name="v1-4-0" />
## 1.4.0 (2021-08-11)

* First publicly available version