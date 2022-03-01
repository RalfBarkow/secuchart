# Signal

## Access to contact list

* https://signal.org/blog/private-contact-discovery/

> Technology preview: Private contact discovery for Signal

It details two alternatives:

* a brute forceable truncated hash of the phone numbers and
* an SGX security enclave that places trust on the server hardware equipped with all kinds of backdoors.

* https://signal.org/blog/contact-discovery/

> The Difficulty Of Private Contact Discovery

From that overview of possible implementation alternatives, but somehow discounted encrypted bloom filters citing concerns about bandwidth costs.

However, that would have actually worked perfectly if they updated the set on demand when checking for a new contact number and/or if the database was synced P2P via WebRTC to reduce their bandwidth costs.
And also, as I think 99% of the users only have domestic contacts, sharding by region might actually work.
As such contact discovery can be pretty hard on the server side, federated servers would be great to have here as well.

Note that secure, zero-knowledge contact discovery can be an issue for any alternative system even if it used some other identifier, like an email address (or matrix ID, Friendica profile URL, etc.

Stepping back from a theoretically sound solution to one where you must trust a vendor that also happens to have a sketchy safety record is dubious at best.