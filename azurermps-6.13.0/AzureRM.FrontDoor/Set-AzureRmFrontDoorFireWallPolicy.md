---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685430"
---
# Set-AzureRmFrontDoorFireWallPolicy

## Sinossi
aggiornare i criteri di WAF

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### ByFieldsParameterSet (impostazione predefinita)
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmFrontDoor** aggiorna un criterio WAF esistente. Se non vengono forniti parametri di input, verranno usati i parametri obsoleti dei criteri di WAF esistenti.

## ESEMPI

### Esempio 1: aggiornare un criterio di WAF esistente
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

aggiornare un criterio di WAF esistente

### Esempio 2: aggiornare un criterio di WAF esistente
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

aggiornare un criterio di WAF esistente

### Esempio 3: aggiornare un criterio di WAF esistente
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

aggiornare un criterio di WAF esistente

### Esempio 4: aggiornare tutti i criteri di WAF in $resourceGroup
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

aggiornare tutti i criteri di WAF in $resourceGroup

## PARAMETRI

### -Customrule
Regole personalizzate all'interno del criterio

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -EnabledState
Se il criterio si trova in stato abilitato o disabilitato.
I valori possibili includono:' disabled ',' Enabled '

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
L'oggetto FireWallPolicy da aggiornare.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ManagedRule
Regole gestite all'interno del criterio

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Modalità
Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.
I valori possibili includono: "prevenzione", "rilevamento"

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Il nome del FireWallPolicy da aggiornare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Il gruppo di risorse a cui appartiene FireWallPolicy.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa di FireWallPolicy da aggiornare

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy

### System. String

## OUTPUT

### Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy

## Note

## COLLEGAMENTI CORRELATI

[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
