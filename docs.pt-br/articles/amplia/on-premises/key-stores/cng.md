﻿# Armazenamento de chaves via CNG

> [!NOTE]
> Armazenamento de chaves via CNG são compatíveis somente com instalações Windows Server

A **Cryptography API: Next Generation** trabalha com armazenamento de chaves através de um número de **Key Storage Providers (KSPs)** que fazem o trabalho real de armazenar chaves.
Dispositivos como HSMs *(Hardware Security Modules)* e tokens USB criptográficos podem fornecer um CNG KSP que pode ser usado para se comunicar com o dispositivo.

<!--
> [!TIP]
> Embora o Windows Server tenha seu próprio KSP que fornece acesso a seus armazenamentos de chaves nativos, para isso você deve usar [Armazenamento de chaves no store nativo](native.md).
-->

Cada CNG KSP é identificado por um *nome*. Se estiver usando um token de criptografia ou HSM, consulte a documentação do dispositivo para encontrar o nome e o tipo do KSP. Além disso,
consulte a seção abaixo para nomes comuns de KSP.

Para configurar um armazenamento de chaves via CNG no Amplia, use as seguintes configurações:

* **Type**: `CNG`
* **ProviderName**: nome que identifica o KSP a ser usado
* **UseMachineStore**: alguns KSPs tem o conceito de armazenar chaves no *armazenamento do usuário* ou no *armazenamento da máquina* (mais notável o OS's nativo KSP). Por padrão, o armazanemanto do usuário é usado. Defina esta configuração como `true` para usar o armazenamento da máquina.
* **Pin**: o PIN do armazenamento, se necessário

<!--
TODO:
OverrideKeyPins: ?
RememberKeyPins: ?
-->

Configuração de amostra:

```json
"KeyStores": {
	...,
	"MyCngKeyStore": {
		"Type": "Cng",
		"ProviderName": "..."
	},
	...
}
```

## Armazenamento comum de chaves via CNG

Safenet eToken criptográfico USB token:

```json
"CngToken": {
	"Type": "Cng",
	"ProviderName": "SafeNet Smart Card Key Storage Provider"
}
```

## Veja também

* [Armazenamento de chaves](index.md)
* [Amplia on premises](../index.md)
