## Sewer          

Sewer is a Let's Encrypt(ACME) client.         
It allows you to obtain ssl/tls certificates from Let's Encrypt.       
Sewer currently only supports the DNS mode of validation. The only currently supported DNS provider is cloudflare but I will add more as time progresses.      


## Usage:

```python
import ACMEclient

client = ACMEclient(domain_name='example.com',
                    CLOUDFLARE_DNS_ZONE_ID='random',
                    CLOUDFLARE_EMAIL='example@example.com',
                    CLOUDFLARE_API_KEY='nsa-grade-api-key')
certificate = client.cert()

print "your certicate is:", certificate
print "\n\n"
print "you can write it to a file then add that file to your favourite webserver."
```

## TODO:
- make it DNS provider agnostic
- support more DNS providers
- add robust tests
- be able to handle SAN(subject alternative names)



## FAQ:
- Why another ACME client?          
  I wanted an ACME client that I could use to programmatically(as a library) acquire/get certificates. However I could not 
  find anything satisfactory for use in Python code.
- Why is it called Sewer?
  Because, for the longest time now, getting certificates has felt like wading through sewers. That was before Let's Encrypt showed up.                     
  Also, I really like the Kenyan hip hop artiste going by the name of Kitu Sewer.
