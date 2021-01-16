---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333172"
---
# Get-AzAccessToken

## Sinossi
Ottenere un token di accesso non elaborato. Quando si usa-ResourceUrl, verificare che il valore corrisponda all'ambiente Azure corrente. È possibile fare riferimento al valore di `(Get-AzContext).Environment` .

## SINTASSI

### KnownResourceTypeName (impostazione predefinita)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Ottenere il token di accesso

## ESEMPI

### Esempio 1 ottenere un token di accesso non elaborato per endpoint ARM
```powershell
PS C:\> Get-AzAccessToken
```

Ottenere il token di accesso dell'endpoint ResourceManager per l'account corrente

### Esempio 2 ottenere un token di accesso non elaborato per l'endpoint AAD Graph
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Ottenere il token di accesso dell'endpoint di AAD Graph per l'account corrente

### Esempio 3 ottenere un token di accesso non elaborato per l'endpoint AAD Graph
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Ottenere il token di accesso dell'endpoint di AAD Graph per l'account corrente

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Nome tipo facoltativo di resouce, valori supportati: AadGraph, AnalysisServices, ARM, Attestation, batch, datalake, Vault, OperationalInsights, ResourceManager, sinapsi. Il valore predefinito è ARM se non è specificato.

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
URL della risorsa per il quale si richiede il token, ad esempio ' http://graph.windows.net/ '.

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

### -ID tenant
ID tenant facoltativo. usare l'ID tenant del contesto predefinito, se non specificato.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI
