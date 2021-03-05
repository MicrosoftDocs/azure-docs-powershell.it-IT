---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984744"
---
# Remove-AzDnsZone

## SYNOPSIS
Rimuove un'area DNS da un gruppo di risorse.

## SINTASSI

### Campi
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Oggetto
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzDnsZone** elimina definitivamente un'area DNS (Domain Name System) da un gruppo di risorse specificato.
Vengono eliminati anche tutti i set di record contenuti nell'area.
È possibile passare un **oggetto DnsZone** usando il parametro *Name* o usando l'operatore pipeline oppure in alternativa è possibile specificare i parametri *ZoneName* e *ResourceGroupName.*
È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.
Quando si specifica l'area usando un oggetto **DnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché l'oggetto **DnsZone** locale è stato recuperato (solo le operazioni direttamente nella risorsa zona DNS vengono conteggiati come modifiche, non le operazioni sui set di record all'interno dell'area).
Ciò fornisce protezione per le modifiche simultanee all'area.
Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.

## ESEMPI

### Esempio 1: Rimuovere un'area
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Questo comando rimuove l'area myzone.com denominata risorse dal gruppo di risorse denominato MyResourceGroup.

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

### -Name
Specifica il nome dell'area DNS rimossa dal cmdlet.
È anche necessario specificare il *parametro ResourceGroupName.*
In alternativa, è possibile specificare l'area DNS usando il *parametro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Quando si specifica l'area usando un oggetto **DnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché l'oggetto **DnsZone** locale è stato recuperato (solo le operazioni direttamente nella risorsa zona DNS vengono conteggiati come modifiche, non le operazioni sui set di record all'interno dell'area).
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
passthru

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
Specifica il nome del gruppo di risorse che contiene l'area da rimuovere.
È anche necessario specificare il *parametro ZoneName.*
In alternativa, è possibile specificare l'area DNS usando un **oggetto DnsZone,** passato tramite la pipeline o il parametro *Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Specifica l'area DNS da eliminare.
**L'oggetto DnsZone** passato può essere passato anche tramite la pipeline.
In alternativa, è possibile specificare l'area DNS da eliminare usando i parametri *ZoneName* *e ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

## OUTPUT

### System.Boolean

## NOTE
A causa dell'impatto potenziale dell'eliminazione di un'area DNS, per impostazione predefinita questo cmdlet richiede conferma se la variabile $ConfirmPreference Windows PowerShell ha un valore diverso da Nessuno.
Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.
Se si specifica *Conferma:$False,* il cmdlet non richiede conferma. 

## COLLEGAMENTI CORRELATI

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
