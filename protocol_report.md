# Protocol Report — Wireshark Capture (Kali Linux)

## Capture Summary
- File: `capture.pcap`
- Duration: 1 minute
- Activities: Visited youtube.com, pinged youtube.com

## Protocols Identified
1. **DNS**
   - Lookups for `youtube.com` and related Google domains.
   - A and AAAA record queries.

2. **ICMP**
   - Echo Requests and Echo Replies from `ping youtube.com`.
   - Used for connectivity and latency testing.

3. **OCSP**
   - Online Certificate Status Protocol exchanges for validating TLS certificates.

4. **QUIC**
   - UDP-based encrypted transport used by YouTube for streaming and fast page loads.

5. **TCP**
   - Underlying transport for non-QUIC connections.

6. **TLS**
   - Encrypted HTTPS sessions to YouTube servers and other Google services.

## Observations
- QUIC is heavily used by YouTube for streaming over UDP.
- TLS connections protect web traffic from interception.
- OCSP ensures certificates are valid and not revoked.
- DNS queries are in plaintext, visible in the capture.
- ICMP packets confirm network connectivity to YouTube.

## Recommendations
- Consider DNS over HTTPS (DoH) to encrypt DNS queries.
- QUIC and TLS already provide strong encryption for YouTube traffic.
- OCSP checks are good security practice but reveal sites visited to the OCSP responder.
