Eric presented on 7710-bis-00

Imported to the capport github location

Suggestion made to try this at the next IETF where the captive will always be false but this would help check how many user agents can

Tommy commented this would be worth considering

Lorenzo commented on figuring out the logistics - who&#39;s gong to issue the TLS cert etc

Tommy presenting capport-api

- Cleaned up and tightened the definition for the various keys
- Have an IANA registry
- Changed &quot;vendor-info-url&quot; to &quot;venue-info-url&quot;
- Open issue - should JSON key registration include a prefix (no X-\* )
- Lorenzo - If there&#39;s a way to include session id in venue-info-url  so that devices (e.g. android) can allow users to go back at a later stage
- Next steps - need to do an interop with portal vendors



WBA Presentation (Brian Shields)

- Brian providing WBA overview (see slides from WBA)
- Ovewrview of WBA working groups (specifically captive portal)
- WBA captive portal workgroup charter
- Explaining current captive portal workflow, demonstrates that its fragmented
- Pressing issues - client connectivity check
  - Non standard uri, TLS cert mismatch
- Fragmented use cases between ios and android devices
- No support for client side state machine
- How can WBA collaborate with ietf-capport wg
  - Interested in 7710-bis
  - Support HS2.0 / 802.11u use cases
- Lorenzo comment - implementing 7710-bis and will be sending an upstream patch
  - Long term the capport-api would be a better way to streamline experience
  - If someone is ready to write some tests, we would be happy to test
- Dan Harkins
  - Asked if OWE is included in the considerations
- Tommy
  - Would be good to an experiment for the next ietf and possibly at the hackathon
- Darshak:
  - Maxima willing to implement 7710-bis (Ilya Volynkin related on Jabber)

Chairs going thru issues on capport-architecture ([https://github.com/capport-wg/architecture/issues](https://github.com/capport-wg/architecture/issues))

- Issue #25 -
  - Michael Richardson - Would like some statement around use of DNSSEC,
  - Eric - Its possible DOT and DNSSEC may be blocked
  - Lorenzo - Requiring the capport dns name to be globally reachable may have implementation issues.
  - Discussion on including recommendation for DNS resolution
  - Tommy - When using capport infrastrucutre, must use local DNS infrastructure and should be separate from what applications use latere (e.g. DOH)
  - Cullen - ?
- Issue #24 - Its possible captive portal may lie about captivity
  - Provide guidance and statement that UE
  - Michael Richardson - when is it considered nuisance, its only an issue when the nw enforcement function has no captivity but the api says captive = true
  - Reviewed section 7.4 of capport-arch
  - Jean Chalard - Operator reporting that captivee = false but wanting to show venue-info-url but if UE doesn&#39;t show anything then it would encourage operators to indicate captive=true.
- Issue #15
  - What happens if the portal URI changes
  - Includes the venue-info-uri
  - Darshak - maybe provide a senteence to explain that the possibility exists
  - Tommy - within the api, there is the expiry time which would trigger UE to fetch updated info
  - Lorenzo - Maybe state that the uri should not change during a UE&#39;s session lifetime

Malcom Hubert, Tommy, Loreenzo, Jean Chalard, Darshak to review 7710-bis
