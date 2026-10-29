# easyssf

**Shared Signals Framework support for Java, .NET, Go and Rust.**

easyssf adds an [OpenID Shared Signals Framework](https://openid.net/specs/openid-sharedsignals-framework-1_0.html) (SSF)
receiver to your application, so that it reacts when your identity provider revokes a session, changes a credential
or signals a risk. The receiver verifies the incoming Security Event Tokens, CAEP events about sessions and
credentials, RISC events about accounts and SCIM Events about changes to your users, rejects the affected access
tokens, ends the affected sessions and hands everything else to your code.

One library, one behaviour, on the JVM, .NET, Go and Rust.

## Repositories

| Repository | |
|---|---|
| [easyssf-java](https://github.com/easyssf/easyssf-java) | Core library, Spring Boot starter and plain Java integration; the Quarkus extension lives at [quarkiverse/quarkus-openid-ssf](https://github.com/quarkiverse/quarkus-openid-ssf) |
| [easyssf-dotnet](https://github.com/easyssf/easyssf-dotnet) | ASP.NET Core integration |
| [easyssf-go](https://github.com/easyssf/easyssf-go) | Go module |
| [easyssf-rust](https://github.com/easyssf/easyssf-rust) | Rust crates |
| [website](https://github.com/easyssf/website) | [easyssf.org](https://easyssf.org): getting started guides, use cases, specifications and the tools page |

Each repository ships example applications for the common use cases, rejecting revoked access tokens, ending the
sessions of a web application and mirroring users from SCIM Events, with a Keycloak setup for the full round trip.

## What it implements

- **OpenID SSF 1.0**: transmitter metadata discovery, stream management and verification
- **OpenID CAEP 1.0** and the **CAEP Interoperability Profile 1.0**: session and credential events, with built-in resource server and OIDC client integrations
- **OpenID RISC Profile 1.0**: account events for handlers of your own
- **RFC 8417** Security Event Tokens, **RFC 8935** push and **RFC 8936** poll delivery, **RFC 9493** subject identifiers, **RFC 9967** SCIM Events

Tested against the OpenID conformance suite.

## Links

- Website and documentation: [easyssf.org](https://easyssf.org)
- Tools: [SET generator, inspector and transmitter metadata checker](https://easyssf.org/tools.html)
- News: [easyssf.org/news.html](https://easyssf.org/news.html)
- Contact: oss@easyssf.org

easyssf is open source under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
