---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973022"
---
# Get-AzAccessToken

## SYNOPSIS
Ottieni il token di accesso non elaborato. Quando si usa -ResourceUrl, verificare che il valore corrisponda all'ambiente Azure corrente. È possibile fare riferimento al valore di `(Get-AzContext).Environment` .

## SINTASSI

### KnownResourceTypeName (Default)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Ottieni token di accesso

## ESEMPI

### Esempio 1 Ottenere il token di accesso non elaborati per ARM endpoint
```powershell
PS C:\> Get-AzAccessToken
```

Ottenere il token di accesso dell'endpoint ResourceManager per l'account corrente

### Esempio 2: Ottenere il token di accesso non elaborato per l'endpoint del grafico AAD
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Ottenere il token di accesso dell'endpoint grafico AAD per l'account corrente

### Esempio 3: Ottenere il token di accesso non elaborato per l'endpoint del grafico AAD
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Ottenere il token di accesso dell'endpoint grafico AAD per l'account corrente

## PARAMETERS

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

### -ResourceTypeName
Nome del tipo di resouce facoltativo, valori supportati: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Il valore predefinito è Arm, se non è specificato.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
URL della risorsa per il token richiesto, ad esempio ' http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
ID tenant facoltativo. Se non viene specificato, usare l'ID tenant del contesto predefinito.

```yaml
Type: System.String
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

### System.String

## NOTE

## COLLEGAMENTI CORRELATI
