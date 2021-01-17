---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476564"
---
# <span data-ttu-id="4bee9-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4bee9-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="4bee9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bee9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bee9-103">Modifica la proprietà transparent per un pool SQL.</span><span class="sxs-lookup"><span data-stu-id="4bee9-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="4bee9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bee9-104">SYNTAX</span></span>

### <span data-ttu-id="4bee9-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4bee9-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bee9-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bee9-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bee9-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bee9-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bee9-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bee9-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bee9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bee9-109">DESCRIPTION</span></span>
<span data-ttu-id="4bee9-110">Il cmdlet **set-AzSynapseSqlPoolTransparentDataEncryption** modifica la proprietà Transparent Data Encryption (SecurityTransparent) di un pool SQL di analisi di una sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="4bee9-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4bee9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bee9-111">EXAMPLES</span></span>

### <span data-ttu-id="4bee9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4bee9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="4bee9-113">Questo comando consente a Transparent per il pool SQL denominato ContosoSqlPool sotto l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4bee9-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4bee9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bee9-114">PARAMETERS</span></span>

### <span data-ttu-id="4bee9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bee9-115">-AsJob</span></span>
<span data-ttu-id="4bee9-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4bee9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bee9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bee9-117">-DefaultProfile</span></span>
<span data-ttu-id="4bee9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bee9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bee9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bee9-119">-InputObject</span></span>
<span data-ttu-id="4bee9-120">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bee9-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4bee9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4bee9-121">-Name</span></span>
<span data-ttu-id="4bee9-122">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="4bee9-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4bee9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bee9-123">-ResourceGroupName</span></span>
<span data-ttu-id="4bee9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4bee9-124">Resource group name.</span></span>

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

### <span data-ttu-id="4bee9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bee9-125">-ResourceId</span></span>
<span data-ttu-id="4bee9-126">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="4bee9-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4bee9-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="4bee9-127">-State</span></span>
<span data-ttu-id="4bee9-128">Lo stato di crittografia dati trasparente del pool di analisi di Azure sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="4bee9-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="4bee9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4bee9-129">-WorkspaceName</span></span>
<span data-ttu-id="4bee9-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="4bee9-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4bee9-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4bee9-131">-WorkspaceObject</span></span>
<span data-ttu-id="4bee9-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bee9-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4bee9-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4bee9-133">-Confirm</span></span>
<span data-ttu-id="4bee9-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bee9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bee9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bee9-135">-WhatIf</span></span>
<span data-ttu-id="4bee9-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bee9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bee9-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bee9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bee9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bee9-138">CommonParameters</span></span>
<span data-ttu-id="4bee9-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bee9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bee9-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bee9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bee9-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bee9-141">INPUTS</span></span>

### <span data-ttu-id="4bee9-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4bee9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4bee9-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4bee9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4bee9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bee9-144">OUTPUTS</span></span>

### <span data-ttu-id="4bee9-145">Microsoft. Azure. Commands. sinapsi. Models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4bee9-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="4bee9-146">Note</span><span class="sxs-lookup"><span data-stu-id="4bee9-146">NOTES</span></span>

## <span data-ttu-id="4bee9-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bee9-147">RELATED LINKS</span></span>
