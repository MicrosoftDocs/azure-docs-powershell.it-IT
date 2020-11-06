---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508783"
---
# Set-AzureRmApiManagementProperty

## Sinossi
Modifica una proprietà di gestione API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmApiManagementProperty** modifica una proprietà di gestione delle API di Azure.

## ESEMPI

### Esempio 1: modificare i tag in una proprietà
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

Il primo comando assegna due valori alla variabile $Tags.

Il secondo comando modifica la proprietà che contiene l'ID Property11.
Il comando assegna le stringhe in $Tags come tag nella proprietà.

### Esempio 2: modificare una proprietà per avere un valore segreto
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

Questo comando modifica la proprietà da crittografare.

## PARAMETRI

### -Contesto
Specifica un oggetto **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome della proprietà.
La lunghezza massima è di 100 caratteri.
I nomi contengono solo lettere, cifre, punto, trattino e caratteri di sottolineatura.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Indica che questo cmdlet restituisce il **PsApiManagementProperty** modificato da questo cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PropertyId
Specifica un ID della proprietà modificata da questo cmdlet.

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

### -Segreto
Indica che il valore della proprietà è un segreto e deve essere crittografato.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Specifica una matrice di tag che questo cmdlet associa alla proprietà.
Puoi usare i tag per filtrare l'elenco delle proprietà.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valore
Specifica un valore per la proprietà.
Questo valore può contenere espressioni di criteri.
La lunghezza massima è di 1000 caratteri.
Il valore potrebbe non essere vuoto o costituito solo da spazi vuoti.

```yaml
Type: System.String
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

## OUTPUT

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmApiManagementProperty](./Get-AzureRmApiManagementProperty.md)

[New-AzureRmApiManagementProperty](./New-AzureRmApiManagementProperty.md)

[Remove-AzureRmApiManagementProperty](./Remove-AzureRmApiManagementProperty.md)


