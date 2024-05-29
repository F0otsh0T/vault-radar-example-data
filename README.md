---
title: HashiCorp Vault Radar Example Data
description: Example Data for Vault Radar
---
# HashiCorp Vault Radar Example Data
#### OVERVIEW
Sample or dummy "secure" data for HashiCorp Vault Radar

---

#### OPENSSL
###### CA Certificate
1. Private Key
```shell
$ openssl genrsa -out 01-01.privatecakey.pem 4096
```
2. Generate CA Certificate with Private Key
```shell
$ openssl req -new -x509 -sha256 -days 3650 -key 01-01.privatecakey.pem -out 01-02.cacert.pem
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:US
State or Province Name (full name) [Some-State]:NJ
Locality Name (eg, city) []:New Jersey
Organization Name (eg, company) [Internet Widgits Pty Ltd]:Yoyodyne Propulsion Systems
Organizational Unit Name (eg, section) []:Red Lectroids   
Common Name (e.g. server FQDN or YOUR name) []:redlectroids.com
Email Address []:john.bigboote@redlectroids.com
```
3. Examine Certificate
```shell
openssl x509 -in 01-02.cacert.pem -text
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            7a:d0:bb:8e:ae:2f:b6:fb:6c:3d:27:23:2f:b3:e7:ca:b5:44:3f:71
        Signature Algorithm: sha256WithRSAEncryption
        Issuer: C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Red Lectroids, CN=redlectroids.com, emailAddress=john.bigboote@redlectroids.com
        Validity
            Not Before: May 29 21:17:42 2024 GMT
            Not After : May 27 21:17:42 2034 GMT
        Subject: C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Red Lectroids, CN=redlectroids.com, emailAddress=john.bigboote@redlectroids.com
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (4096 bit)
                Modulus:
                    00:b6:1f:2a:ec:51:dd:20:a2:d8:09:d8:df:8c:37:
                    71:11:e6:c7:1a:15:f5:b5:50:85:21:a8:42:89:e2:
                    70:12:fe:3c:25:30:2e:7c:b4:a8:82:31:f5:ee:93:
                    3d:00:d1:1d:c4:37:96:c9:66:4b:7f:04:32:4c:4d:
                    8a:96:5c:6a:cd:e7:57:62:71:9f:8d:d7:07:e2:01:
                    48:b6:c1:97:d0:47:1d:64:99:61:ec:40:c8:60:12:
                    fd:b6:14:30:58:17:b6:89:49:b0:38:d2:26:ca:7f:
                    9d:b9:4e:9f:9e:4b:fb:42:92:06:9b:ec:73:3b:a2:
                    ba:02:f8:f1:99:05:64:14:00:4f:e4:6f:2e:d4:3a:
                    e2:87:f2:c6:a6:71:0b:8f:ff:c0:c4:5b:27:ad:c2:
                    18:c4:a3:56:e3:2e:06:d0:2e:11:c1:58:e2:30:4a:
                    cb:95:68:a4:84:19:e4:08:97:3e:50:e0:4c:98:92:
                    47:22:b0:f6:4e:5f:ad:04:34:46:63:28:48:ba:cb:
                    9a:e2:cb:ad:a6:61:77:c0:34:0f:df:d0:60:8d:4d:
                    97:4e:97:5b:5b:58:4a:82:06:de:c0:c1:65:f3:d2:
                    a8:20:b6:02:f3:2e:27:e1:c5:f2:ed:15:f4:bf:67:
                    e3:bd:3e:fa:dc:3d:78:35:54:d3:e4:26:12:0a:14:
                    1e:49:b1:3b:51:fc:d0:7f:df:3f:15:3c:19:67:3d:
                    02:ba:f0:9e:48:18:15:14:a5:09:ac:86:b6:48:09:
                    cf:9a:b9:ec:ad:6f:5e:4d:d9:b7:5c:d9:ff:50:6c:
                    f5:c3:f1:b1:a9:f1:d7:9e:cb:06:81:1a:fb:c5:fb:
                    f1:25:67:73:61:80:20:89:de:7b:5e:ed:8c:63:80:
                    c5:f2:a8:ee:83:9f:6b:e0:0a:85:24:fe:44:98:64:
                    84:97:53:25:0c:74:a4:0f:d4:12:0c:09:b0:c2:e7:
                    91:e5:78:9c:a2:32:cc:7c:f9:a0:88:0f:bf:3f:7d:
                    3e:d6:a6:5a:2b:7c:e9:17:50:fb:7b:33:b1:15:99:
                    25:23:74:1c:6c:56:67:f6:69:a5:0c:67:56:5f:55:
                    f8:9c:e9:85:78:56:d2:39:30:5b:df:92:87:49:3e:
                    05:5f:b9:d7:80:33:c9:4a:ff:03:35:74:56:b1:be:
                    b8:b1:97:72:9b:bf:d9:ce:5c:67:db:92:aa:da:18:
                    b9:7e:88:e6:20:bf:d9:7d:a2:b3:0b:8b:bb:ea:88:
                    a7:6f:0b:c2:d5:21:5a:90:6f:fa:e5:95:c4:14:c4:
                    7d:55:25:e0:99:90:cc:7a:8b:99:a6:35:dd:06:a3:
                    d5:52:b0:88:41:1d:86:19:8f:f3:54:4e:e1:25:45:
                    e8:61:85
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Subject Key Identifier: 
                60:CA:94:26:43:D5:D6:14:38:BF:D3:FD:D8:A9:10:DB:BA:20:CB:96
            X509v3 Authority Key Identifier: 
                60:CA:94:26:43:D5:D6:14:38:BF:D3:FD:D8:A9:10:DB:BA:20:CB:96
            X509v3 Basic Constraints: critical
                CA:TRUE
    Signature Algorithm: sha256WithRSAEncryption
    Signature Value:
        8b:0b:85:cd:83:80:e6:43:77:15:a5:72:70:8c:0c:e0:36:58:
        79:c1:cf:24:81:de:45:32:bf:f2:8d:ff:58:67:a0:b0:db:fb:
        08:2f:c2:11:93:68:90:97:f3:6a:3c:9d:4e:a2:23:bd:bb:ac:
        6a:c4:5a:c7:30:a3:9a:f7:94:09:ee:a0:bd:41:0e:47:7f:d5:
        3c:31:4f:9a:85:a1:77:40:fe:5c:ec:51:fb:17:d2:ca:db:98:
        96:94:91:dc:70:7e:7f:14:11:2e:9c:15:fb:4f:be:54:9b:3f:
        a1:6f:98:33:f0:74:8b:db:6d:40:05:e7:a0:84:3e:cc:d6:05:
        54:0f:f2:87:d2:f3:a4:9d:dd:23:24:93:e0:74:1d:34:89:84:
        ad:7d:dc:35:f8:4d:26:e5:1c:3f:96:93:af:18:53:47:b6:07:
        09:b9:39:1a:e2:56:00:92:39:64:59:47:4b:cf:43:0a:3d:6c:
        05:52:8d:89:db:ac:7f:f3:23:9c:31:b7:10:fb:9e:73:a1:93:
        c1:29:fd:51:5c:9b:3e:22:eb:66:36:53:a3:d9:75:99:44:d4:
        e3:3b:a3:1c:d3:8f:67:66:5f:6d:c2:b1:06:5d:17:c6:c5:f7:
        62:40:73:c3:d5:96:7f:bf:db:51:f6:9d:12:bc:02:74:33:2e:
        07:0e:37:41:e6:be:ec:18:2e:53:aa:85:aa:5e:e6:b8:ea:92:
        3b:35:b9:c2:dd:a5:11:f7:6f:fb:e6:33:c1:72:a1:4a:6c:c6:
        a0:6b:d0:a7:ca:13:cd:28:90:30:7e:df:d9:25:9f:8f:57:93:
        77:de:c6:14:09:c8:d4:8a:75:b3:20:09:0a:c0:e4:d2:83:01:
        52:21:a5:ba:7b:db:31:9b:0b:e5:d1:aa:8e:49:3f:5b:55:18:
        f1:8f:2f:e5:aa:0c:ce:55:dd:69:06:1e:0b:03:33:80:26:e1:
        3e:23:b8:01:60:58:e9:db:e2:89:7e:44:1c:13:e4:e1:5f:c0:
        11:71:7e:e3:d8:a3:6e:9e:84:f3:55:e7:bd:e8:58:d9:10:d8:
        46:0b:d7:1a:72:88:e3:61:b8:87:a8:58:4c:af:c7:25:c3:c1:
        9a:46:81:98:92:47:d0:9d:38:21:51:20:61:e7:f8:f6:5d:c2:
        9a:86:e3:dd:c2:1f:7e:ff:e5:82:0e:23:b6:10:11:0e:5d:9b:
        3e:1e:9d:9d:6c:f5:d3:e8:5a:68:4d:2e:0e:12:e5:a4:ea:ad:
        c2:d5:ec:3e:aa:28:af:08:ba:40:6a:0e:e2:ff:6d:53:bc:9d:
        4e:ee:d2:fb:c0:ac:64:0c:da:26:b4:65:62:5a:a4:d8:eb:17:
        3e:08:ee:a6:30:c4:de:f0
-----BEGIN CERTIFICATE-----
MIIGUTCCBDmgAwIBAgIUetC7jq4vtvtsPScjL7PnyrVEP3EwDQYJKoZIhvcNAQEL
BQAwgbcxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjETMBEGA1UEBwwKTmV3IEpl
cnNleTEkMCIGA1UECgwbWW95b2R5bmUgUHJvcHVsc2lvbiBTeXN0ZW1zMRYwFAYD
VQQLDA1SZWQgTGVjdHJvaWRzMRkwFwYDVQQDDBByZWRsZWN0cm9pZHMuY29tMS0w
KwYJKoZIhvcNAQkBFh5qb2huLmJpZ2Jvb3RlQHJlZGxlY3Ryb2lkcy5jb20wHhcN
MjQwNTI5MjExNzQyWhcNMzQwNTI3MjExNzQyWjCBtzELMAkGA1UEBhMCVVMxCzAJ
BgNVBAgMAk5KMRMwEQYDVQQHDApOZXcgSmVyc2V5MSQwIgYDVQQKDBtZb3lvZHlu
ZSBQcm9wdWxzaW9uIFN5c3RlbXMxFjAUBgNVBAsMDVJlZCBMZWN0cm9pZHMxGTAX
BgNVBAMMEHJlZGxlY3Ryb2lkcy5jb20xLTArBgkqhkiG9w0BCQEWHmpvaG4uYmln
Ym9vdGVAcmVkbGVjdHJvaWRzLmNvbTCCAiIwDQYJKoZIhvcNAQEBBQADggIPADCC
AgoCggIBALYfKuxR3SCi2AnY34w3cRHmxxoV9bVQhSGoQonicBL+PCUwLny0qIIx
9e6TPQDRHcQ3lslmS38EMkxNipZcas3nV2Jxn43XB+IBSLbBl9BHHWSZYexAyGAS
/bYUMFgXtolJsDjSJsp/nblOn55L+0KSBpvsczuiugL48ZkFZBQAT+RvLtQ64ofy
xqZxC4//wMRbJ63CGMSjVuMuBtAuEcFY4jBKy5VopIQZ5AiXPlDgTJiSRyKw9k5f
rQQ0RmMoSLrLmuLLraZhd8A0D9/QYI1Nl06XW1tYSoIG3sDBZfPSqCC2AvMuJ+HF
8u0V9L9n470++tw9eDVU0+QmEgoUHkmxO1H80H/fPxU8GWc9ArrwnkgYFRSlCayG
tkgJz5q57K1vXk3Zt1zZ/1Bs9cPxsanx157LBoEa+8X78SVnc2GAIInee17tjGOA
xfKo7oOfa+AKhST+RJhkhJdTJQx0pA/UEgwJsMLnkeV4nKIyzHz5oIgPvz99Ptam
Wit86RdQ+3szsRWZJSN0HGxWZ/ZppQxnVl9V+JzphXhW0jkwW9+Sh0k+BV+514Az
yUr/AzV0VrG+uLGXcpu/2c5cZ9uSqtoYuX6I5iC/2X2iswuLu+qIp28LwtUhWpBv
+uWVxBTEfVUl4JmQzHqLmaY13Qaj1VKwiEEdhhmP81RO4SVF6GGFAgMBAAGjUzBR
MB0GA1UdDgQWBBRgypQmQ9XWFDi/0/3YqRDbuiDLljAfBgNVHSMEGDAWgBRgypQm
Q9XWFDi/0/3YqRDbuiDLljAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3DQEBCwUA
A4ICAQCLC4XNg4DmQ3cVpXJwjAzgNlh5wc8kgd5FMr/yjf9YZ6Cw2/sIL8IRk2iQ
l/NqPJ1OoiO9u6xqxFrHMKOa95QJ7qC9QQ5Hf9U8MU+ahaF3QP5c7FH7F9LK25iW
lJHccH5/FBEunBX7T75Umz+hb5gz8HSL221ABeeghD7M1gVUD/KH0vOknd0jJJPg
dB00iYStfdw1+E0m5Rw/lpOvGFNHtgcJuTka4lYAkjlkWUdLz0MKPWwFUo2J26x/
8yOcMbcQ+55zoZPBKf1RXJs+IutmNlOj2XWZRNTjO6Mc049nZl9twrEGXRfGxfdi
QHPD1ZZ/v9tR9p0SvAJ0My4HDjdB5r7sGC5TqoWqXua46pI7NbnC3aUR92/75jPB
cqFKbMaga9CnyhPNKJAwft/ZJZ+PV5N33sYUCcjUinWzIAkKwOTSgwFSIaW6e9sx
mwvl0aqOST9bVRjxjy/lqgzOVd1pBh4LAzOAJuE+I7gBYFjp2+KJfkQcE+ThX8AR
cX7j2KNunoTzVee96FjZENhGC9cacojjYbiHqFhMr8clw8GaRoGYkkfQnTghUSBh
5/j2XcKahuPdwh9+/+WCDiO2EBEOXZs+Hp2dbPXT6FpoTS4OEuWk6q3C1ew+qiiv
CLpAag7i/21TvJ1O7tL7wKxkDNomtGViWqTY6xc+CO6mMMTe8A==
-----END CERTIFICATE-----
```
4. Combine Key and Certificate in a PKCS#12 (P12) bundle
```shell
$ openssl pkcs12 -inkey 01-01.privatecakey.pem -in 01-02.cacert.pem -export -out 01-03.certificate.p12
Enter Export Password:
Verifying - Enter Export Password:
```
5. Validate your P12 file (PEM pass phrase: `password123`)
```shell
$ openssl pkcs12 -in 01-03.certificate.p12 -info
Enter Import Password:
MAC: sha256, Iteration 2048
MAC length: 32, salt length: 8
PKCS7 Encrypted data: PBES2, PBKDF2, AES-256-CBC, Iteration 2048, PRF hmacWithSHA256
Certificate bag
Bag Attributes
    localKeyID: C1 55 71 EF 8F CC 95 43 A9 7F 6D 2F B8 CA A7 2E 8D 4A 83 3D 
subject=C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Red Lectroids, CN=redlectroids.com, emailAddress=john.bigboote@redlectroids.com
issuer=C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Red Lectroids, CN=redlectroids.com, emailAddress=john.bigboote@redlectroids.com
-----BEGIN CERTIFICATE-----
MIIGUTCCBDmgAwIBAgIUetC7jq4vtvtsPScjL7PnyrVEP3EwDQYJKoZIhvcNAQEL
BQAwgbcxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjETMBEGA1UEBwwKTmV3IEpl
cnNleTEkMCIGA1UECgwbWW95b2R5bmUgUHJvcHVsc2lvbiBTeXN0ZW1zMRYwFAYD
VQQLDA1SZWQgTGVjdHJvaWRzMRkwFwYDVQQDDBByZWRsZWN0cm9pZHMuY29tMS0w
KwYJKoZIhvcNAQkBFh5qb2huLmJpZ2Jvb3RlQHJlZGxlY3Ryb2lkcy5jb20wHhcN
MjQwNTI5MjExNzQyWhcNMzQwNTI3MjExNzQyWjCBtzELMAkGA1UEBhMCVVMxCzAJ
BgNVBAgMAk5KMRMwEQYDVQQHDApOZXcgSmVyc2V5MSQwIgYDVQQKDBtZb3lvZHlu
ZSBQcm9wdWxzaW9uIFN5c3RlbXMxFjAUBgNVBAsMDVJlZCBMZWN0cm9pZHMxGTAX
BgNVBAMMEHJlZGxlY3Ryb2lkcy5jb20xLTArBgkqhkiG9w0BCQEWHmpvaG4uYmln
Ym9vdGVAcmVkbGVjdHJvaWRzLmNvbTCCAiIwDQYJKoZIhvcNAQEBBQADggIPADCC
AgoCggIBALYfKuxR3SCi2AnY34w3cRHmxxoV9bVQhSGoQonicBL+PCUwLny0qIIx
9e6TPQDRHcQ3lslmS38EMkxNipZcas3nV2Jxn43XB+IBSLbBl9BHHWSZYexAyGAS
/bYUMFgXtolJsDjSJsp/nblOn55L+0KSBpvsczuiugL48ZkFZBQAT+RvLtQ64ofy
xqZxC4//wMRbJ63CGMSjVuMuBtAuEcFY4jBKy5VopIQZ5AiXPlDgTJiSRyKw9k5f
rQQ0RmMoSLrLmuLLraZhd8A0D9/QYI1Nl06XW1tYSoIG3sDBZfPSqCC2AvMuJ+HF
8u0V9L9n470++tw9eDVU0+QmEgoUHkmxO1H80H/fPxU8GWc9ArrwnkgYFRSlCayG
tkgJz5q57K1vXk3Zt1zZ/1Bs9cPxsanx157LBoEa+8X78SVnc2GAIInee17tjGOA
xfKo7oOfa+AKhST+RJhkhJdTJQx0pA/UEgwJsMLnkeV4nKIyzHz5oIgPvz99Ptam
Wit86RdQ+3szsRWZJSN0HGxWZ/ZppQxnVl9V+JzphXhW0jkwW9+Sh0k+BV+514Az
yUr/AzV0VrG+uLGXcpu/2c5cZ9uSqtoYuX6I5iC/2X2iswuLu+qIp28LwtUhWpBv
+uWVxBTEfVUl4JmQzHqLmaY13Qaj1VKwiEEdhhmP81RO4SVF6GGFAgMBAAGjUzBR
MB0GA1UdDgQWBBRgypQmQ9XWFDi/0/3YqRDbuiDLljAfBgNVHSMEGDAWgBRgypQm
Q9XWFDi/0/3YqRDbuiDLljAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3DQEBCwUA
A4ICAQCLC4XNg4DmQ3cVpXJwjAzgNlh5wc8kgd5FMr/yjf9YZ6Cw2/sIL8IRk2iQ
l/NqPJ1OoiO9u6xqxFrHMKOa95QJ7qC9QQ5Hf9U8MU+ahaF3QP5c7FH7F9LK25iW
lJHccH5/FBEunBX7T75Umz+hb5gz8HSL221ABeeghD7M1gVUD/KH0vOknd0jJJPg
dB00iYStfdw1+E0m5Rw/lpOvGFNHtgcJuTka4lYAkjlkWUdLz0MKPWwFUo2J26x/
8yOcMbcQ+55zoZPBKf1RXJs+IutmNlOj2XWZRNTjO6Mc049nZl9twrEGXRfGxfdi
QHPD1ZZ/v9tR9p0SvAJ0My4HDjdB5r7sGC5TqoWqXua46pI7NbnC3aUR92/75jPB
cqFKbMaga9CnyhPNKJAwft/ZJZ+PV5N33sYUCcjUinWzIAkKwOTSgwFSIaW6e9sx
mwvl0aqOST9bVRjxjy/lqgzOVd1pBh4LAzOAJuE+I7gBYFjp2+KJfkQcE+ThX8AR
cX7j2KNunoTzVee96FjZENhGC9cacojjYbiHqFhMr8clw8GaRoGYkkfQnTghUSBh
5/j2XcKahuPdwh9+/+WCDiO2EBEOXZs+Hp2dbPXT6FpoTS4OEuWk6q3C1ew+qiiv
CLpAag7i/21TvJ1O7tL7wKxkDNomtGViWqTY6xc+CO6mMMTe8A==
-----END CERTIFICATE-----
PKCS7 Data
Shrouded Keybag: PBES2, PBKDF2, AES-256-CBC, Iteration 2048, PRF hmacWithSHA256
Bag Attributes
    localKeyID: C1 55 71 EF 8F CC 95 43 A9 7F 6D 2F B8 CA A7 2E 8D 4A 83 3D 
Key Attributes: <No Attributes>
Enter PEM pass phrase:
Verifying - Enter PEM pass phrase:
-----BEGIN ENCRYPTED PRIVATE KEY-----
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
-----END ENCRYPTED PRIVATE KEY-----
```


