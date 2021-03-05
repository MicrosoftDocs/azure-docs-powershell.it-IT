---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: c1bdb71dcfbc554d8d9ca1d7d09a80053a564402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001997"
---
# New-AzApiManagementSslSetting

## SYNOPSIS
Crea un'istanza di PsApiManagementSslSetting

## SINTASSI

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Comando helper per creare un'istanza di PsApiManagementSslSetting.
Questo comando deve essere usato con New-AzApiManagement comando.

## ESEMPI

### Esempio 1: Creare un'impostazione SSL per abilitare TLS 1.0 sia in Backend che frontend
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

Creare una nuova istanza di PsApiManagementSslSetting per abilitare TLSv 1.0 sia in Frontend (tra client che APIM) e Backend (tra APIM e Backend) di ApiManagement Gateway.

## PARAMETERS

### -BackendProtocol
Impostazioni del protocollo di sicurezza back-end. Questo parametro è facoltativo.
Le impostazioni del protocollo valide sono `Tls11` Tls 1.1 `Tls10` - Tls 1.0 - SSL `Ssl30` 3.0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CipherSuite
Impostazioni dei pacchetti di crittografia Ssl nell'ordine specificato. Questo parametro è facoltativo.
Le impostazioni valide sono `TripleDes168` - Abilitare/Disabilitare Tripe Des 168

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendProtocol
Impostazioni dei protocolli di sicurezza frontend. Questo parametro è facoltativo.
Le impostazioni del protocollo valide sono `Tls11` Tls 1.1 `Tls10` - Tls 1.0 - SSL `Ssl30` 3.0


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerProtocol
Impostazioni del protocollo server come Http2. Questo parametro è facoltativo.
Le impostazioni valide sono `Http2` - Abilitare Http 2.0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings

## NOTE

## COLLEGAMENTI CORRELATI

[New-AzApiManagement](./New-AzApiManagement.md)

