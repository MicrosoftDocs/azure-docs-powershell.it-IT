---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 6e3c5c935f6703f5c4f29b2a4ae793fc48e9b16f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995006"
---
# <span data-ttu-id="de95d-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="de95d-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="de95d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de95d-102">SYNOPSIS</span></span>
<span data-ttu-id="de95d-103">Modifica le impostazioni di controllo per un database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="de95d-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="de95d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de95d-104">SYNTAX</span></span>

### <span data-ttu-id="de95d-105">DatabaseParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de95d-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de95d-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de95d-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de95d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de95d-107">DESCRIPTION</span></span>
<span data-ttu-id="de95d-108">Il cmdlet **Set-AzSqlDatabaseAudit** modifica le impostazioni di controllo di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="de95d-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="de95d-109">Per usare il cmdlet, usare i *parametri ResourceGroupName,* *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="de95d-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="de95d-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i log di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de95d-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="de95d-111">È anche possibile definire la conservazione per i log di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="de95d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de95d-112">EXAMPLES</span></span>

### <span data-ttu-id="de95d-113">Esempio 1: Abilitare i criteri di controllo di archiviazione BLOB di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="de95d-114">Esempio 2: Disabilitare i criteri di controllo di archiviazione BLOB di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="de95d-115">Esempio 3: Abilitare i criteri di controllo di archiviazione BLOB di un database di SQL azure con i filtri usando un predicato di SQL BLOB</span><span class="sxs-lookup"><span data-stu-id="de95d-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="de95d-116">Esempio 4: Rimuovere il filtro dai criteri di controllo di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="de95d-117">Esempio 5: Abilitare i criteri di controllo dell'hub eventi di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="de95d-118">Esempio 6: Disabilitare i criteri di controllo dell'hub eventi di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="de95d-119">Esempio 7: Abilitare i criteri di controllo di analisi dei log di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="de95d-120">Esempio 8: Disabilitare i criteri di controllo di analisi dei log di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="de95d-121">Esempio 9: Disabilitare, tramite pipeline, i criteri di controllo di analisi dei log di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="de95d-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="de95d-122">Esempio 10: Disabilitare l'invio dei record di controllo di un database di azure SQL all'archiviazione BLOB e abilitarli all'analisi del log.</span><span class="sxs-lookup"><span data-stu-id="de95d-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="de95d-123">Esempio 11: Abilitare l'invio dei record di controllo di un database SQL Azure all'archiviazione BLOB, all'hub eventi e all'analisi del log.</span><span class="sxs-lookup"><span data-stu-id="de95d-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="de95d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de95d-124">PARAMETERS</span></span>

### <span data-ttu-id="de95d-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="de95d-125">-AuditAction</span></span>
<span data-ttu-id="de95d-126">Insieme di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-126">The set of audit actions.</span></span>  
<span data-ttu-id="de95d-127">Le azioni supportate da controllare sono:</span><span class="sxs-lookup"><span data-stu-id="de95d-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="de95d-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="de95d-128">SELECT</span></span>  
<span data-ttu-id="de95d-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="de95d-129">UPDATE</span></span>  
<span data-ttu-id="de95d-130">INS</span><span class="sxs-lookup"><span data-stu-id="de95d-130">INSERT</span></span>  
<span data-ttu-id="de95d-131">CANC</span><span class="sxs-lookup"><span data-stu-id="de95d-131">DELETE</span></span>  
<span data-ttu-id="de95d-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="de95d-132">EXECUTE</span></span>  
<span data-ttu-id="de95d-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="de95d-133">RECEIVE</span></span>  
<span data-ttu-id="de95d-134">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="de95d-134">REFERENCES</span></span>  
<span data-ttu-id="de95d-135">La maschera generale per definire un'azione da controllare è: [azione] ON [oggetto] BY [entità] Si noti che [oggetto] nel formato precedente può fare riferimento a un oggetto come una tabella, una visualizzazione o una stored procedure oppure a un intero database o schema.</span><span class="sxs-lookup"><span data-stu-id="de95d-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="de95d-136">Per gli ultimi casi, vengono usate, rispettivamente, le maschere DATABASE::[nome db] e SCHEMA::[nome schema].</span><span class="sxs-lookup"><span data-stu-id="de95d-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="de95d-137">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="de95d-137">For example:</span></span>  
<span data-ttu-id="de95d-138">SELECT su dbo.myTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="de95d-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="de95d-139">SELECT su DATABASE::myDatabase per pubblico</span><span class="sxs-lookup"><span data-stu-id="de95d-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="de95d-140">SELECT su SCHEMA::mySchema per pubblico</span><span class="sxs-lookup"><span data-stu-id="de95d-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="de95d-141">Per altre informazioni, vedere https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="de95d-141">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="de95d-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="de95d-142">-AuditActionGroup</span></span>
<span data-ttu-id="de95d-143">La combinazione consigliata di gruppi di azioni da usare è la seguente: in questo modo verranno controllati tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti:</span><span class="sxs-lookup"><span data-stu-id="de95d-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="de95d-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="de95d-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="de95d-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="de95d-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="de95d-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="de95d-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="de95d-147">Anche questa combinazione è configurata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="de95d-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="de95d-148">Questi gruppi coprono tutte SQL istruzione e le stored procedure eseguite sul database e non devono essere usati insieme ad altri gruppi perché ciò genererà log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="de95d-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="de95d-149">Per altre informazioni, vedere https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="de95d-149">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="de95d-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="de95d-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="de95d-151">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="de95d-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de95d-152">-DatabaseName</span></span>
<span data-ttu-id="de95d-153">SQL nome del database.</span><span class="sxs-lookup"><span data-stu-id="de95d-153">SQL Database name.</span></span>

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

