Index of pages:
---------------

* [Summary](/README.md)
* [Introduction](/README.md)
* [CMS Versioning (CMSver)](/VERSIONING.md)
* [Why Explicit Versioning](/WHY.md)
* [FAQ](/FAQ.md)
* [ABOUT](/ABOUT.md)
* [Who is using CMS Versioning?](/USERS.md)


# CMS Versioning (CMSver)

Given 1.0.0.0 as the first version for a Production Release:

* RELEASE:
  * Major Code Overhaul that impacts a significant number of end points in the Public Api will increment version to 2.0.0.0.
  * Major UX change that impacts in a significant way the usability will increment version to 2.0.0.0.
* MAJOR:
  * Any Breaking Code Change will increment version to 1.1.0.0.
  * UX change that impacts the usability will increment version to 1.1.0.0.
* MINOR:
  * New Features will increment version to 1.0.1.0.
  * Refracting Code that do not impact Public Api will increment version to 1.0.1.0.
  * Deprecating Code that do not impact Public Api will increment version to 1.0.1.0.
  * Removing Code that do not impact Public Api will increment version to 1.0.1.0.
  * UX change that not impacts the usability will increment version to 1.0.1.0.
* PATCH:
  * Security Fix(es) will increment version to 1.0.0.1.
  * Bug Fix(es) will increment version to 1.0.0.1.
  

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://tools.ietf.org/html/rfc2119).

1. Software using Semantic Versioning MUST declare a public API. This API
could be declared in the code itself or exist strictly in documentation.
However it is done, it should be precise and comprehensive.

1. A normal version number MUST take the form W.X.Y.Z where W, X, Y, and Z are
non-negative integers, and MUST NOT contain leading zeroes. W is the RELEASE version, X is the MAJOR version, Y is the MINOR version, and Z is the PATCH version.
Each element MUST increase numerically. For instance: 1.9.0.0 -> 1.10.0.0 -> 1.10.0.1.

1. Once a versioned package has been released, the contents of that version
MUST NOT be modified. Any modifications MUST be released as a new version.

1. Major version zero (0.x.y.z) is for initial development. Anything may change
at any time. The public API should not be considered stable.

1. Version 1.0.0.0 defines the public API. The way in which the version number
is incremented after this release is dependent on this public API and how it changes.

1. PATCH version Z (w.x.y.Z | w > 0) MUST be incremented if only backwards
compatible bug fixes are introduced. A bug fix is defined as an internal change that fixes incorrect behavior.

1. MINOR version Y (w.x.Y.z | w > 0) MUST be incremented if new, backwards
compatible functionality is introduced. It MAY include PATCH level changes. PATCH version MUST be reset to 0 when  version is incremented.

1. MAJOR version X (w.X.y.z | w > 0) MUST be incremented if new, backwards
incompatible functionality is introduced. It MUST be incremented if any public API functionality is marked as deprecated. It MAY be incremented if substantial new functionality or improvements are introduced within the private code. It MAY include MINOR and PATCH level changes. PATCH and MINOR version MUST be reset to 0 when MAJOR version is incremented.

1. RELEASE version W (W.x.y.z | w > 0) MUST be incremented if any backwards
incompatible changes are introduced to the public API. It MAY include MAJOR, MINOR and PATCH level changes. PATCH, MINOR and MAJOR version MUST be reset to 0 when RELEASE version is incremented.
---
1. A pre-release version MAY be denoted by appending a hyphen and a
series of dot separated identifiers immediately following the patch version. Identifiers MUST comprise only ASCII alphanumerics and hyphen [0-9A-Za-z-]. Identifiers MUST NOT be empty. Numeric identifiers MUST NOT include leading zeroes. Pre-release versions have a lower precedence than the associated normal version. A pre-release version indicates that the version is unstable and might not satisfy the intended compatibility requirements as denoted by its associated normal version.
Examples: 1.0.0-alpha, 1.0.0-alpha.1, 1.0.0-0.3.7,1.0.0-x.7.z.92.

1. Build metadata MAY be denoted by appending a plus sign and a series of dot
separated identifiers immediately following the patch or pre-release version.
Identifiers MUST comprise only ASCII alphanumerics and hyphen [0-9A-Za-z-].
Identifiers MUST NOT be empty. Build metadata SHOULD be ignored when determining version precedence. Thus two versions that differ only in the build metadata,have the same precedence.
Examples: 1.0.0-alpha+001, 1.0.0+20130313144700, 1.0.0-beta+exp.sha.5114f85.

1. Precedence refers to how versions are compared to each other when ordered.
Precedence MUST be calculated by separating the version into RELEASE, MAJOR, MINOR, PATCH and PRE-RELEASE identifiers in that order (Build metadata does not figure into precedence). Precedence is determined by the first difference when comparing each of these identifiers from left to right as follows: RELEASE, MAJOR, MINOR and PATCH versions are always compared numerically. 
Example: 1.0.0.0 < 2.0.0.0 < 2.1.0.0 < 2.1.1.0. 

When RELEASE, MAJOR, MINOR and PATCH, a pre-release version has lower precedence than a normal version. 
Example: 1.0.0.0-alpha < 1.0.0.0. 

Precedence for two pre-release versions with the same RELEASE, MAJOR, MINOR and PATCH version MUST be determined by comparing each dot separated identifier from left to right until a difference is found as follows: identifiers consisting of only digits are compared numerically and identifiers with letters or hyphens are compared lexically in ASCII sort order. Numeric identifiers always have lower precedence than non-numeric identifiers. A larger set of pre-release fields has a higher precedence than a smaller set, if all of the preceding identifiers are equal.
Example: 1.0.0.0-alpha < 1.0.0.0-alpha.1 < 1.0.0.0-alpha.beta < 1.0.0.0-beta < 1.0.0.0-beta.2 < 1.0.0.0-beta.11 < 1.0.0.0-rc.1 < 1.0.0.0.


---



[Start page](./)

