---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: 4b9186265287c52c27cff6cb1a7f0d0570949e76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991617"
---
# New-AzCommunicationServiceKey

## SYNOPSIS
Rigenerare la chiave di accesso CommunicationService.
PrimaryKey e SecondaryKey non possono essere rigenerate contemporaneamente.

## SINTASSI

### RegenerateExpanded (impostazione predefinita)
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Rigenerare
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### RegenerateViaIdentity
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### RegenerateViaIdentityExpanded
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Rigenerare la chiave di accesso CommunicationService.
PrimaryKey e SecondaryKey non possono essere rigenerate contemporaneamente.

## ESEMPI

### Esempio 1: Rigenerare la chiave primaria usando una tabella hash IRegenerateKeyParameters
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

Invalida la chiave primaria precedente, rigenera una nuova chiave e la restituisce.

### Esempio 2: Rigenera la chiave secondaria con KeyType
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

Invalida la chiave secondaria precedente, rigenera una nuova chiave e la restituisce.

## PARAMETERS

### -CommunicationServiceName
Nome della risorsa CommunicationService.

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyType
KeyType da rigenerare.
Deve essere "principale" o "secondario" (senza distinzione tra maiuscole e minuscole).

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameter
Parameters descrive la richiesta di rigenerare le chiavi di accesso da creare, vedere la sezione NOTES per le proprietà PARAMETER e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse che contiene la risorsa.
È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.
L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters

### Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ICommunicationIdentity> : parametro identity
  - `[CommunicationServiceName <String>]`: nome della risorsa CommunicationService.
  - `[Id <String>]`: percorso di identità della risorsa
  - `[Location <String>]`: l'area geografica Azure
  - `[OperationId <String>]`: ID di un'operazione di sincronizzazione in corso
  - `[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.
  - `[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

PARAMETER: <IRegenerateKeyParameters> Parameters descrive la richiesta di rigenerare le chiavi di accesso
  - `[KeyType <KeyType?>]`: il tipo di chiave da rigenerare. Deve essere "principale" o "secondario" (senza distinzione tra maiuscole e minuscole).

## COLLEGAMENTI CORRELATI

