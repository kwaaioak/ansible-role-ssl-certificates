# Create (self-signed) SSL certificates

## Configuration options

ssl_certificates_path:        The location to store public certificates
ssl_certificates_key_path:    The location to store private certificate keys

ssl_certificates_selfsigned:  A dictionary of self-signed certificates to create
    x509_country:             x509 Country code (e.g. US)
    x509_state:               x509 Full state name (e.g. California)
    x509_locality:            x509 Locality (e.g. Los Angeles)
    x509_org:                 x509 Organization name
    x509_cn:                  x509 Common name (i.e. the domain name)

## Example configuration

Create a self-signed certificate. The certificate files will be stored in:
  Certificate: /etc/ssl/certs/www_example_com.crt
  Private key: /etc/ssl/private/www_example_com.key

```
ssl_certificates_selfsigned:
  www_example_com:
    x509_country: US
    x509_state: California
    x509_locality: Los Angeles
    x509_org: Example org, inc.
    x509_cn: www.example.com
```
