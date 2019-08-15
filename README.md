### jwks-rsa-java
---
https://github.com/auth0/jwks-rsa-java

```java
JwkProvider provider = new UrlJwkProvider("https://samples.auth0.com/");
Jwk jwk = provider.get("{kid of the signing key}");

JwkProvider provider = new UrlJwkProvider(new URL("https://samples.auth0.com/"));
Jwk jwk = provider.get("{kid of the signing key}");

JwkProvider http = new UrlJwkProvider("https://samples.auth0.com/");
JwkProvider provider = new GuavaCachedJwkProvider(http);
Jwk jwk = provider.get("{kid of the signing key}");

JwkProvider url = new UrlJwkProvider();
Bucket bucket = new Bucket(10, 1, TimeUnit.MINUTES);
JwkProvider provider = new RateLimitJwkProvider(url, bucket);
Jwk jwk = provider.get("{kid of the signing key}");

JwkProvider provider = new JwkProviderBuilder("https://samples.auth0.com/")
Jwk jwk = provider.get("{kid of the signing key}");

JwkProvider provider = new JwkProviderBuilder("https://samples.auth0.com/")
  .cached(10, 24, TimeUnit.HOURS)
  .rateLimited(10, 1, TimeUnit.MINUTES)
  .build();
Jwk jwk = provider.get("{kid of the signing key}");
```

```sh
implementation 'com.auth0:jwks-rsa:0.8.3'
implementation 'com.auth0:jwks-rsa:0.8.3'

```

```
```
