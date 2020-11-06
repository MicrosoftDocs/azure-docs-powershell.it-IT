---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: 2694ce516b1bb3202fc194e1c1eec55610f7b92a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508267"
---
# Get-AzureRmConsumptionUsageDetail

## Sinossi
Ottenere i dettagli sull'utilizzo dell'abbonamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Abbonamento (impostazione predefinita)
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Fattura
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BillingPeriod
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmConsumptionUsageDetail** ottiene i dettagli sull'utilizzo dell'abbonamento. 

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

Ottenere i dettagli sull'utilizzo della fattura con il nome specificato e includere la proprietà MeterDetails nel risultato.

### Esempio 2
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

Ottenere i dettagli sull'utilizzo del periodo di fatturazione con il nome specificato e includere la proprietà AdditionalProperties nel risultato.

### Esempio 3
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

Ottenere i dettagli sull'utilizzo dell'abbonamento compreso tra 2017-01-17 e 2017-01-19.

## PARAMETRI

### -BillingPeriodName
Nome di un periodo di fatturazione specifico per ottenere i dettagli sull'utilizzo associati.

```yaml
Type: String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
Data di fine (in formato UTC) degli usi.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeAdditionalProperties
Includi proprietà aggiuntive negli usi.

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

### -IncludeMeterDetails
Includere i dettagli dei contatori negli usi.

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

### -Invoicename
Nome di una fattura specifica per ottenere i dettagli sull'utilizzo associati.

```yaml
Type: String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Determinare il numero massimo di record da restituire.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartDate
Data di inizio (in formato UTC) degli usi.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. consume. Models. PSUsageDetail, Microsoft. Azure. Commands. consumer, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]

## Note

## COLLEGAMENTI CORRELATI

