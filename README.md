# runner_ip2nslookupptr

This project defines a runner that performs a reverse DNS lookup (PTR record) for a given IP address.

It uses the `nslookup -type=PTR <ip_address>` command to find the domain name associated with the provided IP address.

The `runner.yaml` file defines the following:
- **Runner:** Name, description, and version.
- **Build:** Installs the `dnsutils` package (which includes `nslookup`) using `apt`.
- **Webform:** Defines an input field named `ip_address` to accept the target IP address.
- **Launch:** Specifies the `nslookup -type=PTR ${ip_address}` command to be executed.