---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: c99a7c24e6582db9eea0bcf2811afded8c985489
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194047"
---
# Get-AzMySqlFlexibleServerConnectionString

## SYNOPSIS
Ottenere la stringa di connessione in base al provider di connessione client.

## SINTASSI

### Ottieni (impostazione predefinita)
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIZIONE
Ottenere la stringa di connessione in base al provider di connessione client.

## ESEMPI

### Esempio 1: Ottenere la stringa di connessione in base al nome
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

Questo cmdlet mostra la stringa di connessione di un client per nome server.

### Esempio 2: Ottenere la stringa di connessione del server MySql in base all'identità
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

Questo cmdlet ottiene la stringa di connessione del server MySql in base all'identità.

## PARAMETERS

### -Client
Provider di connessione client.

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
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Server per la stringa di connessione.
Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome del server.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID sottoscrizione che identifica una sottoscrizione di Azure.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity

## OUTPUT

### System.String

## NOTE

ALIAS

PROPRIETÀ DEI PARAMETRI COMPLESSE

Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate. Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.


<IMySqlIdentity>INPUTOBJECT: server per la stringa di connessione.
  - `[ConfigurationName <String>]`: nome della configurazione del server.
  - `[DatabaseName <String>]`: nome del database.
  - `[FirewallRuleName <String>]`: nome della regola del firewall del server.
  - `[Id <String>]`: percorso di identità della risorsa
  - `[KeyName <String>]`: nome della chiave del server.
  - `[LocationName <String>]`: nome della posizione.
  - `[ResourceGroupName <String>]`: nome del gruppo di risorse. Per il nome non viene distinzione tra maiuscole e minuscole.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.
  - `[ServerName <String>]`: nome del server.
  - `[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.
  - `[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.

## COLLEGAMENTI CORRELATI

