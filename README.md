# txtr-server

Test server for TXTR. Includes prosody and ejabberd config files and some required modules.

## Design
![screenshots](https://raw.githubusercontent.com/juanignaciomolina/txtr-server/master/TXTR-LayersDiagram.png)

## XMPP Servers

### Prosody

##### Client-Server
1. XEP-0163: PEP (Avatars) -> **OK**
2. XEP-0198: Stream Management [INFO](https://code.google.com/p/prosody-modules/wiki/mod_smacks) -> **OK**
3. XEP-0280: Message Carbons [INFO](https://code.google.com/p/prosody-modules/wiki/mod_carbons) -> **OK**
4. Compression (zLib) [INFO](http://prosody.im/doc/modules/mod_compression) -> **OK**
5. TLS/SSL [INFO](http://prosody.im/doc/certificates) -> **OK** (self-signed for testing)

##### Server Only
1. zLib [INFO](http://prosody.im/doc/depends) -> **OK**
2. LuaSec 0.5 [INFO](http://prosody.im/doc/depends) -> **OK**
3. LuaDBI *(lua-dbi-mysql)* [INFO](http://prosody.im/doc/depends) -> **OK**
4. MySQL [INFO](http://prosody.im/doc/storage) -> **OK**
5. LuaEvent [INFO](http://prosody.im/doc/depends) -> **OK**


### ejabberd

* Basic config

## TXTR Layer

* pinRequest: Generate new PIN

## Notes

* mysqld.sock [FIX INFO](http://stackoverflow.com/questions/11990708/error-cant-connect-to-local-mysql-server-through-socket-var-run-mysqld-mysq)