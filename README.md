# authservice
An implementation of [Envoy](https://envoyproxy.io) [External Authorization](https://www.envoyproxy.io/docs/envoy/latest/configuration/http/http_filters/ext_authz_filter), focused on delivering authN/Z solutions for [Istio](https://istio.io) and [Kubernetes](https://kubernetes.io).

## Introduction
`authservice` can help developers delegate [OIDC Authorization Code Grant](https://openid.net/specs/openid-connect-core-1_0.html#CodeFlowAuth) flow 
to the Istio mesh so that they do not have to write  auth logic in application codebases with language/framework-specific libraries. 
As a result, identity can be centrally managed on the mesh level, as opposed to on the individual application code level.

## Architecture
TBD

## Example
Please refer to the [bookinfo-example](./config) directory for an example integration. 

## Building an `authservice` image
TBD

## Roadmap
Features not yet implemented:
 - Token renewal via refresh token.
 - Start new flow to fetch new tokens when either the ID token or the access token has expired.
 - Support multiple IDPs for the same app.
 - Support adding ext_authz filter and using the `authservice` on the Istio ingress gateway.

Additional features being considered:
 - A more Istio-integrated experience of deploying/configuring/enabling `authservice` 
 (e.g.: extending Istio Authenticaion Policy to include `authservice` configs).  
 
## Contributing & Contact
We welcome feedback and contributions. Aside from submitting Github issues/PRs, you can reach out at `#oidc-proposal` 
or `#security` channel on [Istio’s Slack](https://istio.slack.com/) workspace 
([here's how to join](https://istio.io/about/community/join/)).
