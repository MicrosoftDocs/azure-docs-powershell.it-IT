---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010046"
---
# Remove-AzApiManagementRegion

## SYNOPSIS
Rimuove un'area di distribuzione esistente dall'istanza di PsApiManagement.

## SINTASSI

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzApiManagementRegion** rimuove un'istanza del tipo **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** da una raccolta **di AdditionalRegions** di provided l'istanza di **tipo Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement.**
Questo cmdlet non modifica la distribuzione da sola ma aggiorna l'istanza di **PsApiManagement** in memoria.
Per aggiornare una distribuzione di Gestione API, passare **psApiManagementInstance modificata** a **Set-AzApiManagement.**

## ESEMPI

### Esempio 1: Rimuovere un'area da un'istanza di PsApiManagement
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Questo comando rimuove l'area geografica denominata Stati Uniti orientali **dall'istanza di PsApiManagement.**

### Esempio 2: Rimuovere un'area da un'istanza di PsApiManagement usando una serie di comandi
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

Il primo comando ottiene un'istanza di **PsApiManagement** dal gruppo di risorse contoso denominato ContosoApi.
Il comando finale rimuove quindi l'area geografica denominata Stati Uniti orientali da tale istanza e quindi aggiorna la distribuzione.

## PARAMETERS

### -ApiManagement
Specifica **l'istanza PsApiManagement** da cui questo cmdlet rimuove l'area di distribuzione aggiuntiva.

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

### -Location
Specifica la posizione dell'area geografica rimossa dal cmdlet.
Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione delle API.
Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider -ProviderManagement "Microsoft.ApiManagement" | dove {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object percorsi

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

### System.String

## OUTPUT

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[Update-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


