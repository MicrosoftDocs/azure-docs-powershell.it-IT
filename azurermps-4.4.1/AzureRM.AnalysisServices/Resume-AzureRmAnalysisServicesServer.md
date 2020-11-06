---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508864"
---
# Resume-AzureRmAnalysisServicesServer

## Sinossi
Riprende un'istanza di Analysis Services server

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet Resume-AzureRmAnalysisServicesServer riprende un'istanza di Analysis Services server

## ESEMPI

### Esempio 1
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

Questo comando riprenderà un server in pausa denominato TestServer nel ResourceGroup TestGroup

## PARAMETRI

### -Nome
Nome del server di Analysis Services

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse Azure a cui appartiene il server

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Chiede all'utente di confermare se eseguire l'operazione

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente

```yaml
Type: SwitchParameter
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

## OUTPUT

### Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer

## Note
Alias: Resume-AzureAs

## COLLEGAMENTI CORRELATI

[Get-AzureRmAnalysisServicesServer](./Get-AzureRmAnalysisServicesServer.md)

[Suspend-AzureRmAnalysisServicesServer](./Suspend-AzureRmAnalysisServicesServer.md)
