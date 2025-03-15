---
title: "Updates to OAuth 2.0 Client Asseertion Authentication and Assertion Based Authorization Grants"
abbrev: "Client Assertion Auth Redux"
category: std
updates: 7523, 7522, 7521, 9126

docname: draft-campbell-oauth-rfc7523redux-latest
submissiontype: IETF
consensus: true
v: 3
area: Security
workgroup: "Web Authorization Protocol"
keyword: [OAuth, audience, JWT, client authentication]
venue:
  group: "Web Authorization Protocol"
  type: "Working Group"
  mail: "oauth@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/oauth/"
  github: "bc-pi/7523redux"
  latest: "https://bc-pi.github.io/7523redux/draft-campbell-oauth-rfc7523redux.html"

author:
 -
    fullname: Michael B. Jones
    organization: Self-Issued Consulting
    email: michael_b_jones@hotmail.com
    uri: https://self-issued.info/
 -
    fullname: Chuck Mortimore
    organization: Disney
    email: charliemortimore@gmail.com
 -
    fullname: Brian Campbell
    organization: Ping Identity
    email: bcampbell@pingidentity.com

normative:
  RFC7521:
  RFC7522:
  RFC7523:
  RFC9126:
  RFC6749:

informative:
  AUDIENCE-TAKES-SHOW:
    target: https://talks.secworkshop.events/osw2025/talk/R8D9BS/
    title: "Client Assertions Gone Wrong: When the Audience Takes Over the Show"
    author:
      -
        name: Pedram Hosseyni
      -
        name: Tim Würtele
    date: 2024-03
  IANA.MediaTypes:
    target: https://www.iana.org/assignments/media-types/
    title: "Media Types"
    author:
        organization: IANA
  IANA.OAuth.Parameters:
    target: https://www.iana.org/assignments/oauth-parameters/
    title: "OAuth Parameters"
    author:
        organization: IANA
  RFC6838:
  RFC8725:
  RFC7519:
  RFC7515:
  RFC8725:
  RFC8414:
  I-D.ietf-oauth-rfc7523bis:


--- abstract

TODO Abstract


--- middle

# Introduction

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

This specification tightens assertion audience handling directives as a mitigation for
potential attacks arising from the exploitation of ambiguities in authorization server
identification allowed by {{RFC7523}}, {{RFC7522}}, {{RFC7521}}, and compounded by {{RFC9126}}.


# IANA Considerations

## OAuth URI Registry Updates

IANA is requested to update the "OAuth URI" registry {{IANA.OAuth.Parameters}} for the following entriest to add \[\[this specfication]]
as an addtional refernce:

* `urn:ietf:params:oauth:grant-type:jwt-bearer`
* `urn:ietf:params:oauth:client-assertion-type:jwt-bearer`
* `urn:ietf:params:oauth:grant-type:saml2-bearer`
* `urn:ietf:params:oauth:client-assertion-type:saml2-bearer`

## Media Type Registration

Registration is requested for the following media type in the IANA
"Media Types" registry {{IANA.MediaTypes}} in the manner described in {{RFC6838}}.

TODO

--- back

# Document History
{:unnumbered}

> \[\[ to be removed by the RFC Editor before publication as an RFC ]]

draft-campbell-oauth-rfc7523redux-00:

* Initial draft proposing a simipler and less distrupitve alternative to {{I-D.ietf-oauth-rfc7523bis}}

# Acknowledgments
{:unnumbered}

The authors would like to acknowledge the following people for their contributions to this document:
John Bradley,
Ralph Bragg,
Joseph Heenan,
Pedram Hosseyni,
Aaron Parecki,
Filip Skokan,
and Tim Würtele.
