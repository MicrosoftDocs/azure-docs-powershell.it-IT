---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsystemcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSystemCertificate.md
ms.openlocfilehash: fa64e9bade3a6cd8ec4edc8e04956c97306328ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507768"
---
# New-AzureRmApiManagementSystemCertificate

## Sinossi
Crea un'istanza di `PsApiManagementSystemCertificate` . Il certificato può essere emesso da una CA privata e verrà installato nel servizio di gestione delle API in `CertificateAuthority` o `Root` Store.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmApiManagementSystemCertificate -StoreName <String> -PfxPath <String> [-PfxPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmApiManagementSystemCertificate** è un comando helper che crea un'istanza di **PsApiManagementSystemCertificate**.
Questo comando viene usato con il cmdlet New-AzureRmApiManagement e Set-AzureRmApiManagement.

## ESEMPI

### Esempio 1: creare e inizializzare un'istanza di PsApiManagementSystemCertificate usando un certificato SSL da un file
```powershell
PS C:\>$rootCa = New-AzureRmApiManagementSystemCertificate -StoreName "Root" -PfxPath "C:\contoso\certificates\privateCa.cer"
PS C:\>$systemCert = @($rootCa)
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -SystemCertificateConfiguration $systemCert
```

Questo comando crea e Inizializza un'istanza di **PsApiManagementSystemCertificate** con un certificato della CA radice. Crea quindi il servizio di gestione delle API che installa il certificato CA nell'archivio radice.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfxPassword
Password per il file di certificato PFX.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPath
Percorso di un file di certificato PFX.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StoreName
Certificato StoreName

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: CertificateAuthority, Root

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### System. Security. SecureString

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Set-AzureRmApiManagement](./Set-AzureRmApiManagement.md)
