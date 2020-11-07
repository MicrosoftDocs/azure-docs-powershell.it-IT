---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: f6e466b4aa25532a1ea025684dbfe0f20e698f75
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861878"
---
# New-AzWebAppSSLBinding

## Sinossi
Crea un binding a un certificato SSL per una Web App Azure.

## SINTASSI

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzWebAppSSLBinding** crea un binding di certificato SSL (Secure Socket Layer) per un'app Azure Web.
Il cmdlet crea un binding SSL in due modi: 

- Puoi associare un'app Web a un certificato esistente.
- Puoi caricare un nuovo certificato e quindi associare l'app Web a questo nuovo certificato.

Indipendentemente dall'approccio usato, il certificato e l'app Web devono essere associati allo stesso gruppo di risorse Azure.
Se si ha un'app Web nel gruppo di risorse a e si vuole associare l'app Web a un certificato nel gruppo di risorse B, l'unico modo per eseguire questa operazione consiste nel caricare una copia del certificato nel gruppo di risorse A.

Se si carica un nuovo certificato, ricordare i requisiti seguenti per un certificato SSL di Azure: 

- Il certificato deve contenere una chiave privata. 
- Il certificato deve usare il formato PFX (Personal Information Exchange). 
- Il nome dell'oggetto del certificato deve corrispondere al dominio usato per accedere all'app Web. 
- Il certificato deve usare un minimo di crittografia a 2048 bit.

## ESEMPI

### Esempio 1: associare un certificato a un'app Web
```
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Questo comando associa un certificato Azure esistente (un certificato con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) all'app Web denominata ContosoWebApp.

## PARAMETRI

### -CertificateFilePath
Specifica il percorso del file per il certificato da caricare.

Il parametro *CertificateFilePath* è obbligatorio solo se il certificato non è stato ancora caricato in Azure.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Specifica la password di decrittografia per il certificato.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'app Web.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui è assegnato il certificato.

Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Specifica il nome dello slot di distribuzione dell'app Web.
Puoi usare il cmdlet Get-AzWebAppSlot per ottenere uno slot.

Gli slot di distribuzione consentono di organizzare e convalidare le app Web senza che le app siano accessibili tramite Internet.
In genere, le modifiche verranno distribuite in un sito di staging, convalidarle e quindi distribuirle nel sito di produzione (accessibile tramite Internet).

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Specifica se il certificato è abilitato.
Imposta il parametro *SSLState* su 1 per abilitare il certificato oppure imposta *SSLState* su 0 per disabilitare il certificato.

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identificazione personale
Specifica l'identificatore univoco per il certificato.

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web App
Specifica un'app Web.
Per ottenere un'app Web, usa il cmdlet Get-AzWebApp.

Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Specifica il nome dell'app Web per cui è in corso la creazione del nuovo binding SSL.

Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Sito
Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


