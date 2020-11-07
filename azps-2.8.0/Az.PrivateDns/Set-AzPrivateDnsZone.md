---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: a5c4ae9492d64bc8c84439f747031d6facd88673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855849"
---
# Set-AzPrivateDnsZone

## Sinossi
Aggiorna una zona DNS privata da un gruppo di risorse.

## SINTASSI

### Campi (impostazione predefinita)
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzPrivateDnsZone** aggiorna in modo permanente una zona DNS (Domain Name System) privata da un gruppo di risorse specificato.
Puoi passare un oggetto **PrivateDnsZone** usando il parametro *PrivateZone* o usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* e *ResourceGroupName* .
Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene aggiornata se è stata modificata in Azure DNS, poiché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come modifiche, le operazioni sui set di record all'interno della zona non lo sono).
Ciò offre protezione per le modifiche di zona simultanee.
Questa operazione può essere eliminata usando il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: aggiorna un'area privata
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

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
Specifica il nome dell'area DNS privata che questo cmdlet aggiorna.
Devi anche specificare il parametro *ResourceGroupName* .
In alternativa, puoi specificare la zona DNS privata usando il parametro *zone* .

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
Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene aggiornata se è stata modificata in Azure DNS, poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come modifiche, le operazioni sui set di record all'interno della zona non lo sono).
Ciò offre protezione per le modifiche di zona simultanee.
Questa operazione può essere eliminata usando il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.

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

### -PrivateZone
Oggetto zone da impostare.

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
Specifica il nome del gruppo di risorse che contiene la zona da aggiornare.
Devi anche specificare il parametro *zonename* .
In alternativa, puoi specificare la zona DNS privata usando un oggetto **dnsZone** , passato tramite il parametro pipeline o *zone* .

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

### -Tag
Tabella hash che rappresenta i tag delle risorse.

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

### System. String

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

## OUTPUT

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone

## Note

## COLLEGAMENTI CORRELATI

[Get-AzPrivateDnsZone](./Get-AzPrivateDnsZone.md)

[New-AzPrivateDnsZone](./New-AzPrivateDnsZone.md)

[Set-AzPrivateDnsZone](./Set-AzPrivateDnsZone.md)
