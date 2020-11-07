---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: dd3c54b8e2769e1b7643d154b259b4f47fd51f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685903"
---
# Set-AzureRmSqlServerAuditingPolicy

## Sinossi
Modifica i criteri di controllo di un server di database SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmSqlServerAuditingPolicy** modifica i criteri di controllo di un server di database SQL di Azure.
Specifica i parametri *ResourceGroupName* e *ServerName* per identificare il server, il parametro *StorageAccountName* per specificare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione da usare.
È anche possibile definire la conservazione per la tabella log di controllo impostando il valore dei parametri *RetentionInDays* e *TableIdentifier* per definire il periodo e il seme per i nomi delle tabelle del log di controllo.
Specifica il parametro *eventType* per definire i tipi di evento da controllare.
Dopo aver eseguito questo cmdlet, è abilitato il controllo dei database che usano i criteri di questo server.
Se il cmdlet riesce e si specifica il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive il criterio di controllo corrente e gli identificatori del server.
Gli identificatori del server includono **ResourceGroupName** e **ServerName**.

## ESEMPI

### Esempio 1: impostare i criteri di controllo di un server SQL di Azure usare il controllo della tabella
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

Questo comando imposta i criteri di controllo del server denominato Server01 per l'uso di un account di archiviazione denominato Storage22.

### Esempio 2: impostare la chiave dell'account di archiviazione di un criterio di controllo esistente di un server SQL di Azure
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

Questo comando imposta i criteri di controllo del server denominato Server01 per usare la chiave secondaria.
Il comando non modifica il nome dell'account di archiviazione.

### Esempio 3: impostare i criteri di controllo di un server SQL di Azure per l'uso di un tipo di evento specifico
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### Esempio 4: impostare i criteri di controllo di un database per l'uso del controllo BLOB
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

Questo comando imposta i criteri di controllo del server denominato Server01 per usare il tipo di evento Login_Failure.
Questo comando non modifica altre impostazioni.

## PARAMETRI

### -AuditActionGroup
Specificare uno o più gruppi di azioni di controllo. Questo parametro è applicabile solo al controllo BLOB.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditType
Specificare il tipo di controllo. I log di controllo possono essere scritti nell'archiviazione di tabella o nell'archiviazione BLOB. Il controllo BLOB offre prestazioni più elevate e supporta il controllo a livello di oggetto.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -EventType
Specifica i tipi di evento da controllare.
Questo parametro è applicabile solo al controllo della tabella.
Puoi specificare diversi tipi di evento.
Puoi specificare tutti per controllare tutti i tipi di evento o nessuno per specificare che non verranno controllati gli eventi.
Se si specificano tutti o nessuno contemporaneamente, il comando non riesce.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.
Per impostazione predefinita, questo cmdlet non genera alcun output.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse che contiene il database.

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

### -RetentionInDays
Specifica il numero di giorni di conservazione per la tabella log di controllo.
Un valore pari a zero (0) indica che la tabella non viene mantenuta.
Questa è l'impostazione predefinita.
Se specifichi un valore maggiore di zero, devi anche specificare un valore per il parametro *TableIdentifer* .

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome del server che contiene il database.

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

### -StorageAccountName
Specifica il nome dell'account di archiviazione per il controllo del database.
I caratteri jolly non sono consentiti.
Se non specifichi questo parametro, il cmdlet usa l'account di archiviazione definito in precedenza come parte dei criteri di controllo del database.
Se è la prima volta che si definisce un criterio di controllo del database e non si specifica questo parametro, il comando non riesce.

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

### -StorageKeyType
Specifica i tasti di scelta per l'archiviazione da usare.
I valori accettabili per questo parametro sono i seguenti:
- Principale
- Secondario il valore predefinito è Primary.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
Specifica il nome della tabella log di controllo.
Specificare questo valore se si specifica un valore maggiore di zero per il parametro *RetentionInDays* .

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. SQL. auditing. Model. AuditType

### Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []

### System. String []

### System. String

### System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## OUTPUT

### Microsoft. Azure. Commands. SQL. auditing. Model. AuditingPolicyModel

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[Usare-AzureRmSqlServerAuditingPolicy](./Use-AzureRmSqlServerAuditingPolicy.md)

[Documentazione di database SQL](https://docs.microsoft.com/azure/sql-database/)


