---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f97f6c59bc1888f511d84ed49e6d1d49a5d7f57f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512035"
---
# New-AzureRmApiManagementCertificate

## Sinossi
Crea un certificato di gestione API da usare durante l'autenticazione con backend.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### LoadFromFile (impostazione predefinita)
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Non elaborate
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmApiManagementCertificate** crea un certificato di gestione delle API di Azure.

## ESEMPI

### Esempio 1: creare e caricare un certificato
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

Questo comando carica un certificato per la gestione delle API. Questo certificato può essere usato per l'autenticazione reciproca con backend usando i criteri.

## PARAMETRI

### -CertificateId
Specifica l'ID del certificato da creare.
Se non specifichi questo parametro, viene generato un ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Contesto
Specifica un oggetto **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -PfxBytes
Specifica una matrice di byte del file di certificato in formato pfx.
Questo parametro è obbligatorio se non specifichi il parametro *PfxFilePath* .

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxFilePath
Specifica il percorso del file di certificato in formato pfx per creare e caricare.
Questo parametro è obbligatorio se non specifichi il parametro *PfxBytes* .

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PfxPassword
Specifica la password per il certificato.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext

### System. String

### System. Byte []

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmApiManagementCertificate](./Get-AzureRmApiManagementCertificate.md)

[Remove-AzureRmApiManagementCertificate](./Remove-AzureRmApiManagementCertificate.md)

[Set-AzureRmApiManagementCertificate](./Set-AzureRmApiManagementCertificate.md)


