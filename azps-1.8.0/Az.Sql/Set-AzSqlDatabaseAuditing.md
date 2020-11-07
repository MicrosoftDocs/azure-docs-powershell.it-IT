---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 511207be4094dae96f8d138124021ce2f8ed3913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676761"
---
# <span data-ttu-id="7e860-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="7e860-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="7e860-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e860-102">SYNOPSIS</span></span>
<span data-ttu-id="7e860-103">Modifica le impostazioni di controllo per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e860-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="7e860-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e860-104">SYNTAX</span></span>

### <span data-ttu-id="7e860-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e860-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e860-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="7e860-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e860-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="7e860-107">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e860-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="7e860-108">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e860-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7e860-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e860-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7e860-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e860-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7e860-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e860-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="7e860-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e860-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e860-113">DESCRIPTION</span></span>
<span data-ttu-id="7e860-114">Il cmdlet **set-AzSqlDatabaseAuditing** modifica le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7e860-114">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="7e860-115">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="7e860-115">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="7e860-116">La destinazione log di controllo viene determinata specificando uno dei parametri di switch seguenti: BlobStorage, LogAnalytics o EventHub (se non è specificato nessuno, il valore predefinito è BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="7e860-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="7e860-117">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="7e860-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="7e860-118">Quando la destinazione dei log di controllo è archiviazione BLOB, specificare il parametro *StorageAccountName* per determinare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7e860-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7e860-119">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="7e860-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="7e860-120">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive le impostazioni di controllo correnti oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="7e860-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="7e860-121">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="7e860-121">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="7e860-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e860-122">EXAMPLES</span></span>

### <span data-ttu-id="7e860-123">Esempio 1: abilitare i criteri di controllo archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-123">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="7e860-124">Esempio 2: disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-124">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="7e860-125">Esempio 3: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure usando un account di archiviazione da un abbonamento diverso</span><span class="sxs-lookup"><span data-stu-id="7e860-125">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="7e860-126">Esempio 4: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un database SQL di Azure con filtro avanzato usando un predicato T-SQL</span><span class="sxs-lookup"><span data-stu-id="7e860-126">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="7e860-127">Esempio 5: rimuovere l'impostazione di filtro avanzato dai criteri di controllo archiviazione BLOB di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-127">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="7e860-128">Esempio 6: abilitare i criteri di controllo Hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-128">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="7e860-129">Esempio 7: disabilitare i criteri di controllo Hub eventi di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-129">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="7e860-130">Esempio 8: abilitare i criteri di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-130">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="7e860-131">Esempio 9: disabilitare i criteri di controllo del log Analytics di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-131">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="7e860-132">Esempio 10: disabilitare, tramite pipeline, i criteri di controllo di analisi del log di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7e860-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="7e860-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e860-133">PARAMETERS</span></span>

### <span data-ttu-id="7e860-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e860-134">-AsJob</span></span>
<span data-ttu-id="7e860-135">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7e860-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e860-136">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="7e860-136">-AuditAction</span></span>
<span data-ttu-id="7e860-137">Il set di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="7e860-137">The set of audit actions.</span></span>  
<span data-ttu-id="7e860-138">Le azioni supportate per il controllo sono:</span><span class="sxs-lookup"><span data-stu-id="7e860-138">The supported actions to audit are:</span></span>  
<span data-ttu-id="7e860-139">Selezionare</span><span class="sxs-lookup"><span data-stu-id="7e860-139">SELECT</span></span>  
<span data-ttu-id="7e860-140">AGGIORNAMENTO</span><span class="sxs-lookup"><span data-stu-id="7e860-140">UPDATE</span></span>  
<span data-ttu-id="7e860-141">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="7e860-141">INSERT</span></span>  
<span data-ttu-id="7e860-142">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="7e860-142">DELETE</span></span>  
<span data-ttu-id="7e860-143">ESEGUIRE</span><span class="sxs-lookup"><span data-stu-id="7e860-143">EXECUTE</span></span>  
<span data-ttu-id="7e860-144">RICEVERE</span><span class="sxs-lookup"><span data-stu-id="7e860-144">RECEIVE</span></span>  
<span data-ttu-id="7e860-145">RIFERIMENTI il modulo generale per la definizione di un'azione da controllare è: [azione] su [oggetto] di [Principal] Nota che [oggetto] nel formato precedente può fare riferimento a un oggetto come una tabella, una vista o una stored procedure oppure un intero database o uno schema.</span><span class="sxs-lookup"><span data-stu-id="7e860-145">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="7e860-146">Per questi ultimi casi, vengono usati rispettivamente il DATABASE delle maschere:: [dbname] e lo SCHEMA:: [SchemaName].</span><span class="sxs-lookup"><span data-stu-id="7e860-146">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="7e860-147">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="7e860-147">For example:</span></span>  
<span data-ttu-id="7e860-148">Selezionare su dbo. MyTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="7e860-148">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="7e860-149">Selezionare nel DATABASE:: database per pubblico</span><span class="sxs-lookup"><span data-stu-id="7e860-149">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="7e860-150">Selezionare su SCHEMA:: schema per pubblico</span><span class="sxs-lookup"><span data-stu-id="7e860-150">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="7e860-151">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="7e860-151">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="7e860-152">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="7e860-152">-AuditActionGroup</span></span>
<span data-ttu-id="7e860-153">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="7e860-153">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="7e860-154">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7e860-154">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="7e860-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7e860-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="7e860-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7e860-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="7e860-157">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7e860-157">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7e860-158">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="7e860-158">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="7e860-159">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="7e860-159">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="7e860-160">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="7e860-160">-BlobStorage</span></span>
<span data-ttu-id="7e860-161">Specifica che la destinazione dei log di controllo è archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="7e860-161">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="7e860-162">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e860-162">-DatabaseName</span></span>
<span data-ttu-id="7e860-163">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="7e860-163">SQL Database name.</span></span>

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

