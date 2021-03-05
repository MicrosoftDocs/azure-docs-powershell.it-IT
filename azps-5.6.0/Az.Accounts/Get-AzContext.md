---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 2060a1cbe9f002a20b94e82ac9547c5fc96c0e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010126"
---
# Get-AzContext

## SYNOPSIS
Recupera i metadati usati per autenticare le richieste di Gestione risorse di Azure.

## SINTASSI

### GetSingleContext (Impostazione predefinita)
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### ListAllContexts
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il Get-AzContext cmdlet recupera i metadati correnti usati per autenticare le richieste di Gestione risorse di Azure.
Questo cmdlet ottiene l'account di Active Directory, il tenant di Active Directory, la sottoscrizione di Azure e l'ambiente Azure di destinazione.
I cmdlet di Gestione risorse di Azure usano queste impostazioni per impostazione predefinita quando effettuano richieste di Gestione risorse di Azure.

## ESEMPI

### Esempio 1: Recupero del contesto corrente
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

In questo esempio si accede al proprio account con una sottoscrizione di Azure usando Connect-AzAccount e quindi si ottiene il contesto della sessione corrente chiamando Get-AzContext.

### Esempio 2: Elenco di tutti i contesti disponibili
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

In questo esempio vengono visualizzati tutti i contesti attualmente disponibili.  L'utente può selezionare uno di questi contesti usando Select-AzContext.

## PARAMETERS

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -ListAvailable
Elencare tutti i contesti disponibili nella sessione corrente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome del contesto

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshContextFromTokenCache
Aggiornare i contesti dalla cache dei token

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
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

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext

## NOTE

## COLLEGAMENTI CORRELATI

[Set-AzContext](./Set-AzContext.md)