###### SELF SIGNED CERTIFICATE
1. Create Server Private Key
```shell
$ openssl genrsa -out 02-01.private.key 4096
```
2. Create CSR (Certificate Signing Request)
```shell
$ openssl req -new -key 02-01.private.key -out 02-02.cert.csr
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:US
State or Province Name (full name) [Some-State]:NJ
Locality Name (eg, city) []:New Jersey
Organization Name (eg, company) [Internet Widgits Pty Ltd]:Yoyodyne Propulsion Systems
Organizational Unit Name (eg, section) []:Black Lectroids
Common Name (e.g. server FQDN or YOUR name) []:blacklectroids.com
Email Address []:john.gant@blacklectroids.com

Please enter the following 'extra' attributes
to be sent with your certificate request
A challenge password []:
An optional company name []:
```
3. Sign the certificate using the Private Key and CSR
```shell
$ openssl x509 -req -days 3650 -in 02-02.cert.csr -signkey 02-01.private.key -out 02-03.cert.crt
Certificate request self-signature ok
subject=C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Black Lectroids, CN=blacklectroids.com, emailAddress=john.gant@blacklectroids.com
```
4. Validate the Certificate
```shell
$ openssl x509 -in 02-03.cert.crt -text
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            21:63:57:b7:e2:0e:60:da:5e:45:2b:27:49:07:e6:62:91:9f:3c:27
        Signature Algorithm: sha256WithRSAEncryption
        Issuer: C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Black Lectroids, CN=blacklectroids.com, emailAddress=john.gant@blacklectroids.com
        Validity
            Not Before: May 29 21:37:44 2024 GMT
            Not After : May 27 21:37:44 2034 GMT
        Subject: C=US, ST=NJ, L=New Jersey, O=Yoyodyne Propulsion Systems, OU=Black Lectroids, CN=blacklectroids.com, emailAddress=john.gant@blacklectroids.com
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
                Public-Key: (4096 bit)
                Modulus:
                    00:c9:98:92:42:5e:a7:a8:1b:01:96:04:33:5b:f2:
                    ab:04:77:81:03:3c:b6:2f:cb:a1:f4:c5:8d:51:93:
                    76:42:24:31:2d:e4:f4:fa:21:2c:22:14:50:21:70:
                    2c:1b:76:2b:2c:5b:df:37:d2:f4:24:35:12:06:79:
                    79:cc:bd:9e:1d:0f:94:a6:fd:3a:25:9b:a4:33:1c:
                    f2:fc:3f:e0:fc:60:09:76:2e:5e:b8:e1:9d:3f:3c:
                    11:ab:94:c0:01:4d:3f:d3:86:e4:b1:77:c7:bc:bf:
                    df:6c:21:79:50:0f:4a:ba:89:9f:ce:cb:c9:43:00:
                    67:7c:6c:41:84:b4:6b:8f:1b:d4:c4:8b:a4:4e:2d:
                    7b:94:8f:63:eb:0b:70:5b:1b:38:0e:ca:4a:06:e1:
                    c9:7d:ee:6d:85:ff:43:0c:0d:de:39:b0:9e:fc:59:
                    06:d9:07:fb:fb:e7:af:ed:16:4e:3e:b4:f5:13:3b:
                    06:f0:63:9e:dd:f0:9b:f5:88:fe:1e:1f:50:d9:aa:
                    38:03:e1:1c:f1:d8:bf:9e:46:36:e6:96:85:07:60:
                    02:e8:fd:cd:54:d9:26:56:b6:08:2f:16:b1:b7:9f:
                    cb:ad:c9:36:25:2e:66:1c:cd:9d:c2:e5:05:8f:39:
                    e8:4f:42:cc:3a:b4:37:a9:6c:bd:0b:34:08:0f:65:
                    8e:9b:b2:34:ec:c9:c5:b0:99:ab:41:cc:56:36:88:
                    59:c0:d6:29:20:29:5f:ad:90:0d:cb:db:d5:89:9c:
                    53:dd:86:53:d7:a5:ad:3d:5a:6c:e0:47:e3:bf:65:
                    21:71:42:cf:f7:79:2c:c7:eb:89:bb:6d:4e:a5:0d:
                    fb:25:eb:e3:21:52:79:0b:5f:62:90:1d:4e:7c:a1:
                    8d:bc:02:45:f5:64:94:5c:a9:2e:9a:09:dc:89:69:
                    c3:fc:ef:5e:8a:11:f0:27:9a:79:38:2e:dd:35:20:
                    b7:e5:4f:71:75:5f:e1:21:95:2f:06:87:36:99:da:
                    32:8f:29:90:1c:d9:62:cc:ef:1a:07:c1:98:86:6e:
                    39:7a:a0:d3:7c:98:1b:c2:bd:41:f1:26:ff:ad:72:
                    bb:4e:96:d3:76:bc:db:1e:db:75:5b:fc:9b:42:39:
                    55:fc:63:57:a1:38:fb:43:07:ff:b9:af:0f:ae:77:
                    e5:36:92:ec:af:c5:c8:81:52:3c:66:24:4e:5a:23:
                    8e:7f:aa:10:4a:de:8d:4a:48:b1:0a:08:c8:4b:9a:
                    62:90:46:6f:30:61:39:b2:cd:8f:21:0e:4b:a2:b2:
                    04:9a:5b:fb:97:18:41:0a:20:29:41:57:e7:be:8b:
                    1c:81:02:55:13:fa:d5:7b:54:fa:21:8e:b2:49:ef:
                    b2:41:0f
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Subject Key Identifier: 
                98:98:DF:DD:5D:62:87:18:4A:CE:21:30:99:86:8C:C2:8F:BD:6C:52
    Signature Algorithm: sha256WithRSAEncryption
    Signature Value:
        ab:a7:99:23:28:12:7a:4a:57:45:6a:d8:e1:9a:49:71:a7:c4:
        64:a0:62:9b:2c:ff:f1:1c:c6:15:4c:9f:d2:d4:4f:da:5f:a0:
        34:7c:41:2d:c6:9e:2d:af:1f:70:ee:f6:c0:f4:ea:e3:aa:ac:
        4a:c2:f4:12:6f:20:3a:41:fa:8f:30:32:ec:d0:9b:c4:96:94:
        b0:ae:18:58:f2:d9:8f:fa:eb:c3:c5:68:90:32:9b:d6:e5:67:
        2f:23:ae:28:d9:94:0e:ab:86:61:5f:cd:00:16:21:6f:91:e3:
        b5:c3:a9:5b:ad:6d:09:40:0b:eb:34:80:07:ac:2b:98:53:47:
        dc:83:32:9a:df:cb:49:f9:ca:cd:81:70:66:15:50:b0:7a:1a:
        65:85:38:61:09:7a:f4:79:99:16:1e:a7:7e:7c:91:ba:fa:d4:
        48:bd:4e:35:d4:39:1a:d3:f9:83:ef:c7:d3:e0:e2:df:b4:4d:
        d3:85:71:9f:07:cf:c5:7d:f1:9b:1f:49:13:44:55:8e:ba:96:
        75:e1:45:5c:7f:a2:b9:23:e0:48:e2:bf:7c:57:15:e5:f4:d1:
        bd:f4:1e:f1:74:49:0d:82:c7:74:18:e0:72:61:01:77:91:f7:
        1d:fc:72:47:da:72:14:38:2e:d4:d7:1f:14:73:93:b7:a7:3f:
        61:5a:6a:0a:c1:b9:3d:92:12:85:38:e4:3e:b8:f0:32:63:a2:
        ce:82:df:c0:96:20:ba:52:d9:9f:9b:f5:42:fc:90:a1:cb:d6:
        7d:9d:18:66:e2:ae:98:7d:71:d3:01:57:92:47:f0:91:3a:6b:
        d0:e9:0b:b8:80:9a:4c:a0:79:e1:15:12:e6:be:9e:32:50:b3:
        e6:a7:d2:76:c7:57:76:7c:e6:7f:45:16:3a:a3:b9:30:2b:c2:
        f7:e7:a2:41:fa:e3:cf:a8:62:11:5f:57:07:ce:c2:41:65:4c:
        3f:09:76:a1:21:d3:30:eb:4c:ee:8b:76:8c:ee:66:e0:f9:70:
        a4:fe:0f:7f:8b:00:1d:9f:0d:0a:d5:d6:b2:1d:26:34:f7:5e:
        f8:66:ef:01:9b:0d:6d:8d:56:22:db:df:57:9e:68:34:d8:31:
        79:c0:4f:05:d5:b6:c5:bd:0d:55:29:60:72:9e:97:b4:d4:06:
        d1:68:4d:aa:c6:11:b6:7c:9f:6a:df:07:31:27:40:12:7f:3f:
        d9:51:a4:74:e6:86:8d:0c:91:75:65:5c:60:ce:5c:ee:f7:1a:
        02:21:9a:ae:89:93:65:f0:6f:9f:ac:1d:e1:8e:a0:b2:98:4f:
        6a:22:5a:1b:6e:0f:e5:5f:47:e1:e2:56:68:2e:c3:13:e9:22:
        44:96:8e:32:a1:96:ba:ef
-----BEGIN CERTIFICATE-----
MIIGIzCCBAugAwIBAgIUIWNXt+IOYNpeRSsnSQfmYpGfPCcwDQYJKoZIhvcNAQEL
BQAwgbkxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjETMBEGA1UEBwwKTmV3IEpl
cnNleTEkMCIGA1UECgwbWW95b2R5bmUgUHJvcHVsc2lvbiBTeXN0ZW1zMRgwFgYD
VQQLDA9CbGFjayBMZWN0cm9pZHMxGzAZBgNVBAMMEmJsYWNrbGVjdHJvaWRzLmNv
bTErMCkGCSqGSIb3DQEJARYcam9obi5nYW50QGJsYWNrbGVjdHJvaWRzLmNvbTAe
Fw0yNDA1MjkyMTM3NDRaFw0zNDA1MjcyMTM3NDRaMIG5MQswCQYDVQQGEwJVUzEL
MAkGA1UECAwCTkoxEzARBgNVBAcMCk5ldyBKZXJzZXkxJDAiBgNVBAoMG1lveW9k
eW5lIFByb3B1bHNpb24gU3lzdGVtczEYMBYGA1UECwwPQmxhY2sgTGVjdHJvaWRz
MRswGQYDVQQDDBJibGFja2xlY3Ryb2lkcy5jb20xKzApBgkqhkiG9w0BCQEWHGpv
aG4uZ2FudEBibGFja2xlY3Ryb2lkcy5jb20wggIiMA0GCSqGSIb3DQEBAQUAA4IC
DwAwggIKAoICAQDJmJJCXqeoGwGWBDNb8qsEd4EDPLYvy6H0xY1Rk3ZCJDEt5PT6
ISwiFFAhcCwbdissW9830vQkNRIGeXnMvZ4dD5Sm/Tolm6QzHPL8P+D8YAl2Ll64
4Z0/PBGrlMABTT/ThuSxd8e8v99sIXlQD0q6iZ/Oy8lDAGd8bEGEtGuPG9TEi6RO
LXuUj2PrC3BbGzgOykoG4cl97m2F/0MMDd45sJ78WQbZB/v756/tFk4+tPUTOwbw
Y57d8Jv1iP4eH1DZqjgD4Rzx2L+eRjbmloUHYALo/c1U2SZWtggvFrG3n8utyTYl
LmYczZ3C5QWPOehPQsw6tDepbL0LNAgPZY6bsjTsycWwmatBzFY2iFnA1ikgKV+t
kA3L29WJnFPdhlPXpa09WmzgR+O/ZSFxQs/3eSzH64m7bU6lDfsl6+MhUnkLX2KQ
HU58oY28AkX1ZJRcqS6aCdyJacP8716KEfAnmnk4Lt01ILflT3F1X+EhlS8GhzaZ
2jKPKZAc2WLM7xoHwZiGbjl6oNN8mBvCvUHxJv+tcrtOltN2vNse23Vb/JtCOVX8
Y1ehOPtDB/+5rw+ud+U2kuyvxciBUjxmJE5aI45/qhBK3o1KSLEKCMhLmmKQRm8w
YTmyzY8hDkuisgSaW/uXGEEKIClBV+e+ixyBAlUT+tV7VPohjrJJ77JBDwIDAQAB
oyEwHzAdBgNVHQ4EFgQUmJjf3V1ihxhKziEwmYaMwo+9bFIwDQYJKoZIhvcNAQEL
BQADggIBAKunmSMoEnpKV0Vq2OGaSXGnxGSgYpss//EcxhVMn9LUT9pfoDR8QS3G
ni2vH3Du9sD06uOqrErC9BJvIDpB+o8wMuzQm8SWlLCuGFjy2Y/668PFaJAym9bl
Zy8jrijZlA6rhmFfzQAWIW+R47XDqVutbQlAC+s0gAesK5hTR9yDMprfy0n5ys2B
cGYVULB6GmWFOGEJevR5mRYep358kbr61Ei9TjXUORrT+YPvx9Pg4t+0TdOFcZ8H
z8V98ZsfSRNEVY66lnXhRVx/orkj4Ejiv3xXFeX00b30HvF0SQ2Cx3QY4HJhAXeR
9x38ckfachQ4LtTXHxRzk7enP2FaagrBuT2SEoU45D648DJjos6C38CWILpS2Z+b
9UL8kKHL1n2dGGbirph9cdMBV5JH8JE6a9DpC7iAmkygeeEVEua+njJQs+an0nbH
V3Z85n9FFjqjuTArwvfnokH648+oYhFfVwfOwkFlTD8JdqEh0zDrTO6LdozuZuD5
cKT+D3+LAB2fDQrV1rIdJjT3Xvhm7wGbDW2NViLb31eeaDTYMXnATwXVtsW9DVUp
YHKel7TUBtFoTarGEbZ8n2rfBzEnQBJ/P9lRpHTmho0MkXVlXGDOXO73GgIhmq6J
k2Xwb5+sHeGOoLKYT2oiWhtuD+VfR+HiVmguwxPpIkSWjjKhlrrv
-----END CERTIFICATE-----
```

