# Create (self-signed) SSL certificates

## Configuration options

```
ssl_certificates_path:        # The location to store public certificates (default: /etc/ssl/certs)
ssl_certificates_key_path:    # The location to store private certificate keys (default: /etc/ssl/private)

ssl_certificates_selfsigned:  # A dictionary of self-signed certificates to create
  [filename]:                 # Basename used to create the .crt and .key
    x509_country:             # x509 Country code (e.g. US)
    x509_state:               # x509 Full state name (e.g. California)
    x509_locality:            # x509 Locality (e.g. Los Angeles)
    x509_org:                 # x509 Organization name (e.g. Example, Inc.)
    x509_cn:                  # x509 Common name/domain name (e.g. www.example.com)
```

## Example configuration

Create a self-signed certificate...

```
ssl_certificates_selfsigned:
  www_example_com:
    x509_country: US
    x509_state: California
    x509_locality: Los Angeles
    x509_org: Example org, inc.
    x509_cn: www.example.com
```
