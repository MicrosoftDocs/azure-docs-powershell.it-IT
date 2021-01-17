---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383403"
---
# <span data-ttu-id="b1f1e-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b1f1e-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b1f1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f1e-103">Rimuove un amministratore di Azure AD per l'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="b1f1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1f1e-104">SYNTAX</span></span>

### <span data-ttu-id="b1f1e-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1f1e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1f1e-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1f1e-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1f1e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1f1e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f1e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1f1e-108">DESCRIPTION</span></span>
<span data-ttu-id="b1f1e-109">Il cmdlet **Remove-AzSynapseSqlActiveDirectoryAdministrator** rimuove un amministratore di Azure Active Directory (Azure ad) per l'area di lavoro Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="b1f1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1f1e-110">EXAMPLES</span></span>

### <span data-ttu-id="b1f1e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1f1e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b1f1e-112">Questo comando rimuove l'amministratore di Azure AD per l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b1f1e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1f1e-113">PARAMETERS</span></span>

### <span data-ttu-id="b1f1e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1f1e-114">-AsJob</span></span>
<span data-ttu-id="b1f1e-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b1f1e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1f1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f1e-116">-DefaultProfile</span></span>
<span data-ttu-id="b1f1e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f1e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b1f1e-118">-Force</span></span>
<span data-ttu-id="b1f1e-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b1f1e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1f1e-120">-InputObject</span></span>
<span data-ttu-id="b1f1e-121">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f1e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1f1e-122">-PassThru</span></span>
<span data-ttu-id="b1f1e-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b1f1e-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b1f1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1f1e-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f1e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1f1e-127">-ResourceId</span></span>
<span data-ttu-id="b1f1e-128">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f1e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1f1e-129">-WorkspaceName</span></span>
<span data-ttu-id="b1f1e-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f1e-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1f1e-131">-Confirm</span></span>
<span data-ttu-id="b1f1e-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f1e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f1e-133">-WhatIf</span></span>
<span data-ttu-id="b1f1e-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f1e-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f1e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f1e-136">CommonParameters</span></span>
<span data-ttu-id="b1f1e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f1e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f1e-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1f1e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f1e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1f1e-139">INPUTS</span></span>

### <span data-ttu-id="b1f1e-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b1f1e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b1f1e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1f1e-141">OUTPUTS</span></span>

### <span data-ttu-id="b1f1e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1f1e-142">System.Boolean</span></span>

## <span data-ttu-id="b1f1e-143">Note</span><span class="sxs-lookup"><span data-stu-id="b1f1e-143">NOTES</span></span>

## <span data-ttu-id="b1f1e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1f1e-144">RELATED LINKS</span></span>