#### OPENSSH
- Red Lectroids
```shell
$ ssh-keygen -t rsa -b 4096 -f ./redlectroids -C "Yoyodyne Propulsion Systems - Red Lectroids"
Generating public/private rsa key pair.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in ./redlectroids
Your public key has been saved in ./redlectroids.pub
The key fingerprint is:
SHA256:LuPO0ur/eid+q9Xias9BtMoN3uJ1wb7SJEIJJkNoXcU Yoyodyne Propulsion Systems - Red Lectroids
The key's randomart image is:
+---[RSA 4096]----+
|   +...o.        |
|  o + o E        |
| .   + . ..      |
|        o. o     |
|       .S o o    |
|       +.*.o..   |
|     .o *.B++    |
|    .o.++*++..   |
|   .o=***B=o.    |
+----[SHA256]-----+
```
- Black Lectroids
```shell
$ ssh-keygen -t rsa -b 4096 -f ./blacklectroids -C "Yoyodyne Propulsion Systems - Black Lectroids"
Generating public/private rsa key pair.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in ./blacklectroids
Your public key has been saved in ./blacklectroids.pub
The key fingerprint is:
SHA256:j5C6s+mw7HO1T7l+/Loa/5WvQ8rGe1QMcT+uKr7LFQg Yoyodyne Propulsion Systems - Black Lectroids
The key's randomart image is:
+---[RSA 4096]----+
|              ...|
|              ...|
|       E       +.|
|       .. .   . +|
|      o S. .   o |
|     ... +  . +. |
|  . .. .=..+ =o  |
| ..ooo...=+ *.o. |
| .++=o o*BBB+o.o.|
+----[SHA256]-----+
```


