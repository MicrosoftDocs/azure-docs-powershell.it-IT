---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301704"
---
# <span data-ttu-id="75980-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="75980-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="75980-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75980-102">SYNOPSIS</span></span>
<span data-ttu-id="75980-103">Ripristina un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="75980-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="75980-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75980-104">SYNTAX</span></span>

### <span data-ttu-id="75980-105">RestoreFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75980-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75980-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75980-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75980-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75980-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75980-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75980-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75980-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75980-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75980-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75980-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75980-115">DESCRIPTION</span></span>
<span data-ttu-id="75980-116">Il cmdlet **Restore-AzSynapseSqlPool** ripristina un pool SQL di analisi delle sinapsi di Azure da un backup o da un punto di ripristino di qualsiasi pool SQL.</span><span class="sxs-lookup"><span data-stu-id="75980-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="75980-117">Il pool SQL ripristinato viene creato come nuovo pool SQL.</span><span class="sxs-lookup"><span data-stu-id="75980-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="75980-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75980-118">EXAMPLES</span></span>

### <span data-ttu-id="75980-119">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75980-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="75980-120">Questo comando crea un pool SQL di analisi delle sinapsi di Azure tramite il ripristino dal backup più recente di qualsiasi pool SQL in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75980-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="75980-121">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75980-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="75980-122">Questo comando crea un pool SQL di analisi delle sinapsi di Azure sfruttando un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare uno stato precedente.</span><span class="sxs-lookup"><span data-stu-id="75980-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="75980-123">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="75980-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="75980-124">Questo comando crea un pool SQL di analisi delle sinapsi di Azure tramite il ripristino dal backup più recente di qualsiasi pool SQL in questo abbonamento con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="75980-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="75980-125">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="75980-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="75980-126">Questo comando crea un pool SQL di analisi delle sinapsi di Azure sfruttando un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare uno stato precedente con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="75980-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="75980-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75980-127">PARAMETERS</span></span>

### <span data-ttu-id="75980-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75980-128">-AsJob</span></span>
<span data-ttu-id="75980-129">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="75980-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75980-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75980-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="75980-131">Il nome del gruppo di risorse dell'oggetto pool SQL bakcup da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="75980-132">-BackupResourceId</span></span>
<span data-ttu-id="75980-133">Identificatore delle risorse dell'oggetto pool di backup SQL da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="75980-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="75980-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="75980-135">Nome dell'oggetto pool SQL bakcup da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="75980-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="75980-137">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="75980-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75980-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="75980-139">Nome dell'area di lavoro sinapsi dell'oggetto pool SQL bakcup da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75980-140">-DefaultProfile</span></span>
<span data-ttu-id="75980-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75980-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75980-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="75980-142">-FromBackup</span></span>
<span data-ttu-id="75980-143">Indica di ripristinare il backup più recente di qualsiasi pool SQL in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="75980-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="75980-144">-FromRestorePoint</span></span>
<span data-ttu-id="75980-145">Indica di sfruttare un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare uno stato precedente.</span><span class="sxs-lookup"><span data-stu-id="75980-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="75980-146">-Name</span></span>
<span data-ttu-id="75980-147">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="75980-147">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="75980-148">-PerformanceLevel</span></span>
<span data-ttu-id="75980-149">Livello di prestazioni e livelli di servizio SQL da assegnare al pool SQL.</span><span class="sxs-lookup"><span data-stu-id="75980-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="75980-150">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="75980-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75980-151">-ResourceGroupName</span></span>
<span data-ttu-id="75980-152">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75980-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="75980-153">-RestorePoint</span></span>
<span data-ttu-id="75980-154">Tempo di snapshot da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="75980-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75980-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="75980-156">Il nome del gruppo di risorse dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="75980-157">-SourceResourceId</span></span>
<span data-ttu-id="75980-158">Identificatore delle risorse dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-158">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="75980-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="75980-160">Nome dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="75980-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="75980-162">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="75980-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75980-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="75980-164">Il nome dell'area di lavoro sinapsi dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="75980-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="75980-165">-Tag</span></span>
<span data-ttu-id="75980-166">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="75980-166">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75980-167">-WorkspaceName</span></span>
<span data-ttu-id="75980-168">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="75980-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75980-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="75980-169">-WorkspaceObject</span></span>
<span data-ttu-id="75980-170">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="75980-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75980-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75980-171">-Confirm</span></span>
<span data-ttu-id="75980-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75980-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75980-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75980-173">-WhatIf</span></span>
<span data-ttu-id="75980-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75980-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75980-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75980-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75980-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75980-176">CommonParameters</span></span>
<span data-ttu-id="75980-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75980-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75980-178">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75980-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75980-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75980-179">INPUTS</span></span>

### <span data-ttu-id="75980-180">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75980-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="75980-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75980-181">OUTPUTS</span></span>

### <span data-ttu-id="75980-182">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="75980-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="75980-183">Note</span><span class="sxs-lookup"><span data-stu-id="75980-183">NOTES</span></span>

## <span data-ttu-id="75980-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75980-184">RELATED LINKS</span></span>
