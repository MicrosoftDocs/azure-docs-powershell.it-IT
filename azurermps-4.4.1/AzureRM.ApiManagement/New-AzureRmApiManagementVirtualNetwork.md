---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508831"
---
# New-AzureRmApiManagementVirtualNetwork

## Sinossi
Crea un'istanza di PsApiManagementVirtualNetwork.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmApiManagementVirtualNetwork** è un comando helper per creare un'istanza di **PsApiManagementVirtualNetwork**.
Questo comando viene usato con il cmdlet **set-AzureRMApiManagementVirtualNetworks** .

## ESEMPI

### Esempio 1: creare una rete virtuale
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

Questo esempio crea una rete virtuale e quindi chiama il cmdlet **set-AzureRmApiManagementVirtualNetworks** .

## PARAMETRI

### -Posizione
Specifica la posizione della rete virtuale in cui questo cmdlet crea l'istanza.

I valori accettabili per questo parametro sono i seguenti:

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetResourceId
Specifica l'ID della risorsa subnet della rete virtuale.

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

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork

## Note

## COLLEGAMENTI CORRELATI

