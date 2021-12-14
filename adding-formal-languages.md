---
title: Adding formal languages
description: 
published: true
date: 2021-12-14T08:15:10.174Z
tags: 
editor: markdown
dateCreated: 2021-12-11T22:42:14.471Z
---

> This page is still being worked on and needs the formal language section from the Guidelines for I-D Authors to be incorporated
{.is-danger}


> Make sure that any use of formal languages conforms with the [IESG statement on the use of formal languages](https://www.ietf.org/about/groups/iesg/statements/formal-languages-use/).
{.is-success}

There are a number of formal languages used in I-Ds and several tools have been written to help process them. 

## 1. rfcstrip
[rfcstrip](https://github.com/mbj4668/rfcstrip) extracts code components, YANG modules and SMIv2 modules from RFCs and I-Ds, and extracts and unfolds artwork from RFCs and I-Ds in XML format.

## 2. Extract and validate ABNF with bap
[bap](https://github.com/ietf-tools/bap) can extract and validate ABNF.  The extraction feature is available as a separate [web service](https://tools.ietf.org/abnf/) and the validation as a separate [web form](https://tools.ietf.org/tools/bap/abnf.cgi).

If ABNF is used, your I-D should contain a normative reference to RFC 5234, the specification for ABNF.

## 3. Extract and validate YANG with YANG Catalog
[YANG Catalog](https://www.yangvalidator.com/) is a website operated and maintained by the IETF that provides a central resource for the use of YANG, including the [YANG Validator](https://www.yangvalidator.com/yangvalidator).

## 4. Validate and convert YANG with pyang
[pyang](https://github.com/mbj4668/pyang) validates YANG modules and converts them into other formal languages.

## 5. Validate MIBs with smilint
smilint is a command line tool that is part of the [libsmi](https://www.ibr.cs.tu-bs.de/projects/libsmi/download.html?lang=de) suite of tools and is available as a [package](https://command-not-found.com/smilint) for most operating systems.

All MIB modules should have correct syntax, so they should compile cleanly using smilint, e.g.:
```bash
smilint -m -s -l 6 -i namelength-32
```
An [online service](https://www.ibr.cs.tu-bs.de/projects/libsmi/tools/) is available for MIB syntax checking. This allows you to extract the MIB module from a document for your own local use, but you can also directly run a syntax check.

Please evaluate all diagnostic messages and if in doubt, feel free to check on the [ietfmibs mailing list](https://www.ietf.org/mailman/listinfo/IETFMIBS) or with the OPS ADs.

> You should also ensure that you follow the Guidelines for Authors and Reviewers of MIB documents (RFC 4181)
{.is-success}