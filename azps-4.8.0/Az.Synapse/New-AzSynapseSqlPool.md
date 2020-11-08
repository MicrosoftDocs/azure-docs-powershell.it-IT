---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192632"
---
# <span data-ttu-id="9b989-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9b989-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9b989-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b989-102">SYNOPSIS</span></span>
<span data-ttu-id="9b989-103">Crea un pool di analisi delle sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="9b989-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b989-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b989-104">SYNTAX</span></span>

### <span data-ttu-id="9b989-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b989-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b989-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b989-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b989-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b989-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b989-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b989-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b989-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b989-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b989-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b989-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b989-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b989-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b989-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b989-117">DESCRIPTION</span></span>
<span data-ttu-id="9b989-118">Il cmdlet **New-AzSynapseSqlPool** crea un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b989-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9b989-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b989-119">EXAMPLES</span></span>

### <span data-ttu-id="9b989-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b989-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="9b989-121">Questo comando crea un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b989-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="9b989-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9b989-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9b989-123">Questo comando crea un pool SQL di analisi delle sinapsi di Azure tramite il ripristino dal backup più recente di qualsiasi pool SQL in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9b989-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="9b989-124">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9b989-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9b989-125">Questo comando crea un pool SQL di analisi delle sinapsi di Azure sfruttando un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare uno stato precedente.</span><span class="sxs-lookup"><span data-stu-id="9b989-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="9b989-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9b989-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="9b989-127">Questo comando crea un pool SQL di analisi delle sinapsi di Azure tramite il ripristino dal backup più recente di qualsiasi pool SQL in questo abbonamento con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b989-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="9b989-128">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="9b989-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="9b989-129">Questo comando crea un pool SQL di analisi delle sinapsi di Azure sfruttando un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare uno stato precedente con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b989-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="9b989-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b989-130">PARAMETERS</span></span>

### <span data-ttu-id="9b989-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b989-131">-AsJob</span></span>
<span data-ttu-id="9b989-132">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b989-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b989-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b989-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="9b989-134">Il nome del gruppo di risorse dell'oggetto pool SQL bakcup da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="9b989-135">-BackupResourceId</span></span>
<span data-ttu-id="9b989-136">Identificatore delle risorse dell'oggetto pool di backup SQL da cui ripristinare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="9b989-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9b989-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="9b989-138">Nome dell'oggetto pool SQL bakcup da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9b989-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="9b989-140">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b989-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b989-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="9b989-142">Nome dell'area di lavoro sinapsi dell'oggetto pool SQL bakcup da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-143">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="9b989-143">-Collation</span></span>
<span data-ttu-id="9b989-144">La fascicolatura definisce le regole di ordinamento e confronto dei dati e non può essere modificata dopo la creazione del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="9b989-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="9b989-145">Le regole di confronto predefinite sono SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="9b989-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b989-146">-DefaultProfile</span></span>
<span data-ttu-id="9b989-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b989-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b989-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="9b989-148">-FromBackup</span></span>
<span data-ttu-id="9b989-149">Indica di ripristinare il backup più recente di qualsiasi pool SQL in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9b989-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9b989-150">-FromRestorePoint</span></span>
<span data-ttu-id="9b989-151">Indica di sfruttare un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare uno stato precedente.</span><span class="sxs-lookup"><span data-stu-id="9b989-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b989-152">-Name</span></span>
<span data-ttu-id="9b989-153">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="9b989-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9b989-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9b989-154">-PerformanceLevel</span></span>
<span data-ttu-id="9b989-155">Livello di prestazioni e livelli di servizio SQL da assegnare al pool SQL.</span><span class="sxs-lookup"><span data-stu-id="9b989-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9b989-156">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="9b989-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b989-157">-ResourceGroupName</span></span>
<span data-ttu-id="9b989-158">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b989-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="9b989-159">-RestorePoint</span></span>
<span data-ttu-id="9b989-160">Tempo di snapshot da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="9b989-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b989-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="9b989-162">Il nome del gruppo di risorse dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9b989-163">-SourceResourceId</span></span>
<span data-ttu-id="9b989-164">Identificatore delle risorse dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9b989-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="9b989-166">Nome dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9b989-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="9b989-168">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b989-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b989-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="9b989-170">Il nome dell'area di lavoro sinapsi dell'oggetto pool SQL di origine da cui creare.</span><span class="sxs-lookup"><span data-stu-id="9b989-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b989-171">-Tag</span></span>
<span data-ttu-id="9b989-172">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b989-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="9b989-173">-Versione</span><span class="sxs-lookup"><span data-stu-id="9b989-173">-Version</span></span>
<span data-ttu-id="9b989-174">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="9b989-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="9b989-175">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="9b989-175">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b989-176">-WorkspaceName</span></span>
<span data-ttu-id="9b989-177">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="9b989-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-178">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9b989-178">-WorkspaceObject</span></span>
<span data-ttu-id="9b989-179">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b989-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b989-180">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b989-180">-Confirm</span></span>
<span data-ttu-id="9b989-181">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b989-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b989-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b989-182">-WhatIf</span></span>
<span data-ttu-id="9b989-183">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b989-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b989-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b989-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b989-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b989-185">CommonParameters</span></span>
<span data-ttu-id="9b989-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b989-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b989-187">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b989-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b989-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b989-188">INPUTS</span></span>

### <span data-ttu-id="9b989-189">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b989-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9b989-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b989-190">OUTPUTS</span></span>

### <span data-ttu-id="9b989-191">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9b989-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9b989-192">Note</span><span class="sxs-lookup"><span data-stu-id="9b989-192">NOTES</span></span>

## <span data-ttu-id="9b989-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b989-193">RELATED LINKS</span></span>
