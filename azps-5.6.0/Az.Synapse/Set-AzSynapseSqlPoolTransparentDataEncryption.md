---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cdc72a2bb0e21873bd0fa2d82123afe8ed011378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992093"
---
# <span data-ttu-id="1653f-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1653f-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="1653f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1653f-102">SYNOPSIS</span></span>
<span data-ttu-id="1653f-103">Modifica la proprietà TDE per un SQL pool.</span><span class="sxs-lookup"><span data-stu-id="1653f-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="1653f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1653f-104">SYNTAX</span></span>

### <span data-ttu-id="1653f-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1653f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1653f-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1653f-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1653f-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1653f-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1653f-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1653f-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1653f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1653f-109">DESCRIPTION</span></span>
<span data-ttu-id="1653f-110">Il cmdlet **Set-AzSynapseSqlPoolTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (TDE) di un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1653f-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1653f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1653f-111">EXAMPLES</span></span>

### <span data-ttu-id="1653f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1653f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="1653f-113">Questo comando abilita TDE per il pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1653f-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1653f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1653f-114">PARAMETERS</span></span>

### <span data-ttu-id="1653f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1653f-115">-AsJob</span></span>
<span data-ttu-id="1653f-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1653f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1653f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1653f-117">-DefaultProfile</span></span>
<span data-ttu-id="1653f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1653f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1653f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1653f-119">-InputObject</span></span>
<span data-ttu-id="1653f-120">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1653f-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1653f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1653f-121">-Name</span></span>
<span data-ttu-id="1653f-122">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1653f-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1653f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1653f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1653f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1653f-124">Resource group name.</span></span>

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

### <span data-ttu-id="1653f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1653f-125">-ResourceId</span></span>
<span data-ttu-id="1653f-126">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="1653f-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="1653f-127">-State</span><span class="sxs-lookup"><span data-stu-id="1653f-127">-State</span></span>
<span data-ttu-id="1653f-128">Stato di crittografia dati trasparente del pool SQL di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1653f-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1653f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1653f-129">-WorkspaceName</span></span>
<span data-ttu-id="1653f-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="1653f-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1653f-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1653f-131">-WorkspaceObject</span></span>
<span data-ttu-id="1653f-132">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1653f-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1653f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1653f-133">-Confirm</span></span>
<span data-ttu-id="1653f-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1653f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1653f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1653f-135">-WhatIf</span></span>
<span data-ttu-id="1653f-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1653f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1653f-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1653f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1653f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1653f-138">CommonParameters</span></span>
<span data-ttu-id="1653f-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1653f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1653f-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1653f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1653f-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="1653f-141">INPUTS</span></span>

### <span data-ttu-id="1653f-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1653f-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1653f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1653f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1653f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1653f-144">OUTPUTS</span></span>

### <span data-ttu-id="1653f-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1653f-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="1653f-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="1653f-146">NOTES</span></span>

## <span data-ttu-id="1653f-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1653f-147">RELATED LINKS</span></span>
