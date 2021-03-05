---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987404"
---
# Add-AzTrafficManagerCustomHeaderToEndpoint

## SYNOPSIS
Aggiunge informazioni di intestazione personalizzate a un oggetto endpoint di Gestione traffico locale.

## SINTASSI

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** aggiunge informazioni di intestazione personalizzate a un oggetto endpoint di Gestione traffico Di Azure locale.
È possibile ottenere un endpoint usando i cmdlet New-AzTrafficManagerEndpoint o Get-AzTrafficManagerEndpoint endpoint.

Questo cmdlet opera sull'oggetto endpoint locale.
Eseguire il commit delle modifiche nell'endpoint per Gestione traffico usando il cmdlet Set-AzTrafficManagerEndpoint.

## ESEMPI

### Esempio 1: Aggiungere informazioni di intestazione personalizzate a un endpoint
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Il primo comando crea un endpoint di Gestione traffico di Azure usando il cmdlet **New-AzTrafficManagerEndpoint.**
Il comando archivia l'endpoint locale nella $TrafficManagerEndpoint variabile.
Il secondo comando aggiunge informazioni di intestazione personalizzate all'endpoint archiviato in $TrafficManagerEndpoint.
Il comando finale aggiorna l'endpoint in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerEndpoint.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Specifica il nome delle informazioni di intestazione personalizzate da aggiungere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Specifica un oggetto **TrafficManagerEndpoint** locale.
Questo cmdlet modifica l'oggetto locale.
Per ottenere un **oggetto TrafficManagerEndpoint,** usare il cmdlet Get-AzTrafficManagerEndpoint o New-AzTrafficManagerEndpoint TrafficManagerEndpoint.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Value
Specifica il valore delle informazioni di intestazione personalizzate da aggiungere.

```yaml
Type: System.String
Parameter Sets: (All)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## OUTPUT

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## NOTE

## COLLEGAMENTI CORRELATI

[Remove-AzTrafficManagerCustomHeaderFromEndpoint](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
