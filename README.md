# File del Cyber Middleware
Su piattaforme windows il Cyber Middleware è implementato nella dll `cybermw.dll` presente nella cartella `System32`.

Su piattaforme MacOS il cyber middleware PKCS#11 è implementato nello shared object `libcybermw.dylib` presente nella cartella `/Library/Cyberneid/Middleware`.

Il CryptoTokenKit è implementato nell’applicazione CNSApp, presente nella cartella `/Applications/Utilities`, che all’interno esporta il modulo CNSToken.appex.

# Interfaccia PKCS#11
L’interfaccia PKCS#11 implementata è conforme alle specifiche PKCS#11v. 2.20
Il contesto applicativo del PKCS#11 è limitato ai seguenti scenari di utilizzo:
1. autenticazione HTTPS/TLS1.2
2. funzione di “Firma Digitale QSCD” per applicazioni di firma digitale
3. funzione di enrollment di credenziali di firma digitale mediante apposita Certification Authority

Sistemi operativi supportati:
- Windows 7, 8, 8.1, 10, 11
- MacOS 13.x e 14.x

# Installazione
Per installare il middleware occorre scaricare e lanciare il pacchetto di setup relativo al sistema operativo sul quale si vuole installare.
Il pacchetto di setup installerà in pochi secondi il software sulla postazione.

Windows
-
- Setup: `CyberneidMWSetup-1.3.9.13.exe`  
https://github.com/intesi-group/cyberneid-middleware/releases/download/v1.3.9.13/CyberneidMWSetup-1.3.9.13.exe
- Portable 64bit: `cybermw_64.dll`  
https://github.com/intesi-group/cyberneid-middleware/releases/download/v1.3.9.13/cybermw_64.dll
- Portable 32bit: `cybermw_32.dll`  
https://github.com/intesi-group/cyberneid-middleware/releases/download/v1.3.9.13/cybermw_32.dll

MacOS - UNIVERSAL
-
- Setup: `CyberneidMW-1.3.9.13.pkg`  
https://github.com/intesi-group/cyberneid-middleware/releases/download/v1.3.9.13/CyberMW-1.3.9.13.pkg
- Portable: `libcybermw.dylib`  
https://github.com/intesi-group/cyberneid-middleware/releases/download/v1.3.9.13/libcybermw.dylib

# ATR

I dispositivi FirmaQUI (smart card e token USB) sono caratterizzati dal seguente ATR: `3BDB18FF81B1FE451FC38073C8211065434E53107339`.
