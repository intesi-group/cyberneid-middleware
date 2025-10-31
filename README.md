# File del Cyber Middleware
Su piattaforme windows il Cyber Middleware è implementato nella dll cybermw.dll presente nella cartella System32

Su piattaforme linux il cyber middleware PKCS#11 è implementato nello shared object libcybermw.so

Su piattaforme MacOS il cyber middleware PKCS#11 è implementato nello shared object libcybermw.dylib presente nella cartella /Library/Cyberneid/Middleware

Il CryptoTokenKit è implementato nell’applicazione CNSApp, presente nella cartella /Applications/Utilities, che all’interno esporta il modulo CNSToken.appex

# Interfaccia PKCS#11
L’interfaccia PKCS#11 implementata è conforme alle specifiche PKCS#11v. 2.20
Il contesto applicativo del PKCS#11 è limitato ai seguenti scenari di utilizzo:
1) autenticazione HTTPS/TLS1.2 con Mozilla Firefox
2) funzione di “Firma Digitale QSCD” per applicazioni di firma digitale
3) funzione di enrollment di credenziali di firma digitale mediante apposita Certification Authority

Sistemi operativi supportati:
- Windows 7, 8, 8.1, 10, 11
- MacOS 13.x e 14.x
- Ubuntu 20.04 e 22.04

Browser supportati:
- Mozilla Firefox
