---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677725"
---
# Remove-AzPrivateDnsZone

## Sinossi
Rimuove una zona DNS privata da un gruppo di risorse.

## SINTASSI

### Campi (impostazione predefinita)
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzPrivateDnsZone** Elimina definitivamente una zona DNS (private Domain Name System) da un gruppo di risorse specificato.
Vengono eliminati anche tutti i set di record contenuti nella zona.
Puoi passare un oggetto **PrivateDnsZone** usando il parametro *PrivateZone* o usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* e *ResourceGroupName* .
Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).
Ciò offre protezione per le modifiche di zona simultanee.
Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: rimuovere un'area privata
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Questo comando rimuove la zona denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.

## PARAMETRI

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

### -Nome
Specifica il nome dell'area DNS privata rimossa da questo cmdlet.
Devi anche specificare il parametro *ResourceGroupName* .
In alternativa, puoi specificare la zona DNS usando il parametro *zone* .

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sovrascrivere
Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).
Ciò offre protezione per le modifiche di zona simultanee.
Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Usato per passare il risultato (booleano) dell'operazione elimina l'area privata più avanti nella pipeline.

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

### -PrivateZone
Oggetto area privata da eliminare.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene la zona da rimuovere.
Devi anche specificare il parametro *zonename* .
In alternativa, puoi specificare la zona DNS usando un oggetto **PrivateDnsZone** , passato tramite il parametro pipeline o *zone* .

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Area DNS privata ResourceID.

```yaml
Type: System.String
Parameter Sets: ResourceId
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

### System. String

## OUTPUT

### System. Boolean

## Note

## COLLEGAMENTI CORRELATI

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
