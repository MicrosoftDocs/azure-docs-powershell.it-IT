---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510363"
---
# New-AzureRmRelayHybridConnection

## Sinossi
Crea un HybridConnection nello spazio dei nomi Relay specificato.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### HybridConnectionInputObjectSet
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### HybridConnectionPropertiesSet
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet New-AzureRmRelayHybridConnection crea un HybridConnection nello spazio dei nomi Relay specificato.

## ESEMPI

### Esempio 1-InputObject
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

Crea un nuovo HybirdConnection \` TestHybirdConnection2 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-HybirdConnection \` .

### Esempio 2-proprietà
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

Crea un nuovo HybirdConnection \` TestHybirdConnection1 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-HybirdConnection \` .

## PARAMETRI

### -RequiresClientAuthorization
true se è necessaria l'autorizzazione client per questo HybridConnections; in caso contrario, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserMetadata
Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto HybridConnections.

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome HybridConnections.

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

### -Spazio dei nomi
Nome dello spazio dei nomi.

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

### -ResourceGroupName
Nome del gruppo di risorse.

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

### -ResourceGroupName
System. String

### -NamespaceName
System. String

### -HybridConnectionsName
System. String

### -InputObject
Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes

### -RequiresClientAuthorization
System. Boolean

### -UserMetadata
System. String

## OUTPUT

### Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes

### Esempi-1: InputObject
CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: User Meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 nome: TestHybirdConnection2 tipo: Microsoft. Relay/HybridConnections

### Esempi-2: Proprietà
CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: User Meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 nome: TestHybirdConnection1 tipo: Microsoft. Relay/HybridConnections

## Note

## COLLEGAMENTI CORRELATI

