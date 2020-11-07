---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 5ba80e2b8c2ca315f9b51b9873688f0b80f1e85f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864963"
---
# <span data-ttu-id="43aea-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="43aea-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="43aea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43aea-102">SYNOPSIS</span></span>
<span data-ttu-id="43aea-103">Modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="43aea-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="43aea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43aea-104">SYNTAX</span></span>

### <span data-ttu-id="43aea-105">ServerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43aea-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43aea-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43aea-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43aea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43aea-107">DESCRIPTION</span></span>
<span data-ttu-id="43aea-108">Il cmdlet **set-AzSqlServerAudit** modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="43aea-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="43aea-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="43aea-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="43aea-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="43aea-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="43aea-111">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="43aea-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43aea-112">EXAMPLES</span></span>

### <span data-ttu-id="43aea-113">Esempio 1: abilitare i criteri di controllo archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="43aea-114">Esempio 2: disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="43aea-115">Esempio 3,1: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un server SQL di Azure con il filtro avanzato usando un predicato T-SQL</span><span class="sxs-lookup"><span data-stu-id="43aea-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="43aea-116">Esempio 3,2: rimuovere l'impostazione di filtro avanzato dai criteri di controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="43aea-117">Esempio 4: abilitare i criteri di controllo Hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-117">Example 4: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="43aea-118">Esempio 5: disabilitare i criteri di controllo Hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-118">Example 5: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="43aea-119">Esempio 6: abilitare i criteri di controllo del log Analytics di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-119">Example 6: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="43aea-120">Esempio 7: disabilitare i criteri di controllo del log Analytics di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-120">Example 7: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="43aea-121">Esempio 8: disabilitare, tramite pipeline, i criteri di controllo di analisi del log di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="43aea-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="43aea-122">Esempio 9: disabilitare l'invio di record di controllo di un server SQL di Azure a archiviazione BLOB e consentire l'invio di un log di analisi.</span><span class="sxs-lookup"><span data-stu-id="43aea-122">Example 9: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="43aea-123">Esempio 10: consentire l'invio di record di controllo di un server SQL di Azure a archiviazione BLOB, Hub eventi e analisi log.</span><span class="sxs-lookup"><span data-stu-id="43aea-123">Example 10: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="43aea-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43aea-124">PARAMETERS</span></span>

### <span data-ttu-id="43aea-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43aea-125">-AsJob</span></span>
<span data-ttu-id="43aea-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="43aea-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43aea-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="43aea-127">-AuditActionGroup</span></span>
<span data-ttu-id="43aea-128">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="43aea-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="43aea-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="43aea-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="43aea-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="43aea-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="43aea-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="43aea-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="43aea-132">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="43aea-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="43aea-133">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="43aea-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="43aea-134">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="43aea-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="43aea-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="43aea-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="43aea-136">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="43aea-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43aea-137">-DefaultProfile</span></span>
<span data-ttu-id="43aea-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43aea-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43aea-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="43aea-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="43aea-140">ID risorsa per la regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="43aea-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="43aea-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="43aea-141">-EventHubName</span></span>
<span data-ttu-id="43aea-142">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="43aea-142">The name of the event hub.</span></span> <span data-ttu-id="43aea-143">Se non viene specificato alcuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="43aea-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="43aea-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="43aea-144">-EventHubTargetState</span></span>
<span data-ttu-id="43aea-145">Indica se l'hub eventi è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="43aea-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="43aea-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="43aea-147">Indica se analisi log è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="43aea-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43aea-148">-PassThru</span></span>
<span data-ttu-id="43aea-149">Specifica se l'output dei criteri di controllo alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="43aea-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="43aea-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="43aea-150">-PredicateExpression</span></span>
<span data-ttu-id="43aea-151">Predicato T-SQL (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="43aea-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43aea-152">-ResourceGroupName</span></span>
<span data-ttu-id="43aea-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43aea-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="43aea-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="43aea-154">-RetentionInDays</span></span>
<span data-ttu-id="43aea-155">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="43aea-156">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="43aea-156">-ServerName</span></span>
<span data-ttu-id="43aea-157">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="43aea-157">SQL server name.</span></span>

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

### <span data-ttu-id="43aea-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="43aea-158">-ServerObject</span></span>
<span data-ttu-id="43aea-159">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-159">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="43aea-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="43aea-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="43aea-161">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="43aea-161">The storage account resource id</span></span>

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

### <span data-ttu-id="43aea-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="43aea-162">-StorageKeyType</span></span>
<span data-ttu-id="43aea-163">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="43aea-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="43aea-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="43aea-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="43aea-165">ID area di lavoro (ID risorsa di un'area di lavoro analisi log) per un'area di lavoro analisi log in cui si desidera inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="43aea-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="43aea-166">Esempio:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="43aea-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="43aea-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43aea-167">-Confirm</span></span>
<span data-ttu-id="43aea-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43aea-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43aea-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43aea-169">-WhatIf</span></span>
<span data-ttu-id="43aea-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43aea-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43aea-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43aea-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43aea-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43aea-172">CommonParameters</span></span>
<span data-ttu-id="43aea-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43aea-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43aea-174">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43aea-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43aea-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43aea-175">INPUTS</span></span>

### <span data-ttu-id="43aea-176">System. String</span><span class="sxs-lookup"><span data-stu-id="43aea-176">System.String</span></span>

### <span data-ttu-id="43aea-177">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="43aea-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="43aea-178">Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="43aea-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="43aea-179">System. Guid</span><span class="sxs-lookup"><span data-stu-id="43aea-179">System.Guid</span></span>

### <span data-ttu-id="43aea-180">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43aea-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="43aea-181">Microsoft. Azure. Commands. SQL. auditing. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="43aea-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="43aea-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43aea-182">OUTPUTS</span></span>

### <span data-ttu-id="43aea-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43aea-183">System.Boolean</span></span>

## <span data-ttu-id="43aea-184">Note</span><span class="sxs-lookup"><span data-stu-id="43aea-184">NOTES</span></span>

## <span data-ttu-id="43aea-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43aea-185">RELATED LINKS</span></span>
