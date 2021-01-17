---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476579"
---
# <span data-ttu-id="366d7-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="366d7-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="366d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="366d7-102">SYNOPSIS</span></span>
<span data-ttu-id="366d7-103">Modifica le impostazioni di controllo per un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="366d7-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="366d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="366d7-104">SYNTAX</span></span>

### <span data-ttu-id="366d7-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="366d7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366d7-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="366d7-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366d7-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="366d7-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="366d7-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="366d7-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366d7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="366d7-109">DESCRIPTION</span></span>
<span data-ttu-id="366d7-110">Il cmdlet **set-AzSynapseSqlPoolAuditSetting** modifica le impostazioni di controllo di un pool SQL di analisi di una sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="366d7-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="366d7-111">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i registri di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="366d7-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="366d7-112">È anche possibile definire la conservazione per i registri di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="366d7-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="366d7-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="366d7-113">EXAMPLES</span></span>

### <span data-ttu-id="366d7-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="366d7-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="366d7-115">Abilitare i criteri di controllo dello spazio di archiviazione BLOB di un pool di analisi SQL di Azure sinapsi denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="366d7-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="366d7-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="366d7-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="366d7-117">Disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un pool di analisi SQL sinapsi di Azure denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="366d7-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="366d7-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="366d7-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="366d7-119">Abilitare i criteri di controllo dello spazio di archiviazione BLOB di un pool di analisi SQL di Azure sinapsi denominato ContosoSqlPool con il filtro avanzato usando un predicato T-SQL.</span><span class="sxs-lookup"><span data-stu-id="366d7-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="366d7-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="366d7-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="366d7-121">Rimuovere l'impostazione di filtro avanzato dai criteri di controllo di un pool SQL di analisi di una sinapsi di Azure denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="366d7-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="366d7-122">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="366d7-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="366d7-123">Disabilitare i criteri di controllo dello spazio di archiviazione BLOB di un pool di analisi SQL sinapsi di Azure denominato ContosoSqlPool tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="366d7-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="366d7-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="366d7-124">PARAMETERS</span></span>

### <span data-ttu-id="366d7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="366d7-125">-AsJob</span></span>
<span data-ttu-id="366d7-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="366d7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="366d7-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="366d7-127">-AuditAction</span></span>
<span data-ttu-id="366d7-128">Il set di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="366d7-128">The set of audit actions.</span></span>

<span data-ttu-id="366d7-129">Le azioni supportate per il controllo sono:</span><span class="sxs-lookup"><span data-stu-id="366d7-129">The supported actions to audit are:</span></span>

<span data-ttu-id="366d7-130">Selezionare</span><span class="sxs-lookup"><span data-stu-id="366d7-130">SELECT</span></span>

<span data-ttu-id="366d7-131">AGGIORNAMENTO</span><span class="sxs-lookup"><span data-stu-id="366d7-131">UPDATE</span></span>

<span data-ttu-id="366d7-132">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="366d7-132">INSERT</span></span>

<span data-ttu-id="366d7-133">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="366d7-133">DELETE</span></span>

<span data-ttu-id="366d7-134">ESEGUIRE</span><span class="sxs-lookup"><span data-stu-id="366d7-134">EXECUTE</span></span>

<span data-ttu-id="366d7-135">RICEVERE</span><span class="sxs-lookup"><span data-stu-id="366d7-135">RECEIVE</span></span>

<span data-ttu-id="366d7-136">RIFERIMENTI</span><span class="sxs-lookup"><span data-stu-id="366d7-136">REFERENCES</span></span>

<span data-ttu-id="366d7-137">Il modulo generale per la definizione di un'azione da controllare è:</span><span class="sxs-lookup"><span data-stu-id="366d7-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="366d7-138">\[azione \] su \[ oggetto \] per \[ entità\]</span><span class="sxs-lookup"><span data-stu-id="366d7-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="366d7-139">Tieni presente \[ che \] l'oggetto nel formato precedente può fare riferimento a un oggetto come una tabella, una vista o una stored procedure oppure un intero database o uno schema.</span><span class="sxs-lookup"><span data-stu-id="366d7-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="366d7-140">Per questi ultimi casi, vengono usati rispettivamente il DATABASE Forms:: \[ dbname \] e lo schema:: \[ SchemaName \] .</span><span class="sxs-lookup"><span data-stu-id="366d7-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="366d7-141">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="366d7-141">For example:</span></span>

