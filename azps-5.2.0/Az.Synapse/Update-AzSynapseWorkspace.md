---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363282"
---
# <span data-ttu-id="86417-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="86417-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="86417-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86417-102">SYNOPSIS</span></span>
<span data-ttu-id="86417-103">Aggiorna un'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="86417-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="86417-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86417-104">SYNTAX</span></span>

### <span data-ttu-id="86417-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86417-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86417-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86417-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86417-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86417-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86417-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86417-108">DESCRIPTION</span></span>
<span data-ttu-id="86417-109">Il cmdlet **Update-AzSynapseWorkspace** aggiorna un'area di lavoro di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="86417-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="86417-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86417-110">EXAMPLES</span></span>

### <span data-ttu-id="86417-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86417-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="86417-112">Questo comando Aggiorna i tag per l'area di lavoro di specififed Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="86417-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="86417-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="86417-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="86417-114">Questo comando Aggiorna i tag per l'area di lavoro di specififed Azure sinapsi Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="86417-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="86417-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="86417-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="86417-116">Questo comando Aggiorna i tag per l'area di lavoro di specififed Azure sinapsi Analytics tramite pipeline con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="86417-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="86417-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86417-117">PARAMETERS</span></span>

### <span data-ttu-id="86417-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86417-118">-AsJob</span></span>
<span data-ttu-id="86417-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="86417-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86417-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86417-120">-DefaultProfile</span></span>
<span data-ttu-id="86417-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86417-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86417-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86417-122">-InputObject</span></span>
<span data-ttu-id="86417-123">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="86417-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86417-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="86417-124">-Name</span></span>
<span data-ttu-id="86417-125">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="86417-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86417-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86417-126">-ResourceGroupName</span></span>
<span data-ttu-id="86417-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86417-127">Resource group name.</span></span>

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

### <span data-ttu-id="86417-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86417-128">-ResourceId</span></span>
<span data-ttu-id="86417-129">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="86417-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="86417-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="86417-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="86417-131">La nuova password di amministratore SQL per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="86417-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86417-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="86417-132">-Tag</span></span>
<span data-ttu-id="86417-133">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="86417-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="86417-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86417-134">-Confirm</span></span>
<span data-ttu-id="86417-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86417-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86417-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86417-136">-WhatIf</span></span>
<span data-ttu-id="86417-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86417-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86417-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86417-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86417-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86417-139">CommonParameters</span></span>
<span data-ttu-id="86417-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86417-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86417-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86417-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86417-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86417-142">INPUTS</span></span>

### <span data-ttu-id="86417-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="86417-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="86417-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86417-144">OUTPUTS</span></span>

### <span data-ttu-id="86417-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="86417-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="86417-146">Note</span><span class="sxs-lookup"><span data-stu-id="86417-146">NOTES</span></span>

## <span data-ttu-id="86417-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86417-147">RELATED LINKS</span></span>
