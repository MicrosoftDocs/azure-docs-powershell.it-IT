---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: f84e291c7b69ed8a61288a660b14db9ddf24d95a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018821"
---
# <span data-ttu-id="9714c-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="9714c-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="9714c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9714c-102">SYNOPSIS</span></span>
<span data-ttu-id="9714c-103">Modifica le impostazioni di controllo per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9714c-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="9714c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9714c-104">SYNTAX</span></span>

### <span data-ttu-id="9714c-105">DatabaseParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9714c-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9714c-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9714c-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9714c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9714c-107">DESCRIPTION</span></span>
<span data-ttu-id="9714c-108">Il cmdlet **set-AzSqlDatabaseAudit** modifica le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9714c-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="9714c-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="9714c-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9714c-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9714c-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="9714c-111">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="9714c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9714c-112">EXAMPLES</span></span>

### <span data-ttu-id="9714c-113">Esempio 1: abilitare i criteri di controllo archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="9714c-114">Esempio 2: disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="9714c-115">Esempio 3,1: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure con filtro avanzato usando un predicato T-SQL</span><span class="sxs-lookup"><span data-stu-id="9714c-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="9714c-116">Esempio 3,2: rimuovere l'impostazione di filtro avanzato dai criteri di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="9714c-117">Esempio 4: abilitare i criteri di controllo Hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-117">Example 4: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="9714c-118">Esempio 5: disabilitare i criteri di controllo Hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-118">Example 5: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="9714c-119">Esempio 6: abilitare i criteri di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-119">Example 6: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="9714c-120">Esempio 7: disabilitare i criteri di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-120">Example 7: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="9714c-121">Esempio 8: disabilitare, tramite pipeline, i criteri di controllo di analisi del log di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9714c-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="9714c-122">Esempio 9: disabilitare l'invio di record di controllo di un database SQL di Azure allo spazio di archiviazione BLOB e consentire l'invio di un log di analisi.</span><span class="sxs-lookup"><span data-stu-id="9714c-122">Example 9: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="9714c-123">Esempio 10: consentire l'invio di record di controllo di un database SQL di Azure a archiviazione BLOB, Hub eventi e analisi log.</span><span class="sxs-lookup"><span data-stu-id="9714c-123">Example 10: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="9714c-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9714c-124">PARAMETERS</span></span>

