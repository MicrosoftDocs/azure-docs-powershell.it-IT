---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8b0312ddcdce5c538b80f0245470496c534bf07f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993227"
---
# <span data-ttu-id="8e43a-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="8e43a-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="8e43a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e43a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e43a-103">Modifica le impostazioni di controllo di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8e43a-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="8e43a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e43a-104">SYNTAX</span></span>

### <span data-ttu-id="8e43a-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e43a-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e43a-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e43a-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e43a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e43a-107">DESCRIPTION</span></span>
<span data-ttu-id="8e43a-108">Il cmdlet **Set-AzSqlServerAudit** cambia le impostazioni di controllo di un server SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8e43a-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="8e43a-109">Per usare il cmdlet, usare i *parametri ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="8e43a-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="8e43a-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i log di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8e43a-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="8e43a-111">È anche possibile definire la conservazione per i log di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="8e43a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e43a-112">EXAMPLES</span></span>

### <span data-ttu-id="8e43a-113">Esempio 1: Abilitare i criteri di controllo di archiviazione BLOB di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="8e43a-114">Esempio 2: Disabilitare i criteri di controllo di archiviazione BLOB di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="8e43a-115">Esempio 3: Abilitare i criteri di controllo di archiviazione BLOB di un server di SQL Azure con filtri avanzati usando un predicato di SQL T</span><span class="sxs-lookup"><span data-stu-id="8e43a-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="8e43a-116">Esempio 4: Rimuovere l'impostazione di filtro avanzato dai criteri di controllo di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="8e43a-117">Esempio 5: Abilitare i criteri di controllo dell'hub eventi di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="8e43a-118">Esempio 6: Disabilitare i criteri di controllo dell'hub eventi di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="8e43a-119">Esempio 7: Abilitare i criteri di controllo di analisi dei log di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="8e43a-120">Esempio 8: Disabilitare i criteri di controllo di analisi dei log di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="8e43a-121">Esempio 9: Disabilitare, tramite pipeline, i criteri di controllo di analisi del log di un server SQL Azure</span><span class="sxs-lookup"><span data-stu-id="8e43a-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="8e43a-122">Esempio 10: Disabilitare l'invio dei record di controllo di un server SQL Azure all'archiviazione BLOB e abilitarli all'analisi del log.</span><span class="sxs-lookup"><span data-stu-id="8e43a-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="8e43a-123">Esempio 11: Abilitare l'invio dei record di controllo di un server SQL Azure all'archiviazione BLOB, all'hub eventi e all'analisi del log.</span><span class="sxs-lookup"><span data-stu-id="8e43a-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="8e43a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e43a-124">PARAMETERS</span></span>

### <span data-ttu-id="8e43a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e43a-125">-AsJob</span></span>
<span data-ttu-id="8e43a-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8e43a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e43a-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8e43a-127">-AuditActionGroup</span></span>
<span data-ttu-id="8e43a-128">La combinazione consigliata di gruppi di azioni da usare è la seguente: in questo modo verranno controllati tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti:</span><span class="sxs-lookup"><span data-stu-id="8e43a-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="8e43a-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8e43a-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="8e43a-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8e43a-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="8e43a-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="8e43a-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="8e43a-132">Anche questa combinazione è configurata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8e43a-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="8e43a-133">Questi gruppi coprono tutte SQL istruzione e le stored procedure eseguite sul database e non devono essere usati insieme ad altri gruppi perché ciò genererà log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="8e43a-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="8e43a-134">Per altre informazioni, vedere https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="8e43a-134">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="8e43a-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="8e43a-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="8e43a-136">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="8e43a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e43a-137">-DefaultProfile</span></span>
<span data-ttu-id="8e43a-138">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e43a-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e43a-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="8e43a-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="8e43a-140">ID risorsa per la regola di autorizzazione dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="8e43a-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="8e43a-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8e43a-141">-EventHubName</span></span>
<span data-ttu-id="8e43a-142">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="8e43a-142">The name of the event hub.</span></span> <span data-ttu-id="8e43a-143">Se non ne viene specificato nessuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="8e43a-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="8e43a-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="8e43a-144">-EventHubTargetState</span></span>
<span data-ttu-id="8e43a-145">Indica se l'hub eventi è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="8e43a-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="8e43a-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="8e43a-147">Indica se l'analisi del log è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="8e43a-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e43a-148">-PassThru</span></span>
<span data-ttu-id="8e43a-149">Specifica se l'output del criterio di controllo deve essere generato al termine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e43a-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8e43a-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="8e43a-150">-PredicateExpression</span></span>
<span data-ttu-id="8e43a-151">Predicato di SQL T (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="8e43a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e43a-152">-ResourceGroupName</span></span>
<span data-ttu-id="8e43a-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e43a-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e43a-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8e43a-154">-RetentionInDays</span></span>
<span data-ttu-id="8e43a-155">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="8e43a-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e43a-156">-ServerName</span></span>
<span data-ttu-id="8e43a-157">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="8e43a-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e43a-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="8e43a-158">-ServerObject</span></span>
<span data-ttu-id="8e43a-159">Oggetto server per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e43a-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8e43a-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="8e43a-161">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8e43a-161">The storage account resource id</span></span>

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

### <span data-ttu-id="8e43a-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8e43a-162">-StorageKeyType</span></span>
<span data-ttu-id="8e43a-163">Specifica quale delle chiavi di accesso di archiviazione usare.</span><span class="sxs-lookup"><span data-stu-id="8e43a-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="8e43a-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8e43a-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="8e43a-165">ID area di lavoro (ID risorsa di un'area di lavoro Analisi log) per un'area di lavoro Analisi log a cui inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="8e43a-166">Esempio: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/virntassia2</span><span class="sxs-lookup"><span data-stu-id="8e43a-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="8e43a-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e43a-167">-Confirm</span></span>
<span data-ttu-id="8e43a-168">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e43a-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e43a-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e43a-169">-WhatIf</span></span>
<span data-ttu-id="8e43a-170">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e43a-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e43a-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e43a-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e43a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e43a-172">CommonParameters</span></span>
<span data-ttu-id="8e43a-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e43a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e43a-174">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e43a-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e43a-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e43a-175">INPUTS</span></span>

### <span data-ttu-id="8e43a-176">System.String</span><span class="sxs-lookup"><span data-stu-id="8e43a-176">System.String</span></span>

### <span data-ttu-id="8e43a-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="8e43a-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="8e43a-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="8e43a-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="8e43a-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8e43a-179">System.Guid</span></span>

### <span data-ttu-id="8e43a-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8e43a-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8e43a-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="8e43a-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="8e43a-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e43a-182">OUTPUTS</span></span>

### <span data-ttu-id="8e43a-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e43a-183">System.Boolean</span></span>

## <span data-ttu-id="8e43a-184">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e43a-184">NOTES</span></span>

## <span data-ttu-id="8e43a-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e43a-185">RELATED LINKS</span></span>
