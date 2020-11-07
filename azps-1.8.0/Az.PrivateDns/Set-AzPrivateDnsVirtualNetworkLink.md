---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677724"
---
# Set-AzPrivateDnsVirtualNetworkLink

## Sinossi
Aggiorna/imposta un collegamento di rete virtuale associato a un'area privata e a un gruppo di risorse.

## SINTASSI

### Campi (impostazione predefinita)
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Oggetto
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzPrivateDnsVirtualNetworkLink** aggiorna un collegamento associato a una zona da un gruppo di risorse specificato.
Puoi passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *link* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* *zonename* e *ResourceGroupName* .
Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando specifichi la zona usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), il collegamento non viene aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale. Ciò offre protezione per le modifiche simultanee del collegamento. Questa operazione può essere eliminata usando il parametro *overwrite* , che aggiorna il collegamento indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: impostare un collegamento
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

Questo comando imposta IsRegistrationEnabled su true per il collegamento denominato link, collegato all'area denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.

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

### -InputObject
Oggetto collegamento di rete virtuale da impostare.

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsRegistrationEnabled
Valore booleano che rappresenta se è abilitata la registrazione nel collegamento alla rete virtuale.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del collegamento rimosso da questo cmdlet.
Devi anche specificare il parametro *ResourceGroupName* e *zonename* .
In alternativa, puoi specificare il collegamento DNS privato usando il parametro *link* .

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
Quando specifichi il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), il collegamento non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.
Ciò offre protezione per le modifiche simultanee del collegamento.
Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina il collegamento indipendentemente dalle modifiche simultanee.

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.
Devi anche specificare il parametro *zonename* e *Name* .
In alternativa, puoi specificare il collegamento alla rete virtuale usando un oggetto **PSPrivateDnsVirtualNetworkLink** , passato tramite la pipeline o il parametro *link* .

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

### -Zonename
Specifica il nome dell'area DNS rimossa da questo cmdlet.
Devi anche specificare il *nome* e il parametro *ResourceGroupName* .
In alternativa, puoi specificare il collegamento DNS privato usando il parametro *link* .

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

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink

### System. String

## OUTPUT

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink

## Note

## COLLEGAMENTI CORRELATI

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