### <span data-ttu-id="9714c-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="9714c-125">-AuditAction</span></span>
<span data-ttu-id="9714c-126">Il set di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-126">The set of audit actions.</span></span>  
<span data-ttu-id="9714c-127">Le azioni supportate per il controllo sono:</span><span class="sxs-lookup"><span data-stu-id="9714c-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="9714c-128">Selezionare</span><span class="sxs-lookup"><span data-stu-id="9714c-128">SELECT</span></span>  
<span data-ttu-id="9714c-129">AGGIORNAMENTO</span><span class="sxs-lookup"><span data-stu-id="9714c-129">UPDATE</span></span>  
<span data-ttu-id="9714c-130">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="9714c-130">INSERT</span></span>  
<span data-ttu-id="9714c-131">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="9714c-131">DELETE</span></span>  
<span data-ttu-id="9714c-132">ESEGUIRE</span><span class="sxs-lookup"><span data-stu-id="9714c-132">EXECUTE</span></span>  
<span data-ttu-id="9714c-133">RICEVERE</span><span class="sxs-lookup"><span data-stu-id="9714c-133">RECEIVE</span></span>  
<span data-ttu-id="9714c-134">RIFERIMENTI</span><span class="sxs-lookup"><span data-stu-id="9714c-134">REFERENCES</span></span>  
<span data-ttu-id="9714c-135">Il modulo generale per la definizione di un'azione da controllare è: [azione] su [oggetto] di [Principal] Nota che [oggetto] nel formato precedente può fare riferimento a un oggetto come una tabella, una vista o una stored procedure oppure un intero database o uno schema.</span><span class="sxs-lookup"><span data-stu-id="9714c-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="9714c-136">Per questi ultimi casi, vengono usati rispettivamente il DATABASE delle maschere:: [dbname] e lo SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="9714c-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="9714c-137">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="9714c-137">For example:</span></span>  
<span data-ttu-id="9714c-138">Selezionare su dbo. MyTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="9714c-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="9714c-139">Selezionare nel DATABASE:: database per pubblico</span><span class="sxs-lookup"><span data-stu-id="9714c-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="9714c-140">Selezionare su SCHEMA:: schema per pubblico</span><span class="sxs-lookup"><span data-stu-id="9714c-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="9714c-141">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="9714c-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="9714c-142">-AuditActionGroup</span></span>
<span data-ttu-id="9714c-143">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="9714c-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="9714c-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="9714c-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="9714c-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="9714c-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="9714c-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="9714c-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="9714c-147">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9714c-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="9714c-148">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="9714c-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="9714c-149">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="9714c-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="9714c-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="9714c-151">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9714c-152">-DatabaseName</span></span>
<span data-ttu-id="9714c-153">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="9714c-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9714c-154">-DatabaseObject</span></span>
<span data-ttu-id="9714c-155">Oggetto database per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9714c-156">-DefaultProfile</span></span>
<span data-ttu-id="9714c-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9714c-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9714c-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="9714c-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="9714c-159">ID risorsa per la regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="9714c-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="9714c-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="9714c-160">-EventHubName</span></span>
<span data-ttu-id="9714c-161">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="9714c-161">The name of the event hub.</span></span> <span data-ttu-id="9714c-162">Se non viene specificato alcuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="9714c-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="9714c-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="9714c-163">-EventHubTargetState</span></span>
<span data-ttu-id="9714c-164">Indica se l'hub eventi è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="9714c-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="9714c-166">Indica se analisi log è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9714c-167">-PassThru</span></span>
<span data-ttu-id="9714c-168">Specifica se l'output dei criteri di controllo alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="9714c-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9714c-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="9714c-169">-PredicateExpression</span></span>
<span data-ttu-id="9714c-170">Predicato T-SQL (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="9714c-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9714c-171">-ResourceGroupName</span></span>
<span data-ttu-id="9714c-172">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9714c-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9714c-173">-RetentionInDays</span></span>
<span data-ttu-id="9714c-174">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-175">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9714c-175">-ServerName</span></span>
<span data-ttu-id="9714c-176">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9714c-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9714c-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="9714c-178">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9714c-178">The storage account resource id</span></span>

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

### <span data-ttu-id="9714c-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="9714c-179">-StorageKeyType</span></span>
<span data-ttu-id="9714c-180">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="9714c-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="9714c-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="9714c-182">ID area di lavoro (ID risorsa di un'area di lavoro analisi log) per un'area di lavoro analisi log in cui si desidera inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="9714c-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="9714c-183">Esempio:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="9714c-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="9714c-184">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9714c-184">-Confirm</span></span>
<span data-ttu-id="9714c-185">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9714c-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9714c-186">-WhatIf</span></span>
<span data-ttu-id="9714c-187">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9714c-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9714c-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9714c-188">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9714c-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9714c-189">CommonParameters</span></span>
<span data-ttu-id="9714c-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9714c-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9714c-191">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9714c-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9714c-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9714c-192">INPUTS</span></span>

### <span data-ttu-id="9714c-193">System. String</span><span class="sxs-lookup"><span data-stu-id="9714c-193">System.String</span></span>

### <span data-ttu-id="9714c-194">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9714c-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="9714c-195">Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="9714c-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="9714c-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="9714c-196">System.String[]</span></span>

### <span data-ttu-id="9714c-197">System. Guid</span><span class="sxs-lookup"><span data-stu-id="9714c-197">System.Guid</span></span>

### <span data-ttu-id="9714c-198">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9714c-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9714c-199">Microsoft. Azure. Commands. SQL. auditing. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="9714c-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="9714c-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9714c-200">OUTPUTS</span></span>

### <span data-ttu-id="9714c-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9714c-201">System.Boolean</span></span>

## <span data-ttu-id="9714c-202">Note</span><span class="sxs-lookup"><span data-stu-id="9714c-202">NOTES</span></span>

## <span data-ttu-id="9714c-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9714c-203">RELATED LINKS</span></span>
