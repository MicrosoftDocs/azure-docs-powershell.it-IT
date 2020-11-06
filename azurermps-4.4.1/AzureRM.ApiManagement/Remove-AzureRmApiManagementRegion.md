---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508796"
---
# Remove-AzureRmApiManagementRegion

## Sinossi
Rimuove un'area di distribuzione esistente dall'istanza di PsApiManagement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureRmApiManagementRegion** rimuove l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** da una raccolta di **AdditionalRegions** di cui l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Questo cmdlet non modifica la distribuzione da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di una gestione API, passare il **PsApiManagementInstance** modificato in **Update-AzureRmApiManagement**.

## ESEMPI

### Esempio 1: rimuovere un'area da un'istanza di PsApiManagement
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Questo comando consente di rimuovere l'area geografica denominata East US dall'istanza di **PsApiManagement** .

### Esempio 2: rimuovere un'area da un'istanza di PsApiManagement usando una serie di comandi
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

Questo primo comando consente di ottenere un'istanza di **PsApiManagement** dal gruppo di risorse denominato contoso denominato ContosoApi.
Il comando finale rimuove quindi l'area denominata East US da tale istanza e quindi aggiorna la distribuzione.

## PARAMETRI

### -ApiManagement
Specifica l'istanza di **PsApiManagement** a cui questo cmdlet rimuove l'area di distribuzione aggiuntiva.

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

### -Posizione
Specifica la posizione dell'area rimossa da questo cmdlet.

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

[Update-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


