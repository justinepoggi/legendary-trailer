### HTTPS Server Side

HTTPS is used to secure an HTTP connection (encryption of data + authentication of the server from the client's perspective). It uses now TLS as secure protocol but this is still often referred to as SSL (which is the "former" TLS).

The client makes a connection to a secure server. The server sends its certificate to the client. The client has a trust store which contains the list of trusted certificates and authorities. The server has either a certificate signed by a certification authority or a self-signed certificate. In both case they need to be present in the trust store of the client for the connection to be secure and successfuly set up. The client could also present its certificate to the server, but that is optional.

The certificates are signed and verified using private keys. The key store is holding such keys. 

The JVM has a default trust store under `$JAVA_HOME/lib/security/cacerts`, which contains all the well-known certificates. It has a default password, which is `changeit`.

The trust store and the key store locations can be customised, however this is not usually the case for the trust store. Several system properties can be passed to a Java application to change the default trust store and/or specify a key store.

#### Resources

[Java trust store and key store configuration](https://doc.nuxeo.com/nxdoc/trust-store-and-key-store-configuration/)
[HTTPS and Spring Boot](http://zetcode.com/springboot/https/)
[TLS configuration in Tomcat](https://tomcat.apache.org/tomcat-6.0-doc/ssl-howto.html)

### Support or Contact

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
