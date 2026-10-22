# Open Tracked IPv6

_Server variable template for Google Tag Manager (server container)._

Returns the visitor's address as an IPv6 address. An IPv4 address is written in its IPv6 form (`192.168.1.1` becomes `0000:0000:0000:0000:0000:ffff:c0a8:0101`); an IPv6 address, written in full, shortened or mapped, is returned as it is. Anything that is not an address is returned unchanged. Put the result in `ip_override` of the tags that take an IPv6 address, for example Meta Conversions API and TikTok Events API.

## How to use

1. Add the variable to your server container. The default event data key `ip_override` is where the GA4 client puts the visitor's address.
2. Create an **Augment event** transformation that sets `ip_override` to this variable, limited to the tags that should send IPv6.

## Fields

| Field | Name | What it does |
|---|---|---|
| Event data key holding the visitor's address | `eventDataKey` | Leave as ip_override: the GA4 client puts the visitor's address there. |

## Privacy

- The variable only reads the address already in the event and reshapes it. It does not send it anywhere.

## Permissions

- **Reads event data**: Reads the visitor's address from the event.

## Notes

No account is needed.

## About Open Tracked

[Open Tracked](https://opentracked.io) is a first-party tracking service: a tagging server on your own domain, an analytics pixel and a CRM. Documentation: https://docs.opentracked.io/google-tag-manager

## License

Apache License 2.0, see [LICENSE](LICENSE).
