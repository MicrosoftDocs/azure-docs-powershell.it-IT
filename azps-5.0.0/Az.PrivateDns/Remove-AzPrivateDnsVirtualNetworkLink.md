---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311154"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## Sinossi
Rimuove un collegamento di rete virtuale da un gruppo di risorse.

## SINTASSI

### Campi (impostazione predefinita)
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** Elimina definitivamente un collegamento DNS (Domain Name System) privato da un gruppo di risorse specificato.
Puoi passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *link* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* *zonename* e *ResourceGroupName* .
Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando specifichi il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), il collegamento non viene eliminato se è stato modificato in Azure private DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale. Ciò offre protezione per le modifiche di zona simultanee. Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: rimuovere un collegamento
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

Questo comando consente di rimuovere il collegamento denominato collegamento collegato a zona myzone.com dal gruppo risorse denominato MyResourceGroup.

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
Oggetto collegamento di rete virtuale da rimuovere.

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

### -Nome
Specifica il nome del collegamento da eliminare.
Devi anche specificare il parametro *ResourceGroupName* e *zonename* .
In alternativa, puoi specificare il collegamento usando il parametro *link* .

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
Quando specifichi la zona usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), la zona non viene eliminata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.
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
Usato per passare il risultato (booleano) dell'operazione elimina il collegamento alla rete virtuale più avanti nella pipeline.

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
Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.
Devi anche specificare il parametro *zonename* e *Name* .
In alternativa, puoi specificare la zona DNS usando un oggetto **PSPrivateDnsVirtualNetworkLink** , passato tramite la pipeline o il parametro *link* .

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
Specifica l'ID delle risorse ARM del collegamento.

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

### -Zonename
Specifica il nome dell'area DNS privata a cui è associato il collegamento.
Devi anche specificare il parametro *ResourceGroupName* e *Name* .
In alternativa, puoi specificare il collegamento usando il parametro *link* .

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink

### System. String

## OUTPUT

### System. Boolean

## Note

## COLLEGAMENTI CORRELATI

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
