---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687095"
---
# New-AzureRmWcfRelay

## Sinossi
Crea un WcfRelay nello spazio dei nomi Relay specificato.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### WcfRelayInputObjectSet
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### WcfRelayPropertiesSet
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet New-AzureRmWcfRelay crea un WcfRelay nello spazio dei nomi Relay specificato.

## ESEMPI

### Esempio 1-InputObject
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

Crea un nuovo WcfRelay \` TestWCFRelay2 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-Relay \` .

### Esempio 2-proprietà
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

Crea un nuovo WcfRelay \` TestWCFRelay \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-relay1 \` .

## PARAMETRI

### -RequiresClientAuthorization
true se l'autorizzazione client è necessaria per questo inoltro; in caso contrario, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequiresTransportSecurity
true se è necessaria la sicurezza del trasporto per il relè; in caso contrario, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
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
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WcfRelayType
Tipo WcfRelay.
I valori possibili includono:' NetTcp ' o ' http '

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

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
Oggetto WcfRelay.

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome WcfRelay.

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

### -WcfRelayName
System. String

### -InputObject
Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes

### -WcfRelayType
System. String

### -RequiresClientAuthorization
System. Boolean

### -RequiresTransportSecurity
System. Boolean

### -UserMetadata
System. String

## OUTPUT

### Esempio 1-InputObject

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true dinamico: false UserMetadata: TestWCFRelay2 ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays

### Esempio 2-proprietà

### Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes
RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true dinamico: false UserMetadata: ID metadati dell'utente:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays

## Note

## COLLEGAMENTI CORRELATI