<span data-ttu-id="366d7-142">Selezionare su dbo. MyTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="366d7-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="366d7-143">Selezionare nel DATABASE:: database per pubblico</span><span class="sxs-lookup"><span data-stu-id="366d7-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="366d7-144">Selezionare su SCHEMA:: schema per pubblico</span><span class="sxs-lookup"><span data-stu-id="366d7-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="366d7-145">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="366d7-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="366d7-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="366d7-146">-AuditActionGroup</span></span>
<span data-ttu-id="366d7-147">Il set consigliato di gruppi di azioni da usare è la combinazione seguente: verificherà tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti.</span><span class="sxs-lookup"><span data-stu-id="366d7-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="366d7-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="366d7-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="366d7-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="366d7-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="366d7-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="366d7-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="366d7-151">Questa combinazione sopra è anche il set configurato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="366d7-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="366d7-152">Questi gruppi coprono tutte le istruzioni SQL e le stored procedure eseguite sul database e non devono essere usate in combinazione con altri gruppi, in quanto si tradurrà in log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="366d7-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="366d7-153">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="366d7-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="366d7-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="366d7-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="366d7-155">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="366d7-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="366d7-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366d7-156">-DefaultProfile</span></span>
<span data-ttu-id="366d7-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="366d7-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="366d7-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="366d7-158">-InputObject</span></span>
<span data-ttu-id="366d7-159">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="366d7-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="366d7-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="366d7-160">-Name</span></span>
<span data-ttu-id="366d7-161">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="366d7-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366d7-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="366d7-162">-PassThru</span></span>
<span data-ttu-id="366d7-163">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="366d7-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="366d7-164">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="366d7-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="366d7-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="366d7-165">-PredicateExpression</span></span>
<span data-ttu-id="366d7-166">Predicato T-SQL (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="366d7-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="366d7-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366d7-167">-ResourceGroupName</span></span>
<span data-ttu-id="366d7-168">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="366d7-168">Resource group name.</span></span>

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

### <span data-ttu-id="366d7-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="366d7-169">-ResourceId</span></span>
<span data-ttu-id="366d7-170">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="366d7-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="366d7-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="366d7-171">-RetentionInDays</span></span>
<span data-ttu-id="366d7-172">Numero di giorni di conservazione per i registri di controllo.</span><span class="sxs-lookup"><span data-stu-id="366d7-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="366d7-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="366d7-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="366d7-174">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="366d7-174">The storage account resource id</span></span>

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

### <span data-ttu-id="366d7-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="366d7-175">-StorageKeyType</span></span>
<span data-ttu-id="366d7-176">Specifica i tasti di scelta per l'archiviazione da usare.</span><span class="sxs-lookup"><span data-stu-id="366d7-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="366d7-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="366d7-177">-WorkspaceName</span></span>
<span data-ttu-id="366d7-178">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="366d7-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="366d7-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="366d7-179">-WorkspaceObject</span></span>
<span data-ttu-id="366d7-180">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="366d7-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="366d7-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="366d7-181">-Confirm</span></span>
<span data-ttu-id="366d7-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="366d7-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366d7-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="366d7-183">-WhatIf</span></span>
<span data-ttu-id="366d7-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="366d7-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="366d7-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="366d7-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366d7-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366d7-186">CommonParameters</span></span>
<span data-ttu-id="366d7-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366d7-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366d7-188">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="366d7-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366d7-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="366d7-189">INPUTS</span></span>

### <span data-ttu-id="366d7-190">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="366d7-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="366d7-191">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="366d7-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="366d7-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="366d7-192">OUTPUTS</span></span>

### <span data-ttu-id="366d7-193">Microsoft. Azure. Commands. sinapsi. Models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="366d7-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="366d7-194">Note</span><span class="sxs-lookup"><span data-stu-id="366d7-194">NOTES</span></span>

## <span data-ttu-id="366d7-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="366d7-195">RELATED LINKS</span></span>
