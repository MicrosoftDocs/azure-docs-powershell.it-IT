---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856734"
---
# <span data-ttu-id="7691e-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7691e-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="7691e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7691e-102">SYNOPSIS</span></span>
<span data-ttu-id="7691e-103">**Importante: questo cmdlet è deprecato, [set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) la sostituisce.**</span><span class="sxs-lookup"><span data-stu-id="7691e-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="7691e-104">Modifica le impostazioni di controllo per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7691e-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="7691e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7691e-105">SYNTAX</span></span>

### <span data-ttu-id="7691e-106">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7691e-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7691e-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="7691e-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7691e-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="7691e-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7691e-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="7691e-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7691e-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7691e-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7691e-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7691e-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7691e-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7691e-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7691e-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7691e-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7691e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7691e-114">DESCRIPTION</span></span>
<span data-ttu-id="7691e-115">Il cmdlet **set-AzSqlDatabaseAuditing** modifica le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7691e-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="7691e-116">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="7691e-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="7691e-117">La destinazione log di controllo viene determinata specificando uno dei parametri di switch seguenti: BlobStorage, LogAnalytics o EventHub (se non è specificato nessuno, il valore predefinito è BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="7691e-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="7691e-118">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="7691e-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="7691e-119">Quando la destinazione dei log di controllo è archiviazione BLOB, specificare il parametro *StorageAccountName* per determinare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7691e-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7691e-120">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="7691e-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="7691e-121">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive le impostazioni di controllo correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="7691e-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="7691e-122">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="7691e-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="7691e-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7691e-123">EXAMPLES</span></span>

### <span data-ttu-id="7691e-124">Esempio 1: abilitare i criteri di controllo archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="7691e-125">Esempio 2: disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="7691e-126">Esempio 3: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure usando un account di archiviazione da un abbonamento diverso</span><span class="sxs-lookup"><span data-stu-id="7691e-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="7691e-127">Esempio 4: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure con filtro avanzato usando un predicato T-SQL</span><span class="sxs-lookup"><span data-stu-id="7691e-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="7691e-128">Esempio 5: rimuovere l'impostazione di filtro avanzato dai criteri di controllo archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="7691e-129">Esempio 6: abilitare i criteri di controllo Hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="7691e-130">Esempio 7: disabilitare i criteri di controllo Hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="7691e-131">Esempio 8: abilitare i criteri di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7691e-132">Esempio 9: disabilitare i criteri di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="7691e-133">Esempio 10: disabilitare, tramite pipeline, i criteri di controllo di analisi del log di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7691e-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="7691e-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7691e-134">PARAMETERS</span></span>

