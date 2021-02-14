---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188750"
---
# <span data-ttu-id="a1b78-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a1b78-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="a1b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b78-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b78-103">Modifica le impostazioni di controllo di un'area di lavoro di analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a1b78-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a1b78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1b78-104">SYNTAX</span></span>

### <span data-ttu-id="a1b78-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1b78-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b78-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b78-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1b78-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1b78-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1b78-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1b78-108">DESCRIPTION</span></span>
<span data-ttu-id="a1b78-109">Il cmdlet **Set-AzSynapseSqlAuditSetting** modifica le impostazioni di controllo di un'area di lavoro di analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a1b78-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="a1b78-110">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i log di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1b78-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="a1b78-111">È anche possibile definire la conservazione per i log di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a1b78-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="a1b78-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1b78-112">EXAMPLES</span></span>

### <span data-ttu-id="a1b78-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1b78-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="a1b78-114">Abilitare i criteri di controllo dell'archiviazione BLOB di un'area di lavoro di Azure Synapse Analytics denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1b78-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1b78-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a1b78-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="a1b78-116">Disabilitare i criteri di controllo dell'archiviazione BLOB di un'area di lavoro di analisi di Azure Synapse denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1b78-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1b78-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a1b78-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="a1b78-118">Abilitare i criteri di controllo dell'archiviazione BLOB di un'area di lavoro di analisi Di azure Synapse denominata ContosoWorkspace con filtri avanzati usando un predicato T-SQL.</span><span class="sxs-lookup"><span data-stu-id="a1b78-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="a1b78-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a1b78-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="a1b78-120">Rimuovere l'impostazione di filtro avanzato dai criteri di controllo di un'area di lavoro di Azure Synapse Analytics denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1b78-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a1b78-121">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="a1b78-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="a1b78-122">Disabilitare i criteri di controllo dell'archiviazione BLOB di un'area di lavoro di analisi di Azure Synapse denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1b78-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a1b78-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1b78-123">PARAMETERS</span></span>

### <span data-ttu-id="a1b78-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1b78-124">-AsJob</span></span>
<span data-ttu-id="a1b78-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a1b78-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1b78-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="a1b78-126">-AuditActionGroup</span></span>
<span data-ttu-id="a1b78-127">La combinazione consigliata di gruppi di azioni da usare è la seguente: in questo modo verranno controllati tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti:</span><span class="sxs-lookup"><span data-stu-id="a1b78-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="a1b78-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a1b78-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="a1b78-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a1b78-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="a1b78-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="a1b78-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="a1b78-131">Anche questa combinazione è configurata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a1b78-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="a1b78-132">Questi gruppi coprono tutte SQL istruzione e le stored procedure eseguite sul database e non devono essere usati insieme ad altri gruppi perché ciò genererà log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="a1b78-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="a1b78-133">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="a1b78-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b78-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="a1b78-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="a1b78-135">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="a1b78-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="a1b78-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b78-136">-DefaultProfile</span></span>
<span data-ttu-id="a1b78-137">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b78-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b78-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1b78-138">-InputObject</span></span>
<span data-ttu-id="a1b78-139">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1b78-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b78-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1b78-140">-PassThru</span></span>
<span data-ttu-id="a1b78-141">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a1b78-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a1b78-142">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a1b78-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a1b78-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="a1b78-143">-PredicateExpression</span></span>
<span data-ttu-id="a1b78-144">Predicato di SQL T (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a1b78-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="a1b78-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b78-145">-ResourceGroupName</span></span>
<span data-ttu-id="a1b78-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1b78-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b78-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b78-147">-ResourceId</span></span>
<span data-ttu-id="a1b78-148">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a1b78-148">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b78-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a1b78-149">-RetentionInDays</span></span>
<span data-ttu-id="a1b78-150">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a1b78-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="a1b78-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a1b78-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="a1b78-152">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a1b78-152">The storage account resource id</span></span>

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

### <span data-ttu-id="a1b78-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a1b78-153">-StorageKeyType</span></span>
<span data-ttu-id="a1b78-154">Specifica quale delle chiavi di accesso di archiviazione usare.</span><span class="sxs-lookup"><span data-stu-id="a1b78-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="a1b78-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1b78-155">-WorkspaceName</span></span>
<span data-ttu-id="a1b78-156">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a1b78-156">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b78-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1b78-157">-Confirm</span></span>
<span data-ttu-id="a1b78-158">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1b78-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1b78-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b78-159">-WhatIf</span></span>
<span data-ttu-id="a1b78-160">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1b78-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b78-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1b78-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1b78-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b78-162">CommonParameters</span></span>
<span data-ttu-id="a1b78-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b78-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b78-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1b78-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b78-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1b78-165">INPUTS</span></span>

### <span data-ttu-id="a1b78-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1b78-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a1b78-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1b78-167">OUTPUTS</span></span>

### <span data-ttu-id="a1b78-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="a1b78-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="a1b78-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1b78-169">NOTES</span></span>

## <span data-ttu-id="a1b78-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1b78-170">RELATED LINKS</span></span>
