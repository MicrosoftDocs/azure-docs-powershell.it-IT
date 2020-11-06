---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508772"
---
# Update-AzureRmApiManagementRegion

## Sinossi
Aggiorna l'area di distribuzione esistente nell'istanza di PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Update-AzureRmApiManagementRegion** aggiorna un'istanza esistente di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** in una raccolta di oggetti **AdditionalRegions** di un'istanza specificata di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Questo cmdlet non distribuisce nulla, ma aggiorna un'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di una gestione API, usare il **PsApiManagementInstance** modificato per il cmdlet Update-AzureRmApiManagementDeployment.

## ESEMPI

## PARAMETRI

### -ApiManagement
Specifica l'istanza di **PsApiManagement** per l'aggiornamento di un'area di distribuzione esistente.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Capacità
Specifica il nuovo valore della capacità SKU per l'area di distribuzione.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Posizione
Specifica la posizione dell'area di distribuzione da aggiornare.

I valori validi sono:

- Stati Uniti nord-centrale
- Stati Uniti del centro sud
- Stati Uniti centrali
- Europa occidentale
- Nord Europa
- Ovest degli Stati Uniti
- Stati Uniti orientali
- Stati Uniti Est 2
- Giappone est
- Giappone ovest
- Brasile sud
- Asia sud-orientale
- Asia orientale
- Australia Est
- Australia sud-est

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Specifica il nuovo valore di livello per l'area di distribuzione.

I valori validi sono:

- Sviluppo
- Standard
- Premium

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Specifica una configurazione di rete virtuale per l'area di distribuzione.
Passando $null verrà rimossa la configurazione della rete virtuale per l'area geografica.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PsApiManagement
Il parametro ' ApiManagement ' accetta il valore di tipo ' PsApiManagement ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[Remove-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[Update-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)
