---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195559"
---
# <span data-ttu-id="e72a0-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e72a0-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="e72a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e72a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e72a0-103">Modifica le impostazioni di controllo per un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e72a0-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e72a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e72a0-104">SYNTAX</span></span>

### <span data-ttu-id="e72a0-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e72a0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72a0-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e72a0-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72a0-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e72a0-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e72a0-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e72a0-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e72a0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e72a0-109">DESCRIPTION</span></span>
<span data-ttu-id="e72a0-110">Il cmdlet **Set-AzSynapseSqlPoolAuditSetting** modifica le impostazioni di controllo di un SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e72a0-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="e72a0-111">Quando l'archiviazione BLOB è una destinazione per i log di controllo, specificare il parametro *StorageAccountResourceId* per determinare l'account di archiviazione per i log di controllo e il parametro *StorageKeyType* per definire le chiavi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e72a0-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="e72a0-112">È anche possibile definire la conservazione per i log di controllo impostando il valore del parametro *RetentionInDays* per definire il periodo per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="e72a0-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="e72a0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e72a0-113">EXAMPLES</span></span>

### <span data-ttu-id="e72a0-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e72a0-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="e72a0-115">Abilitare i criteri di controllo dell'archiviazione BLOB di un pool di SQL Azure Synapse Analytics denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="e72a0-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="e72a0-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e72a0-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="e72a0-117">Disabilitare i criteri di controllo dell'archiviazione BLOB di un pool di SQL Azure Synapse Analytics denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="e72a0-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="e72a0-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e72a0-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="e72a0-119">Abilitare i criteri di controllo dell'archiviazione BLOB di un pool di SQL Azure Synapse Analytics denominato ContosoSqlPool con filtri avanzati usando un predicato di SQL T.</span><span class="sxs-lookup"><span data-stu-id="e72a0-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="e72a0-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e72a0-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="e72a0-121">Rimuovere l'impostazione di filtro avanzato dai criteri di controllo di un SQL Azure Synapse Analytics denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="e72a0-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="e72a0-122">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="e72a0-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="e72a0-123">Disabilitare i criteri di controllo dell'archiviazione BLOB di un pool di SQL Azure Synapse Analytics denominato ContosoSqlPool tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e72a0-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="e72a0-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e72a0-124">PARAMETERS</span></span>

### <span data-ttu-id="e72a0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e72a0-125">-AsJob</span></span>
<span data-ttu-id="e72a0-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e72a0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e72a0-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="e72a0-127">-AuditAction</span></span>
<span data-ttu-id="e72a0-128">Insieme di azioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="e72a0-128">The set of audit actions.</span></span>

<span data-ttu-id="e72a0-129">Le azioni supportate da controllare sono:</span><span class="sxs-lookup"><span data-stu-id="e72a0-129">The supported actions to audit are:</span></span>

<span data-ttu-id="e72a0-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="e72a0-130">SELECT</span></span>

<span data-ttu-id="e72a0-131">UPDATE</span><span class="sxs-lookup"><span data-stu-id="e72a0-131">UPDATE</span></span>

<span data-ttu-id="e72a0-132">INS</span><span class="sxs-lookup"><span data-stu-id="e72a0-132">INSERT</span></span>

<span data-ttu-id="e72a0-133">CANC</span><span class="sxs-lookup"><span data-stu-id="e72a0-133">DELETE</span></span>

<span data-ttu-id="e72a0-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="e72a0-134">EXECUTE</span></span>

<span data-ttu-id="e72a0-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="e72a0-135">RECEIVE</span></span>

<span data-ttu-id="e72a0-136">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="e72a0-136">REFERENCES</span></span>

<span data-ttu-id="e72a0-137">Il modulo generale per la definizione di un'azione da controllare è:</span><span class="sxs-lookup"><span data-stu-id="e72a0-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="e72a0-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="e72a0-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="e72a0-139">Si noti che un oggetto nel formato precedente può fare riferimento a un oggetto come una tabella, una visualizzazione o una stored procedure oppure a \[ un intero database o \] schema.</span><span class="sxs-lookup"><span data-stu-id="e72a0-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="e72a0-140">Per gli ultimi casi, vengono usate, rispettivamente, le maschere DATABASE:: \[ nome db e \] SCHEMA:: \[ nome \] schema.</span><span class="sxs-lookup"><span data-stu-id="e72a0-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="e72a0-141">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="e72a0-141">For example:</span></span>

