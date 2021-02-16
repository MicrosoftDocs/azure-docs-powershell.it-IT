---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182687"
---
# <span data-ttu-id="92a96-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="92a96-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="92a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a96-102">SYNOPSIS</span></span>
<span data-ttu-id="92a96-103">Ripristina un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="92a96-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="92a96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92a96-104">SYNTAX</span></span>

### <span data-ttu-id="92a96-105">RestoreFromBackupIdByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92a96-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92a96-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a96-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92a96-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a96-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92a96-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92a96-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a96-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92a96-109">DESCRIPTION</span></span>
<span data-ttu-id="92a96-110">Il cmdlet **Restore-AzSynapseSqlPool** ripristina un pool di SQL Azure Synapse Analytics da un backup o da un punto di ripristino di qualsiasi pool SQL.</span><span class="sxs-lookup"><span data-stu-id="92a96-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="92a96-111">Il pool SQL stato ripristinato viene creato come nuovo SQL pool.</span><span class="sxs-lookup"><span data-stu-id="92a96-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="92a96-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92a96-112">EXAMPLES</span></span>

### <span data-ttu-id="92a96-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92a96-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="92a96-114">Questo comando crea un pool di SQL Azure Synapse Analytics ripristinando dal backup più recente di qualsiasi pool di SQL in questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="92a96-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="92a96-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92a96-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="92a96-116">Questo comando crea un pool di SQL Azure Synapse Analytics sfruttando un punto di ripristino da qualsiasi pool di SQL in questa sottoscrizione per recuperare o copiare da uno stato precedente.</span><span class="sxs-lookup"><span data-stu-id="92a96-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="92a96-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="92a96-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="92a96-118">Questo comando crea un pool di SQL Azure Synapse Analytics ripristinando dal backup più recente di qualsiasi pool di SQL in questa sottoscrizione con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="92a96-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="92a96-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="92a96-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="92a96-120">Questo comando crea un pool di SQL Azure Synapse Analytics sfruttando un punto di ripristino da qualsiasi pool di SQL in questa sottoscrizione per recuperare o copiare da uno stato precedente con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="92a96-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="92a96-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92a96-121">PARAMETERS</span></span>

### <span data-ttu-id="92a96-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92a96-122">-AsJob</span></span>
<span data-ttu-id="92a96-123">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="92a96-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92a96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a96-124">-DefaultProfile</span></span>
<span data-ttu-id="92a96-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92a96-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a96-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="92a96-126">-FromBackup</span></span>
<span data-ttu-id="92a96-127">Indica di eseguire il ripristino dal backup più recente di qualsiasi pool SQL in questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="92a96-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="92a96-128">-FromRestorePoint</span></span>
<span data-ttu-id="92a96-129">Indica di usare un punto di ripristino da qualsiasi pool SQL in questo abbonamento per recuperare o copiare da uno stato precedente.</span><span class="sxs-lookup"><span data-stu-id="92a96-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-130">-Name</span><span class="sxs-lookup"><span data-stu-id="92a96-130">-Name</span></span>
<span data-ttu-id="92a96-131">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="92a96-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="92a96-132">-PerformanceLevel</span></span>
<span data-ttu-id="92a96-133">Il SQL servizio e il livello di prestazioni da assegnare al pool SQL locale.</span><span class="sxs-lookup"><span data-stu-id="92a96-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="92a96-134">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="92a96-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="92a96-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a96-135">-ResourceGroupName</span></span>
<span data-ttu-id="92a96-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92a96-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92a96-137">-ResourceId</span></span>
<span data-ttu-id="92a96-138">ID della risorsa del database da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="92a96-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="92a96-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="92a96-139">-RestorePoint</span></span>
<span data-ttu-id="92a96-140">Tempo di snapshot da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="92a96-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="92a96-141">-WorkspaceName</span></span>
<span data-ttu-id="92a96-142">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="92a96-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="92a96-143">-WorkspaceObject</span></span>
<span data-ttu-id="92a96-144">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="92a96-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92a96-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92a96-145">-Confirm</span></span>
<span data-ttu-id="92a96-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a96-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a96-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a96-147">-WhatIf</span></span>
<span data-ttu-id="92a96-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a96-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a96-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a96-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a96-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a96-150">CommonParameters</span></span>
<span data-ttu-id="92a96-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a96-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a96-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92a96-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a96-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="92a96-153">INPUTS</span></span>

### <span data-ttu-id="92a96-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="92a96-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="92a96-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92a96-155">OUTPUTS</span></span>

### <span data-ttu-id="92a96-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="92a96-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="92a96-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="92a96-157">NOTES</span></span>

## <span data-ttu-id="92a96-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92a96-158">RELATED LINKS</span></span>
