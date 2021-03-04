---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: e61eea1d00468937a46f90fdd6a995f5f53ff468
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956445"
---
# Restart-AzCloudService

## SYNOPSIS
Riavvia una o più istanze di ruoli in un servizio cloud.

## SINTASSI

### RestartExpanded (impostazione predefinita)
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### RestartViaIdentityExpanded
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIZIONE
Riavvia una o più istanze di ruoli in un servizio cloud.

## ESEMPI

### Esempio 1: Riavviare le istanze del ruolo del servizio cloud
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

Questo comando riavvia 2 istanze di ruoli ContosoFrontEnd_IN_0 e ContosoBackEnd_IN_1 del servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.

### Esempio 2: Riavviare tutti i ruoli del servizio cloud
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

Questo comando riavvia tutte le istanze di ruolo del servizio cloud denominate ContosoCS che appartengono al gruppo di risorse denominato ContosOrg.

## PARAMETERS

### -AsJob
Eseguire il comando come processo

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome del servizio cloud.

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Eseguire il comando in modo asincrono

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce true quando il comando ha esito positivo

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstance
Elenco dei nomi di istanza dei ruoli del servizio cloud.
Il valore "*" indica tutte le istanze del ruolo del servizio cloud.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.
L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.

```yaml
Type: System.String
Parameter Sets: RestartExpanded
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

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity

## OUTPUT

### System.Boolean

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


INPUTOBJECT <ICloudServiceIdentity> : parametro Identity
  - `[CloudServiceName <String>]`: 
  - `[Id <String>]`: percorso di identità della risorsa
  - `[ResourceGroupName <String>]`: 
  - `[RoleInstanceName <String>]`: nome dell'istanza del ruolo.
  - `[RoleName <String>]`: nome del ruolo.
  - `[SubscriptionId <String>]`: le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.
  - `[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento. I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.

## COLLEGAMENTI CORRELATI

