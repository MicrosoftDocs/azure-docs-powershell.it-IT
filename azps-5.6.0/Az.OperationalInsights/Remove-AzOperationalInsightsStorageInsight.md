---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 7eece12130095889c5da574a4d0a3ec8d0b0bed2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989769"
---
# <span data-ttu-id="b9287-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b9287-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="b9287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9287-102">SYNOPSIS</span></span>
<span data-ttu-id="b9287-103">Rimuove un approfondimento di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b9287-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="b9287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9287-104">SYNTAX</span></span>

### <span data-ttu-id="b9287-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9287-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9287-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9287-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9287-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9287-107">DESCRIPTION</span></span>
<span data-ttu-id="b9287-108">Il cmdlet **Remove-AzOperationalInsightsStorageInsight** elimina un elemento Storage Insight da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b9287-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="b9287-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9287-109">EXAMPLES</span></span>

### <span data-ttu-id="b9287-110">Esempio 1: Rimuovere un approfondimento di archiviazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="b9287-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="b9287-111">Questo comando rimuove le informazioni di archiviazione denominate MyStorageInsight dall'area di lavoro denominata MyWorkspace nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b9287-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="b9287-112">Il comando non specifica il parametro *Force,* quindi richiede conferma prima di rimuovere Informazioni sull'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b9287-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="b9287-113">Esempio 2: Rimuovere un approfondimento di archiviazione senza conferma</span><span class="sxs-lookup"><span data-stu-id="b9287-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="b9287-114">Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkspace e quindi la archivia nella $Workspace variabile. Il secondo comando rimuove le informazioni di archiviazione denominate MyStorageInsight $Workspace senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b9287-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="b9287-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9287-115">PARAMETERS</span></span>

### <span data-ttu-id="b9287-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9287-116">-DefaultProfile</span></span>
<span data-ttu-id="b9287-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b9287-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9287-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b9287-118">-Force</span></span>
<span data-ttu-id="b9287-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b9287-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9287-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b9287-120">-Name</span></span>
<span data-ttu-id="b9287-121">Specifica il nome dell'approfondimento di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b9287-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9287-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9287-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9287-123">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="b9287-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9287-124">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b9287-124">-Workspace</span></span>
<span data-ttu-id="b9287-125">Specifica l'area di lavoro che contiene i dati di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b9287-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9287-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9287-126">-WorkspaceName</span></span>
<span data-ttu-id="b9287-127">Specifica il nome dell'area di lavoro contenente informazioni dettagliate sull'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b9287-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9287-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9287-128">-Confirm</span></span>
<span data-ttu-id="b9287-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9287-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9287-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9287-130">-WhatIf</span></span>
<span data-ttu-id="b9287-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9287-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9287-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9287-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9287-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9287-133">CommonParameters</span></span>
<span data-ttu-id="b9287-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9287-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9287-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9287-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9287-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9287-136">INPUTS</span></span>

### <span data-ttu-id="b9287-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9287-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b9287-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b9287-138">System.String</span></span>

## <span data-ttu-id="b9287-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9287-139">OUTPUTS</span></span>

### <span data-ttu-id="b9287-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b9287-140">System.Void</span></span>

## <span data-ttu-id="b9287-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9287-141">NOTES</span></span>

## <span data-ttu-id="b9287-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9287-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9287-143">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="b9287-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="b9287-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9287-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


