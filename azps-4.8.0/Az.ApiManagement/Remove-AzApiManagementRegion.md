---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188622"
---
# Remove-AzApiManagementRegion

## Sinossi
Rimuove un'area di distribuzione esistente dall'istanza di PsApiManagement.

## SINTASSI

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzApiManagementRegion** rimuove l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** da una raccolta di **AdditionalRegions** di cui l'istanza di tipo **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.
Questo cmdlet non modifica la distribuzione da solo, ma aggiorna l'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di una gestione API, passare la **PsApiManagementInstance** modificata a **set-AzApiManagement**.

## ESEMPI

### Esempio 1: rimuovere un'area da un'istanza di PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Questo comando consente di rimuovere l'area geografica denominata East US dall'istanza di **PsApiManagement** .

### Esempio 2: rimuovere un'area da un'istanza di PsApiManagement usando una serie di comandi
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
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

### -DefaultProfile

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

### -Posizione
Specifica la posizione dell'area rimossa da questo cmdlet.
Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.
Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

### System. String

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## Note

## COLLEGAMENTI CORRELATI

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


