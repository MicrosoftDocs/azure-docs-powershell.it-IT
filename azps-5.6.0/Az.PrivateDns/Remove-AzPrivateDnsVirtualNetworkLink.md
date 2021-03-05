---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965550"
---
# Remove-AzPrivateDnsVirtualNetworkLink

## SYNOPSIS
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

## DESCRIZIONE
Il cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** elimina definitivamente un collegamento DNS (Domain Name System) privato da un gruppo di risorse specificato.
È possibile passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *Link* o usando l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *Name* *ZoneName* e *ResourceGroupName.*
È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando si specifica il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *link),* il collegamento non viene eliminato se è stato modificato nel DNS privato di Azure perché è stato recuperato l'oggetto **LOCALE PSPrivateDnsVirtualNetworkLink.** Ciò fornisce protezione per le modifiche simultanee all'area. Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: Rimuovere un collegamento
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

Questo comando rimuove il collegamento denominato mylink collegato all'myzone.com di risorse dal gruppo di risorse denominato MyResourceGroup.

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

### -InputObject
L'oggetto collegamento di rete virtuale da rimuovere.

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

### -Name
Specifica il nome del collegamento da eliminare.
È anche necessario specificare il *parametro ResourceGroupName* *e ZoneName.*
In alternativa, è possibile specificare il collegamento usando il *parametro Link.*

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

### -Overwrite
Quando si specifica l'area usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *Link),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché è stato recuperato l'oggetto **LOCALE PSPrivateDnsVirtualNetworkLink.**
Ciò fornisce protezione per le modifiche simultanee all'area.
Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.

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
Consente di passare il risultato (booleano) dell'operazione di eliminazione del collegamento di rete virtuale più avanti nella pipeline.

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
È anche necessario specificare il *parametro ZoneName* *e Name.*
In alternativa, è possibile specificare l'area DNS usando un oggetto **PSPrivateDnsVirtualNetworkLink,** passato tramite la pipeline o il *parametro Link.*

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
Specifica l'ARM ID risorsa del collegamento.

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

### -ZoneName
Specifica il nome dell'area DNS privata a cui è associato il collegamento.
È anche necessario specificare il *parametro ResourceGroupName* *e Name.*
In alternativa, è possibile specificare il collegamento usando il *parametro Link.*

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink

### System.String

## OUTPUT

### System.Boolean

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzPrivateDnsVirtualNetworkLink](./Get-AzPrivateDnsVirtualNetworkLink.md)

[New-AzPrivateDnsVirtualNetworkLink](./New-AzPrivateDnsVirtualNetworkLink.md)

[Set-AzPrivateDnsVirtualNetworkLink](./Set-AzPrivateDnsVirtualNetworkLink.md)