### <span data-ttu-id="7e860-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e860-164">-DefaultProfile</span></span>
<span data-ttu-id="7e860-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e860-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e860-166">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7e860-166">-EventHub</span></span>
<span data-ttu-id="7e860-167">Specifica che la destinazione dei log di controllo è hub eventi</span><span class="sxs-lookup"><span data-stu-id="7e860-167">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="7e860-168">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="7e860-168">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="7e860-169">ID risorsa per la regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="7e860-169">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="7e860-170">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7e860-170">-EventHubName</span></span>
<span data-ttu-id="7e860-171">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7e860-171">The name of the event hub.</span></span> <span data-ttu-id="7e860-172">Se non viene specificato alcuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e860-172">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="7e860-173">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e860-173">-InputObject</span></span>
<span data-ttu-id="7e860-174">Oggetto database per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="7e860-174">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="7e860-175">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e860-175">-LogAnalytics</span></span>
<span data-ttu-id="7e860-176">Specifica che la destinazione dei log di controllo è analisi log</span><span class="sxs-lookup"><span data-stu-id="7e860-176">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="7e860-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e860-177">-PassThru</span></span>
<span data-ttu-id="7e860-178">Specifica se l'output dei criteri di controllo alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e860-178">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7e860-179">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7e860-179">-PredicateExpression</span></span>
<span data-ttu-id="7e860-180">Predicato T-SQL (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="7e860-180">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="7e860-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e860-181">-ResourceGroupName</span></span>
<span data-ttu-id="7e860-182">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e860-182">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e860-183">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7e860-183">-RetentionInDays</span></span>
<span data-ttu-id="7e860-184">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="7e860-184">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="7e860-185">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7e860-185">-ServerName</span></span>
<span data-ttu-id="7e860-186">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7e860-186">SQL server name.</span></span>

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

### <span data-ttu-id="7e860-187">-Stato</span><span class="sxs-lookup"><span data-stu-id="7e860-187">-State</span></span>
<span data-ttu-id="7e860-188">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="7e860-188">The state of the policy.</span></span>

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

### <span data-ttu-id="7e860-189">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e860-189">-StorageAccountName</span></span>
<span data-ttu-id="7e860-190">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7e860-190">The name of the storage account.</span></span>

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

### <span data-ttu-id="7e860-191">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e860-191">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="7e860-192">ID abbonamento account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7e860-192">The storage account subscription id</span></span>

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

### <span data-ttu-id="7e860-193">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7e860-193">-StorageKeyType</span></span>
<span data-ttu-id="7e860-194">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="7e860-194">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="7e860-195">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7e860-195">-WorkspaceResourceId</span></span>
<span data-ttu-id="7e860-196">ID area di lavoro (ID risorsa di un'area di lavoro analisi log) per un'area di lavoro analisi log in cui si desidera inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="7e860-196">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="7e860-197">Esempio:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="7e860-197">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="7e860-198">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e860-198">-Confirm</span></span>
<span data-ttu-id="7e860-199">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e860-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e860-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e860-200">-WhatIf</span></span>
<span data-ttu-id="7e860-201">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e860-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e860-202">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e860-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e860-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e860-203">CommonParameters</span></span>
<span data-ttu-id="7e860-204">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e860-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e860-205">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e860-205">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e860-206">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e860-206">INPUTS</span></span>

### <span data-ttu-id="7e860-207">System. String</span><span class="sxs-lookup"><span data-stu-id="7e860-207">System.String</span></span>

### <span data-ttu-id="7e860-208">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7e860-208">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="7e860-209">Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="7e860-209">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="7e860-210">System. String []</span><span class="sxs-lookup"><span data-stu-id="7e860-210">System.String[]</span></span>

### <span data-ttu-id="7e860-211">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e860-211">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7e860-212">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7e860-212">System.Guid</span></span>

### <span data-ttu-id="7e860-213">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7e860-213">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7e860-214">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e860-214">OUTPUTS</span></span>

### <span data-ttu-id="7e860-215">Microsoft. Azure. Commands. SQL. auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="7e860-215">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="7e860-216">Note</span><span class="sxs-lookup"><span data-stu-id="7e860-216">NOTES</span></span>

## <span data-ttu-id="7e860-217">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e860-217">RELATED LINKS</span></span>
