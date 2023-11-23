# API Versions

The Web PKI provides an API version requirement parameter, in case the developer intends to use a specific feature set and avoid any unecessary update on the user Web PKI components.
In order to do so, use the `requiredApiVersion` parameter on [`init()`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#init) method, e.g.:

```js
pki.init({
    ready: onWebPkiReady,
    requiredApiVersion: pki.apiVersions.v1_2
});
```

In the example above, we defined that we are going to use the feature set of [API 1.2](#v1-2) (and lower), thus any Web PKI component update will only the be required for users with lower versions than the ones defined by [API 1.2](#v1-2).
No unecessary update will be required for users with satisfying versions, even though it is not the latest one.

If the parameter is not set, the dafault requested version is [API 1.3](#v1-3).

<a name="changelog" />
## API changelog

<a name="v1-8-2" />
### 1.8.2 (2023-11-23)

Since lib [2.16.3](../update.md)

- Improve method [`importCertificate`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#importcertificate) supporting multiple calls


<a name="v1-8-1" />
### 1.8.1 (2022-12-17)

- Add methods [encrypt](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#encrypt) and [decrypt](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#decrypt)
- Add Extended Key Usage info to [CertificateModel](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.certificatemodel.html)
- Add parameter `nonExportableKey` on method [generateSoftwareRsaKeyPair](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#generatesoftwarersakeypair)


<a name="v1-7-2" />
### 1.7.2 (2022-07-03)

- Add support to unrestricted size native responses
- Add [CertificateModel](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.certificatemodel.html) international PKI fields: [`PkiArgentinaModel`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.pkiargentinamodel.html), [`PkiEcuadorModel`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.pkiecuadormodel.html), [`PkiParaguayModel`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.pkiparaguaymodel.html), [`PkiPeruModel`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.pkiperumodel.html)
- Add [CertificateModel](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.certificatemodel.html) fields: `certificatePolicies`, `subjectDN`, `issuerDN`


<a name="v1-6-1" />
### 1.6.1 (2020-05-23)

- Add [`downloadToFolder`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#downloadtofolder)&ast; command with TLS 1.2 forced support


<a name="v1-6" />
### 1.6 (2019-10-13)

- Add methods [`keySignData`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#keysigndata) and [`keySignHash`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#keysignhash) for signing with a generated private key Id.
- Add `privateKeyId` parameter to the generate key pair response: [`GenerateKeyPairResponse`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.generatekeypairresponse.html)
- Fix bug on [`sendAuthenticatedRequest`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#sendauthenticatedrequest) response payload when it comes without content length header property.


<a name="v1-5-2" />
### 1.5.2 (2019-07-19)

- Add option for returning de signed document content on local signature commands without the 1MB size limit: [`returnContent`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/enums/_lacuna_web_pki_d_.lacunawebpki.outputmodes.html#returncontent)
- Add certificate validation levels on local signatura commands: [`CertificateValidationLevels`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/enums/_lacuna_web_pki_d_.lacunawebpki.certificatevalidationlevels.html)
- Add vertical and horizontal direction control on PAdES (PDF) visual representation: [`PadesVisualAutoPositioning`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.padesvisualautopositioning.html)
- Add native app life cycle control on `init` method: [`useDomainNativePool`](https://docs.lacunasoftware.com/en-us/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#init)


<a name="v1-5" />
### 1.5 (2018-11-27)

- Add more efficient batch signature command: [`signHashBatch`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signhashbatch)
- Add license v3
- Add mobile integration


<a name="v1-4-1" />
### 1.4.1 (2018-06-15)

- Fix [`sendAuthenticatedRequest`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#sendauthenticatedrequest)&ast; empty buffer bug


<a name="v1-4" />
### 1.4 (2018-02-23)

- Add XML local signature features:
	- [`signFullXml`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signfullxml)&ast;
	- [`signXmlElement`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signxmlelement)&ast;
	- [`openXmlSignature`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#openxmlsignature)&ast;
- Add autheticated request feature:
	- [`sendAuthenticatedRequest`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#sendauthenticatedrequest)&ast;
- Add user error message field on exception object:
	- [`userMessage`](https://docs.lacunasoftware.com/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.exceptionmodel.html#usermessage)


<a name="v1-3" />
### 1.3 (2017-11-10)

- Add improved error handler with exception model
	- [`fail`](https://docs.lacunasoftware.com/content/typedocs/web-pki/interfaces/_lacuna_web_pki_d_.promise.html#fail)


<a name="v1-2" />
### 1.2 (2017-06-19)

- Add local store and PKCS#11 certificate generation features:
	- [`generateSoftwareRsaKeyPair`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#generatesoftwarersakeypair)
	- [`importCertificate`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#importcertificate)
	- [`listTokens`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#listtokens)
	- [`generateTokenRsaKeyPair`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#generatetokenrsakeypair)
	- [`importTokenCertificate`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#importtokencertificate)


<a name="v1-1" />
### 1.1 (2016-08-19)

- Add license v2
- Add local signature features:
	- [`showFileBrowser`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#showfilebrowser)&ast;
	- [`openFile`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#openfile)&ast;
- Add PAdES local signature features:
	- [`signPdf`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signpdf)&ast;
	- [`openPades`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#openpades)&ast;
- Add CAdES local signature features:
	- [`signCades`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signcades)&ast;
	- [`openCades`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#opencades)&ast;


<a name="v1-0" />
### 1.0 (2015-04-28)

- Add basic features:
	- [`init`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#init)
	- [`listCertificates`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#listcertificates)
	- [`readCertificate`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#readcertificate)
	- [`signHash`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signhash)
	- [`signData`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signdata)
	- [`redirectToInstallPage`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#redirecttoinstallpage)
- Add sign batch feature:
	- [`preauthorizeSignatures`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#preauthorizesignatures)
- Add downlad and directory selection features:
	- [`showFolderBrowser`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#showfolderbrowser)
	- [`downloadToFolder`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#downloadtofolder)
	- [`openFolder`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#openfolder)
- Add RestPKI sign integration:
	- [`signWithRestPki`](https://docs.lacunasoftware.com/content/typedocs/web-pki/classes/_lacuna_web_pki_d_.lacunawebpki.html#signwithrestpki)


 &ast; Methods supported only on Windows. For more informations see [Web signatures](../../pki-guide/web-signatures/index.md) article.