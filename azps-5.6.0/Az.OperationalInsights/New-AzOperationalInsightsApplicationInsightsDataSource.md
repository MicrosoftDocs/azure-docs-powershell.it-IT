---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 21de9e423134c78302adf5c172dee0869b9501bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011805"
---
# <span data-ttu-id="05369-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="05369-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="05369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05369-102">SYNOPSIS</span></span>
<span data-ttu-id="05369-103">Raccogliere log da un'applicazione Application-Insights specifica.</span><span class="sxs-lookup"><span data-stu-id="05369-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="05369-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05369-104">SYNTAX</span></span>

### <span data-ttu-id="05369-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05369-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05369-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="05369-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05369-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="05369-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05369-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="05369-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05369-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="05369-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05369-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05369-110">DESCRIPTION</span></span>
<span data-ttu-id="05369-111">Il cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** abilita la raccolta di log da un'applicazione Application-Insights specifica.</span><span class="sxs-lookup"><span data-stu-id="05369-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="05369-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05369-112">EXAMPLES</span></span>

### <span data-ttu-id="05369-113">Esempio 1: Creare un'origine dati application-insights nell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="05369-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="05369-114">Questo comando crea un'origine dati application-insights di una determinata applicazione in una determinata area di lavoro di analisi del log.</span><span class="sxs-lookup"><span data-stu-id="05369-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="05369-115">In questo modo, la raccolta di log da una determinata applicazione viene abilitata nell'area di lavoro di analisi dei log.</span><span class="sxs-lookup"><span data-stu-id="05369-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="05369-116">Esempio 2: ottenere l'oggetto area di lavoro e creare l'origine dati application-insights in base all'ID risorsa dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="05369-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="05369-117">Questo comando mostra come ottenere un oggetto area di lavoro analisi log e quindi passare l'output per creare un'origine dati application-insights associata dall'ID di risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05369-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="05369-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05369-118">PARAMETERS</span></span>

### <span data-ttu-id="05369-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="05369-119">-ApplicationName</span></span>
<span data-ttu-id="05369-120">Nome dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="05369-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05369-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="05369-122">Nome del gruppo di risorse dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="05369-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="05369-123">-ApplicationResourceId</span></span>
<span data-ttu-id="05369-124">ID della risorsa dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="05369-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05369-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="05369-126">ID sottoscrizione dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="05369-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05369-127">-DefaultProfile</span></span>
<span data-ttu-id="05369-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05369-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05369-129">-Force</span><span class="sxs-lookup"><span data-stu-id="05369-129">-Force</span></span>
<span data-ttu-id="05369-130">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="05369-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="05369-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05369-131">-ResourceGroupName</span></span>
<span data-ttu-id="05369-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05369-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-133">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="05369-133">-Workspace</span></span>
<span data-ttu-id="05369-134">L'area di lavoro che conterrà l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="05369-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05369-135">-WorkspaceName</span></span>
<span data-ttu-id="05369-136">Nome dell'area di lavoro che conterrà l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="05369-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05369-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05369-137">-Confirm</span></span>
<span data-ttu-id="05369-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05369-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05369-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05369-139">-WhatIf</span></span>
<span data-ttu-id="05369-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05369-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05369-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05369-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05369-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05369-142">CommonParameters</span></span>
<span data-ttu-id="05369-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05369-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05369-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05369-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05369-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="05369-145">INPUTS</span></span>

### <span data-ttu-id="05369-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="05369-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="05369-147">System.String</span><span class="sxs-lookup"><span data-stu-id="05369-147">System.String</span></span>

## <span data-ttu-id="05369-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05369-148">OUTPUTS</span></span>

### <span data-ttu-id="05369-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="05369-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="05369-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="05369-150">NOTES</span></span>

## <span data-ttu-id="05369-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05369-151">RELATED LINKS</span></span>
