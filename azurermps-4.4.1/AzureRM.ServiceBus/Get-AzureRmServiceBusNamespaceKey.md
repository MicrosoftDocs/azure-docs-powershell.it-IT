---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516011"
---
# Get-AzureRmServiceBusNamespaceKey

## Sinossi
Ottiene le stringhe di connessione primarie e secondarie per lo spazio dei nomi.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmServiceBusNamespaceKey** restituisce le stringhe di connessione primarie e secondarie per lo spazio dei nomi specificato. 

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

Stringa di connessione primaria e secondaria allo spazio dei nomi specificato.

## PARAMETRI

### -ResourceGroup
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -Nome
Nome AuthorizationRule dello spazio dei nomi ServiceBus.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Spazio dei nomi
Nome dello spazio dei nomi ServiceBus.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### -ResourceGroup
 System. String
 

### -NamespaceName
 System. String
 

### -AuthorizationRuleName
 System. String

## OUTPUT

### Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys
PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey value} SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey value} PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: AuthoRule1

## Note

## COLLEGAMENTI CORRELATI