### <span data-ttu-id="7691e-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7691e-135">-AsJob</span></span>
<span data-ttu-id="7691e-136">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7691e-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7691e-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="7691e-137">-AuditAction</span></span>
<span data-ttu-id="7691e-138">Il set di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="7691e-138">The set of audit actions.</span></span>  
<span data-ttu-id="7691e-139">Le azioni supportate per il controllo sono:</span><span class="sxs-lookup"><span data-stu-id="7691e-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="7691e-140">Selezionare</span><span class="sxs-lookup"><span data-stu-id="7691e-140">SELECT</span></span>  
<span data-ttu-id="7691e-141">AGGIORNAMENTO</span><span class="sxs-lookup"><span data-stu-id="7691e-141">UPDATE</span></span>  
<span data-ttu-id="7691e-142">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="7691e-142">INSERT</span></span>  
<span data-ttu-id="7691e-143">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="7691e-143">DELETE</span></span>  
<span data-ttu-id="7691e-144">ESEGUIRE</span><span class="sxs-lookup"><span data-stu-id="7691e-144">EXECUTE</span></span>  
<span data-ttu-id="7691e-145">RICEVERE</span><span class="sxs-lookup"><span data-stu-id="7691e-145">RECEIVE</span></span>  
<span data-ttu-id="7691e-146">RIFERIMENTI il modulo generale per la definizione di un'azione da controllare è: [azione] su [oggetto] di [Principal] Nota che [oggetto] nel formato precedente può fare riferimento a un oggetto come una tabella, una vista o una stored procedure oppure un intero database o uno schema.</span><span class="sxs-lookup"><span data-stu-id="7691e-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="7691e-147">Per questi ultimi casi, vengono usati rispettivamente il DATABASE delle maschere:: [dbname] e lo SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="7691e-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="7691e-148">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="7691e-148">For example:</span></span>  
<span data-ttu-id="7691e-149">Selezionare su dbo. MyTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="7691e-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="7691e-150">Selezionare nel DATABASE:: database per pubblico</span><span class="sxs-lookup"><span data-stu-id="7691e-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="7691e-151">Selezionare su SCHEMA:: schema per pubblico</span><span class="sxs-lookup"><span data-stu-id="7691e-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="7691e-152">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="7691e-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="7691e-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="7691e-153">-AuditActionGroup</span></span>
<span data-ttu-id="7691e-154">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="7691e-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="7691e-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7691e-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="7691e-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7691e-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="7691e-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7691e-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="7691e-158">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7691e-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7691e-159">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="7691e-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="7691e-160">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="7691e-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="7691e-161">-BlobStorage</span></span>
<span data-ttu-id="7691e-162">Specifica che la destinazione dei log di controllo è archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="7691e-162">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7691e-163">-DatabaseName</span></span>
<span data-ttu-id="7691e-164">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="7691e-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7691e-165">-DefaultProfile</span></span>
<span data-ttu-id="7691e-166">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7691e-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7691e-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7691e-167">-EventHub</span></span>
<span data-ttu-id="7691e-168">Specifica che la destinazione dei log di controllo è hub eventi</span><span class="sxs-lookup"><span data-stu-id="7691e-168">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="7691e-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="7691e-170">ID risorsa per la regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="7691e-170">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7691e-171">-EventHubName</span></span>
<span data-ttu-id="7691e-172">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7691e-172">The name of the event hub.</span></span> <span data-ttu-id="7691e-173">Se non viene specificato alcuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7691e-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-174">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7691e-174">-InputObject</span></span>
<span data-ttu-id="7691e-175">Oggetto database per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="7691e-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="7691e-176">-LogAnalytics</span></span>
<span data-ttu-id="7691e-177">Specifica che la destinazione dei log di controllo è analisi log</span><span class="sxs-lookup"><span data-stu-id="7691e-177">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7691e-178">-PassThru</span></span>
<span data-ttu-id="7691e-179">Specifica se l'output dei criteri di controllo alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="7691e-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7691e-180">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7691e-180">-PredicateExpression</span></span>
<span data-ttu-id="7691e-181">Predicato T-SQL (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="7691e-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="7691e-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7691e-182">-ResourceGroupName</span></span>
<span data-ttu-id="7691e-183">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7691e-183">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7691e-184">-RetentionInDays</span></span>
<span data-ttu-id="7691e-185">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="7691e-185">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-186">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7691e-186">-ServerName</span></span>
<span data-ttu-id="7691e-187">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7691e-187">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-188">-Stato</span><span class="sxs-lookup"><span data-stu-id="7691e-188">-State</span></span>
<span data-ttu-id="7691e-189">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="7691e-189">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7691e-190">-StorageAccountName</span></span>
<span data-ttu-id="7691e-191">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7691e-191">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7691e-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="7691e-193">ID abbonamento account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7691e-193">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7691e-194">-StorageKeyType</span></span>
<span data-ttu-id="7691e-195">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="7691e-195">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7691e-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="7691e-197">ID area di lavoro (ID risorsa di un'area di lavoro analisi log) per un'area di lavoro analisi log in cui si desidera inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="7691e-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="7691e-198">Esempio:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="7691e-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7691e-199">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7691e-199">-Confirm</span></span>
<span data-ttu-id="7691e-200">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7691e-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7691e-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7691e-201">-WhatIf</span></span>
<span data-ttu-id="7691e-202">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7691e-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7691e-203">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7691e-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7691e-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7691e-204">CommonParameters</span></span>
<span data-ttu-id="7691e-205">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7691e-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7691e-206">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7691e-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7691e-207">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7691e-207">INPUTS</span></span>

### <span data-ttu-id="7691e-208">System. String</span><span class="sxs-lookup"><span data-stu-id="7691e-208">System.String</span></span>

### <span data-ttu-id="7691e-209">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7691e-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="7691e-210">Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="7691e-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="7691e-211">System. String []</span><span class="sxs-lookup"><span data-stu-id="7691e-211">System.String[]</span></span>

### <span data-ttu-id="7691e-212">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7691e-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7691e-213">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7691e-213">System.Guid</span></span>

### <span data-ttu-id="7691e-214">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7691e-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7691e-215">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7691e-215">OUTPUTS</span></span>

### <span data-ttu-id="7691e-216">Microsoft. Azure. Commands. SQL. auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="7691e-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="7691e-217">Note</span><span class="sxs-lookup"><span data-stu-id="7691e-217">NOTES</span></span>

## <span data-ttu-id="7691e-218">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7691e-218">RELATED LINKS</span></span>
