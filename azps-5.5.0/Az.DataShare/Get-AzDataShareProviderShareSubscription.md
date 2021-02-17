---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 5422b43019b7b667ba7ea787663e91e2b6beb118
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198791"
---
# Get-AzDataShareProviderShareSubscription

## SYNOPSIS
Ottiene informazioni sulle sottoscrizioni per le condivisioni consumer sul lato provider.

## SINTASSI

### ByFieldsParameterSet (Impostazione predefinita)
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByProviderShareSubscriptionIdParameterSet
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDataShareProviderSubscription** ottiene informazioni sulle sottoscrizioni per le condivisioni consumer sul lato provider. Se si specifica l'ID sottoscrizione della condivisione, questo cmdlet ottiene informazioni sulla sottoscrizione della condivisione. Se non si specifica l'ID sottoscrizione per la condivisione, questo cmdlet riceve informazioni su tutte le sottoscrizioni per le condivisioni consumer associate alla condivisione.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

Questo comando fornisce informazioni sull'abbonamento alla condivisione consumer associato a Share AdsShare nell'account di condivisione dati WikiAds.

## PARAMETERS

### -AccountName
Nome account Azure DataShare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ResourceGroupName
Gruppo di risorse dell'account Azure DataShare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa della condivisione

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShareName
Nome Azure DataShare.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareSubscriptionId
ID della sottoscrizione per la condivisione consumer

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription

## NOTE

## COLLEGAMENTI CORRELATI