<span data-ttu-id="e72a0-142">SELECT su dbo.myTable per pubblico</span><span class="sxs-lookup"><span data-stu-id="e72a0-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="e72a0-143">SELECT su DATABASE::myDatabase per pubblico</span><span class="sxs-lookup"><span data-stu-id="e72a0-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="e72a0-144">SELECT su SCHEMA::mySchema per pubblico</span><span class="sxs-lookup"><span data-stu-id="e72a0-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="e72a0-145">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="e72a0-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="e72a0-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e72a0-146">-AuditActionGroup</span></span>
<span data-ttu-id="e72a0-147">La combinazione consigliata di gruppi di azioni da usare è la seguente: in questo modo verranno controllati tutte le query e le stored procedure eseguite nel database, nonché gli accessi riusciti e non riusciti:</span><span class="sxs-lookup"><span data-stu-id="e72a0-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="e72a0-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e72a0-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="e72a0-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e72a0-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="e72a0-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="e72a0-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="e72a0-151">Anche questa combinazione è configurata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e72a0-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="e72a0-152">Questi gruppi coprono tutte SQL istruzione e le stored procedure eseguite sul database e non devono essere usati insieme ad altri gruppi perché ciò genererà log di controllo duplicati.</span><span class="sxs-lookup"><span data-stu-id="e72a0-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="e72a0-153">Per altre informazioni, vedere https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="e72a0-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="e72a0-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="e72a0-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="e72a0-155">Indica se l'archiviazione BLOB è una destinazione per i record di controllo.</span><span class="sxs-lookup"><span data-stu-id="e72a0-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="e72a0-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72a0-156">-DefaultProfile</span></span>
<span data-ttu-id="e72a0-157">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e72a0-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e72a0-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e72a0-158">-InputObject</span></span>
<span data-ttu-id="e72a0-159">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="e72a0-159">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e72a0-160">-Name</span><span class="sxs-lookup"><span data-stu-id="e72a0-160">-Name</span></span>
<span data-ttu-id="e72a0-161">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e72a0-161">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e72a0-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e72a0-162">-PassThru</span></span>
<span data-ttu-id="e72a0-163">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e72a0-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e72a0-164">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e72a0-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e72a0-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="e72a0-165">-PredicateExpression</span></span>
<span data-ttu-id="e72a0-166">Predicato di SQL T (clausola WHERE) usato per filtrare i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="e72a0-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="e72a0-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72a0-167">-ResourceGroupName</span></span>
<span data-ttu-id="e72a0-168">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e72a0-168">Resource group name.</span></span>

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

### <span data-ttu-id="e72a0-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e72a0-169">-ResourceId</span></span>
<span data-ttu-id="e72a0-170">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="e72a0-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="e72a0-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e72a0-171">-RetentionInDays</span></span>
<span data-ttu-id="e72a0-172">Numero di giorni di conservazione per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="e72a0-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="e72a0-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e72a0-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="e72a0-174">ID risorsa account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e72a0-174">The storage account resource id</span></span>

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

### <span data-ttu-id="e72a0-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e72a0-175">-StorageKeyType</span></span>
<span data-ttu-id="e72a0-176">Specifica quale delle chiavi di accesso di archiviazione usare.</span><span class="sxs-lookup"><span data-stu-id="e72a0-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="e72a0-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e72a0-177">-WorkspaceName</span></span>
<span data-ttu-id="e72a0-178">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="e72a0-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e72a0-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e72a0-179">-WorkspaceObject</span></span>
<span data-ttu-id="e72a0-180">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="e72a0-180">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e72a0-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e72a0-181">-Confirm</span></span>
<span data-ttu-id="e72a0-182">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e72a0-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e72a0-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e72a0-183">-WhatIf</span></span>
<span data-ttu-id="e72a0-184">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e72a0-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e72a0-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e72a0-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e72a0-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72a0-186">CommonParameters</span></span>
<span data-ttu-id="e72a0-187">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72a0-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72a0-188">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e72a0-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72a0-189">INPUT</span><span class="sxs-lookup"><span data-stu-id="e72a0-189">INPUTS</span></span>

### <span data-ttu-id="e72a0-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e72a0-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e72a0-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e72a0-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e72a0-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e72a0-192">OUTPUTS</span></span>

### <span data-ttu-id="e72a0-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="e72a0-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="e72a0-194">NOTE</span><span class="sxs-lookup"><span data-stu-id="e72a0-194">NOTES</span></span>

## <span data-ttu-id="e72a0-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e72a0-195">RELATED LINKS</span></span>
