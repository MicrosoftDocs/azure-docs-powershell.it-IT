---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197326"
---
# <span data-ttu-id="4f2b7-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4f2b7-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="4f2b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2b7-103">Modifica la proprietà TDE per un SQL pool.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="4f2b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f2b7-104">SYNTAX</span></span>

### <span data-ttu-id="4f2b7-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f2b7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f2b7-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f2b7-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f2b7-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f2b7-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f2b7-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f2b7-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f2b7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f2b7-109">DESCRIPTION</span></span>
<span data-ttu-id="4f2b7-110">Il cmdlet **Set-AzSynapseSqlPoolTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (TDE) di un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4f2b7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f2b7-111">EXAMPLES</span></span>

### <span data-ttu-id="4f2b7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f2b7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="4f2b7-113">Questo comando abilita TDE per il pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4f2b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f2b7-114">PARAMETERS</span></span>

### <span data-ttu-id="4f2b7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f2b7-115">-AsJob</span></span>
<span data-ttu-id="4f2b7-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4f2b7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f2b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2b7-117">-DefaultProfile</span></span>
<span data-ttu-id="4f2b7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f2b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f2b7-119">-InputObject</span></span>
<span data-ttu-id="4f2b7-120">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4f2b7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4f2b7-121">-Name</span></span>
<span data-ttu-id="4f2b7-122">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4f2b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f2b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f2b7-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-124">Resource group name.</span></span>

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

### <span data-ttu-id="4f2b7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f2b7-125">-ResourceId</span></span>
<span data-ttu-id="4f2b7-126">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4f2b7-127">-State</span><span class="sxs-lookup"><span data-stu-id="4f2b7-127">-State</span></span>
<span data-ttu-id="4f2b7-128">Stato crittografia dati trasparente del pool Sql di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="4f2b7-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4f2b7-129">-WorkspaceName</span></span>
<span data-ttu-id="4f2b7-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4f2b7-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4f2b7-131">-WorkspaceObject</span></span>
<span data-ttu-id="4f2b7-132">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4f2b7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f2b7-133">-Confirm</span></span>
<span data-ttu-id="4f2b7-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f2b7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f2b7-135">-WhatIf</span></span>
<span data-ttu-id="4f2b7-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f2b7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f2b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2b7-138">CommonParameters</span></span>
<span data-ttu-id="4f2b7-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2b7-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f2b7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2b7-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f2b7-141">INPUTS</span></span>

### <span data-ttu-id="4f2b7-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4f2b7-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4f2b7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4f2b7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4f2b7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f2b7-144">OUTPUTS</span></span>

### <span data-ttu-id="4f2b7-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4f2b7-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="4f2b7-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f2b7-146">NOTES</span></span>

## <span data-ttu-id="4f2b7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f2b7-147">RELATED LINKS</span></span>
