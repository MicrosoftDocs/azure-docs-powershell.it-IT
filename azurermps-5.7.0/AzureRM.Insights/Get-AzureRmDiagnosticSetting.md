---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508135"
---
# Get-AzureRmDiagnosticSetting

## Sinossi
Ottiene le categorie registrate e i grani temporali.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmDiagnosticSetting** ottiene le categorie e i grani temporali registrati per una risorsa.

Una granulosità temporale è l'intervallo di aggregazione di una metrica.

## ESEMPI

### Esempio 1: ottenere lo stato delle categorie di registrazione e dei grani temporali
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

Questo comando ottiene le categorie e i grani temporali registrati per un Vault di chiave di Azure con un *resourceId* di/subscriptions/1a66ce04-B633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.

## PARAMETRI

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

### -ResourceId
Specifica l'ID della risorsa.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)


