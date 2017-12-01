[libdefaults]
default_realm = MAFITA.HQ
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = arcfour-hmac
default_tkt_enctypes = arcfour-hmac
permitted_enctypes = arcfour-hmac
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
MAFITA.HQ = {
kdc = veroj2.southcentralus.cloudapp.azure.com
admin_server = veroj2.southcentralus.cloudapp.azure.com
}
[domain_realm]
~                                                                                                                                                     
~               