### <span data-ttu-id="de95d-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="de95d-154">-DatabaseObject</span></span>
<span data-ttu-id="de95d-155">Oggetto di database per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="de95d-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de95d-156">-DefaultProfile</span></span>
<span data-ttu-id="de95d-157">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de95d-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de95d-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="de95d-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="de95d-159">ID risorsa per la regola di autorizzazione dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="de95d-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="de95d-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="de95d-160">-EventHubName</span></span>
<span data-ttu-id="de95d-161">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="de95d-161">The name of the event hub.</span></span> <span data-ttu-id="de95d-162">Se non ne viene specificato nessuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="de95d-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="de95d-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="de95d-163">-EventHubTargetState</span></span>
<span data-ttu-id="de95d-164">Indica se l'hub eventi è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="de95d-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="de95d-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="de95d-166">Indica se l'analisi del log è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="de95d-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de95d-167">-PassThru</span></span>
<span data-ttu-id="de95d-168">Specifica se l'output del criterio di controllo deve essere generato al termine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="de95d-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="de95d-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="de95d-169">-PredicateExpression</span></span>
<span data-ttu-id="de95d-170">Predicato di SQL T (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="de95d-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de95d-171">-ResourceGroupName</span></span>
<span data-ttu-id="de95d-172">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de95d-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="de95d-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="de95d-173">-RetentionInDays</span></span>
<span data-ttu-id="de95d-174">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="de95d-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de95d-175">-ServerName</span></span>
<span data-ttu-id="de95d-176">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="de95d-176">SQL server name.</span></span>

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

### <span data-ttu-id="de95d-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="de95d-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="de95d-178">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="de95d-178">The storage account resource id</span></span>

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

### <span data-ttu-id="de95d-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="de95d-179">-StorageKeyType</span></span>
<span data-ttu-id="de95d-180">Specifica quale delle chiavi di accesso di archiviazione usare.</span><span class="sxs-lookup"><span data-stu-id="de95d-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="de95d-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="de95d-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="de95d-182">ID area di lavoro (ID risorsa di un'area di lavoro Analisi log) per un'area di lavoro Analisi log a cui inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="de95d-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="de95d-183">Esempio: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/rba2</span><span class="sxs-lookup"><span data-stu-id="de95d-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="de95d-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de95d-184">-Confirm</span></span>
<span data-ttu-id="de95d-185">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de95d-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de95d-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de95d-186">-WhatIf</span></span>
<span data-ttu-id="de95d-187">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de95d-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de95d-188">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de95d-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de95d-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de95d-189">CommonParameters</span></span>
<span data-ttu-id="de95d-190">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de95d-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de95d-191">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de95d-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de95d-192">INPUT</span><span class="sxs-lookup"><span data-stu-id="de95d-192">INPUTS</span></span>

### <span data-ttu-id="de95d-193">System.String</span><span class="sxs-lookup"><span data-stu-id="de95d-193">System.String</span></span>

### <span data-ttu-id="de95d-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="de95d-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="de95d-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="de95d-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="de95d-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="de95d-196">System.String[]</span></span>

### <span data-ttu-id="de95d-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="de95d-197">System.Guid</span></span>

### <span data-ttu-id="de95d-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="de95d-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="de95d-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="de95d-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="de95d-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de95d-200">OUTPUTS</span></span>

### <span data-ttu-id="de95d-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de95d-201">System.Boolean</span></span>

## <span data-ttu-id="de95d-202">NOTE</span><span class="sxs-lookup"><span data-stu-id="de95d-202">NOTES</span></span>

## <span data-ttu-id="de95d-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de95d-203">RELATED LINKS</span></span>
