# Task 5: Capture and Analyze Network Traffic Using Wireshark on Kali Linux

## Objective
Capture live network packets and identify protocols and traffic types using Wireshark on Kali Linux.

## Tools Used
- **Kali Linux**
- **Wireshark**
- Commands: `ping youtube.com`, Firefox browser (visited youtube.com)

## Steps Followed
1. Started Wireshark and selected the active network interface.
2. Began packet capture.
3. Browsed to **youtube.com** to generate HTTPS, QUIC, OCSP, and TCP traffic.
4. Ran `ping youtube.com` to generate ICMP traffic.
5. Stopped capture after ~1 minute.
6. Applied filters (`dns`, `icmp`, `ocsp`, `quic`, `tcp`, `tls`) to view each protocol separately.
7. Saved capture as `capture.pcap`.
8. Documented findings in `protocol_report.md`.

## Files Included
- `capture.pcap` — Raw packet capture file.
- `protocol_report.md` — Protocol analysis.

## Protocols Observed
- **DNS** — Domain resolution
- **ICMP** — Ping echo requests/replies
- **OCSP** — Certificate status checking
- **QUIC** — Encrypted transport used by YouTube
- **TCP** — General transport for connections
- **TLS** — Encrypted HTTPS sessions

## Conclusion
This task demonstrated how to use Wireshark on Kali Linux to capture and analyze live network traffic by visiting **youtube.com** and performing a ping test. We saw protocols like DNS, ICMP, OCSP, QUIC, TCP, and TLS, learned their roles in browsing and streaming, and noted how encryption protects data. It also showed that some data, like DNS queries, can still be unencrypted, highlighting the need for secure DNS settings.
