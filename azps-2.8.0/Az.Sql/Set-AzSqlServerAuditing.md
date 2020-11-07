---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857213"
---
# <span data-ttu-id="11b3d-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="11b3d-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="11b3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="11b3d-103">**Importante: questo cmdlet è deprecato, [set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) la sostituisce.**</span><span class="sxs-lookup"><span data-stu-id="11b3d-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="11b3d-104">Modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="11b3d-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="11b3d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11b3d-105">SYNTAX</span></span>

### <span data-ttu-id="11b3d-106">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11b3d-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b3d-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11b3d-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b3d-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b3d-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b3d-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11b3d-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b3d-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="11b3d-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b3d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11b3d-114">DESCRIPTION</span></span>
<span data-ttu-id="11b3d-115">Il cmdlet **set-AzSqlServerAuditing** modifica le impostazioni di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="11b3d-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="11b3d-116">Per usare il cmdlet, usare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="11b3d-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="11b3d-117">La destinazione log di controllo viene determinata specificando uno dei parametri di switch seguenti: BlobStorage, LogAnalytics o EventHub (se non è specificato nessuno, il valore predefinito è BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="11b3d-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="11b3d-118">Usa il parametro *state* per abilitare o disabilitare il criterio.</span><span class="sxs-lookup"><span data-stu-id="11b3d-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="11b3d-119">Quando la destinazione dei log di controllo è archiviazione BLOB, specificare il parametro *StorageAccountName* per determinare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="11b3d-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="11b3d-120">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="11b3d-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="11b3d-121">Se il cmdlet riesce e si usa il parametro *PassThru* , viene restituito un oggetto che descrive le impostazioni di controllo correnti oltre agli identificatori del server.</span><span class="sxs-lookup"><span data-stu-id="11b3d-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="11b3d-122">Gli identificatori del server includono, ma non sono limitati a, **ResourceGroupName** e **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="11b3d-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="11b3d-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11b3d-123">EXAMPLES</span></span>

### <span data-ttu-id="11b3d-124">Esempio 1: abilitare i criteri di controllo archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="11b3d-125">Esempio 2: disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="11b3d-126">Esempio 3: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un server SQL di Azure usando un account di archiviazione da un abbonamento diverso</span><span class="sxs-lookup"><span data-stu-id="11b3d-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="11b3d-127">Esempio 4: abilitare i criteri di controllo dello spazio di archiviazione BLOB di un server SQL di Azure con il filtro avanzato usando un predicato T-SQL</span><span class="sxs-lookup"><span data-stu-id="11b3d-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="11b3d-128">Esempio 5: rimuovere l'impostazione di filtro avanzato dal criterio di archiviazione BLOB audit di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="11b3d-129">Esempio 6: abilitare i criteri di controllo Hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="11b3d-130">Esempio 7: disabilitare i criteri di controllo Hub eventi di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="11b3d-131">Esempio 8: abilitare i criteri di controllo del log Analytics di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="11b3d-132">Esempio 9: disabilitare i criteri di controllo del log Analytics di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="11b3d-133">Esempio 10: disabilitare, tramite pipeline, i criteri di controllo di analisi del log di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="11b3d-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="11b3d-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11b3d-134">PARAMETERS</span></span>

### <span data-ttu-id="11b3d-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11b3d-135">-AsJob</span></span>
<span data-ttu-id="11b3d-136">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="11b3d-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11b3d-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="11b3d-137">-AuditActionGroup</span></span>
<span data-ttu-id="11b3d-138">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="11b3d-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="11b3d-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="11b3d-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="11b3d-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="11b3d-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="11b3d-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="11b3d-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="11b3d-142">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="11b3d-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="11b3d-143">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="11b3d-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="11b3d-144">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="11b3d-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="11b3d-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="11b3d-145">-BlobStorage</span></span>
<span data-ttu-id="11b3d-146">Specifica che la destinazione dei log di controllo è archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="11b3d-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="11b3d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b3d-147">-DefaultProfile</span></span>
<span data-ttu-id="11b3d-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11b3d-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b3d-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="11b3d-149">-EventHub</span></span>
<span data-ttu-id="11b3d-150">Specifica che la destinazione dei log di controllo è hub eventi</span><span class="sxs-lookup"><span data-stu-id="11b3d-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="11b3d-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="11b3d-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="11b3d-152">ID risorsa per la regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="11b3d-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="11b3d-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="11b3d-153">-EventHubName</span></span>
<span data-ttu-id="11b3d-154">Nome dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="11b3d-154">The name of the event hub.</span></span> <span data-ttu-id="11b3d-155">Se non viene specificato alcuno quando si fornisce EventHubAuthorizationRuleResourceId, verrà selezionato l'hub eventi predefinito.</span><span class="sxs-lookup"><span data-stu-id="11b3d-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="11b3d-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11b3d-156">-InputObject</span></span>
<span data-ttu-id="11b3d-157">L'oggetto server per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="11b3d-157">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11b3d-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="11b3d-158">-LogAnalytics</span></span>
<span data-ttu-id="11b3d-159">Specifica che la destinazione dei log di controllo è analisi log</span><span class="sxs-lookup"><span data-stu-id="11b3d-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="11b3d-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11b3d-160">-PassThru</span></span>
<span data-ttu-id="11b3d-161">Specifica se l'output dei criteri di controllo alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="11b3d-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="11b3d-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="11b3d-162">-PredicateExpression</span></span>
<span data-ttu-id="11b3d-163">Predicato T-SQL (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="11b3d-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="11b3d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b3d-164">-ResourceGroupName</span></span>
<span data-ttu-id="11b3d-165">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11b3d-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="11b3d-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="11b3d-166">-RetentionInDays</span></span>
<span data-ttu-id="11b3d-167">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="11b3d-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="11b3d-168">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="11b3d-168">-ServerName</span></span>
<span data-ttu-id="11b3d-169">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="11b3d-169">SQL server name.</span></span>

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

### <span data-ttu-id="11b3d-170">-Stato</span><span class="sxs-lookup"><span data-stu-id="11b3d-170">-State</span></span>
<span data-ttu-id="11b3d-171">Stato del criterio.</span><span class="sxs-lookup"><span data-stu-id="11b3d-171">The state of the policy.</span></span>

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

### <span data-ttu-id="11b3d-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="11b3d-172">-StorageAccountName</span></span>
<span data-ttu-id="11b3d-173">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="11b3d-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="11b3d-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11b3d-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="11b3d-175">ID abbonamento account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="11b3d-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="11b3d-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="11b3d-176">-StorageKeyType</span></span>
<span data-ttu-id="11b3d-177">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="11b3d-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="11b3d-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="11b3d-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="11b3d-179">ID area di lavoro (ID risorsa di un'area di lavoro analisi log) per un'area di lavoro analisi log in cui si desidera inviare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="11b3d-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="11b3d-180">Esempio:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="11b3d-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="11b3d-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11b3d-181">-Confirm</span></span>
<span data-ttu-id="11b3d-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b3d-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b3d-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b3d-183">-WhatIf</span></span>
<span data-ttu-id="11b3d-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b3d-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11b3d-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b3d-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b3d-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b3d-186">CommonParameters</span></span>
<span data-ttu-id="11b3d-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b3d-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b3d-188">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11b3d-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b3d-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11b3d-189">INPUTS</span></span>

### <span data-ttu-id="11b3d-190">System. String</span><span class="sxs-lookup"><span data-stu-id="11b3d-190">System.String</span></span>

### <span data-ttu-id="11b3d-191">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="11b3d-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="11b3d-192">Microsoft. Azure. Commands. SQL. auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="11b3d-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="11b3d-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="11b3d-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="11b3d-194">System. Guid</span><span class="sxs-lookup"><span data-stu-id="11b3d-194">System.Guid</span></span>

### <span data-ttu-id="11b3d-195">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11b3d-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="11b3d-196">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11b3d-196">OUTPUTS</span></span>

### <span data-ttu-id="11b3d-197">Microsoft. Azure. Commands. SQL. auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="11b3d-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="11b3d-198">Note</span><span class="sxs-lookup"><span data-stu-id="11b3d-198">NOTES</span></span>

## <span data-ttu-id="11b3d-199">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11b3d-199">RELATED LINKS</span></span>
