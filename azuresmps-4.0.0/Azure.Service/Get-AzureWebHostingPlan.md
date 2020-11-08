---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029974"
---
# Get-AzureWebHostingPlan

## Sinossi
Ottiene i piani di hosting Web di Azure nell'abbonamento corrente.

## SINTASSI

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Get-AzureWebHostingPlan** ottiene i piani di hosting Web di Azure nell'abbonamento corrente.

Per impostazione predefinita, **Get-AzureWebHostingPlan** ottiene tutti i piani di hosting di Azure nell'abbonamento corrente e restituisce un oggetto che fornisce informazioni di base sui piani.
Quando usi i parametri *webspace* e *Name* , **Get-AzureWebHostingPlan** restituisce un oggetto piano di hosting specifico.

Per trovare l'abbonamento corrente, usa il parametro *Current* del cmdlet **Get-AzureSubscription** .
Per cambiare l'abbonamento corrente, usare il cmdlet **Select-AzureSubscription** .

## ESEMPI

### Esempio 1: ottenere tutti i piani di hosting Web in un abbonamento
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Questo comando ottiene tutti i piani di hosting Web di Azure nell'abbonamento corrente.

### Esempio 2: ottenere un piano di hosting Web specifico in un abbonamento
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Questo comando ottiene il piano di hosting Web denominato Default0 nella barra multispazio denominata westeuropewebspace nell'abbonamento corrente.

## PARAMETRI

### -Nome
Specifica il nome di un piano nell'abbonamento.
Per impostazione predefinita, questo cmdlet ottiene tutti i piani della sottoscrizione corrente.
Questo parametro non supporta i caratteri jolly.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webspacename
Specifica il nome di uno spazio Web nell'abbonamento.
Per impostazione predefinita, questo cmdlet recupera tutti i siti Web nel webspace specificato.
Questo parametro non supporta i caratteri jolly.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

###  
Puoi passare l'input al cmdlet in base al nome della proprietà, ma non in base al valore.

## OUTPUT

### Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. WebHostingPlan
Per impostazione predefinita, **Get-AzureWebHostingPlan** restituisce una matrice di oggetti **WebHostingPlan** .

## Note

## COLLEGAMENTI CORRELATI

