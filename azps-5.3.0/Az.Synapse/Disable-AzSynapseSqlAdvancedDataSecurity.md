---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384145"
---
# <span data-ttu-id="17aaa-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="17aaa-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="17aaa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="17aaa-103">Disabilita la sicurezza dei dati avanzata in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="17aaa-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="17aaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17aaa-104">SYNTAX</span></span>

### <span data-ttu-id="17aaa-105">DisableByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17aaa-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17aaa-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17aaa-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17aaa-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17aaa-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17aaa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17aaa-108">DESCRIPTION</span></span>
<span data-ttu-id="17aaa-109">Il cmdlet **Disable-AzSynapseSqlAdvancedDataSecurity Disabilita** la sicurezza dei dati avanzata in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="17aaa-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="17aaa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17aaa-110">EXAMPLES</span></span>

### <span data-ttu-id="17aaa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17aaa-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="17aaa-112">Questo comando Disabilita la sicurezza dei dati avanzata nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="17aaa-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="17aaa-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17aaa-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="17aaa-114">Questo comando Disabilita la sicurezza dei dati avanzata nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="17aaa-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="17aaa-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17aaa-115">PARAMETERS</span></span>

### <span data-ttu-id="17aaa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17aaa-116">-AsJob</span></span>
<span data-ttu-id="17aaa-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="17aaa-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17aaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17aaa-118">-DefaultProfile</span></span>
<span data-ttu-id="17aaa-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17aaa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17aaa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17aaa-120">-InputObject</span></span>
<span data-ttu-id="17aaa-121">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="17aaa-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17aaa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17aaa-122">-ResourceGroupName</span></span>
<span data-ttu-id="17aaa-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17aaa-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17aaa-124">-ResourceId</span></span>
<span data-ttu-id="17aaa-125">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="17aaa-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaa-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17aaa-126">-WorkspaceName</span></span>
<span data-ttu-id="17aaa-127">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="17aaa-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aaa-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17aaa-128">-Confirm</span></span>
<span data-ttu-id="17aaa-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17aaa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17aaa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17aaa-130">-WhatIf</span></span>
<span data-ttu-id="17aaa-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17aaa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17aaa-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17aaa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17aaa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17aaa-133">CommonParameters</span></span>
<span data-ttu-id="17aaa-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17aaa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17aaa-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17aaa-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17aaa-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17aaa-136">INPUTS</span></span>

### <span data-ttu-id="17aaa-137">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="17aaa-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="17aaa-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17aaa-138">OUTPUTS</span></span>

### <span data-ttu-id="17aaa-139">Microsoft. Azure. Commands. sinapsi. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="17aaa-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="17aaa-140">Note</span><span class="sxs-lookup"><span data-stu-id="17aaa-140">NOTES</span></span>

## <span data-ttu-id="17aaa-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17aaa-141">RELATED LINKS</span></span>
