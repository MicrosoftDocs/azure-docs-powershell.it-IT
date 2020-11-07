---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 92ef4802ce842fa88389da19f1b5ba1aacf84b3e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677809"
---
# <span data-ttu-id="1e55c-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1e55c-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="1e55c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e55c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e55c-103">Raccogliere i log dall'applicazione Application-Insights specificata.</span><span class="sxs-lookup"><span data-stu-id="1e55c-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="1e55c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e55c-104">SYNTAX</span></span>

### <span data-ttu-id="1e55c-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e55c-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e55c-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="1e55c-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e55c-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="1e55c-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e55c-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="1e55c-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e55c-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="1e55c-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e55c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e55c-110">DESCRIPTION</span></span>
<span data-ttu-id="1e55c-111">Il cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** consente di abilitare la raccolta di log da una determinata applicazione Application-Insights.</span><span class="sxs-lookup"><span data-stu-id="1e55c-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="1e55c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e55c-112">EXAMPLES</span></span>

### <span data-ttu-id="1e55c-113">Esempio 1: creare un'origine dati dell'applicazione-Insights nell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1e55c-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="1e55c-114">Questo comando crea un'origine dati Application-Insights di una determinata applicazione in un workpsace di analisi del log specifico.</span><span class="sxs-lookup"><span data-stu-id="1e55c-114">This command creates an application-insights data source of a given application in a given log analytics workpsace.</span></span> <span data-ttu-id="1e55c-115">In questo modo, la raccolta di log da un'applicazione specificata alla workpsace analisi log.</span><span class="sxs-lookup"><span data-stu-id="1e55c-115">This enables the collection of logs from given application to the log analytics workpsace.</span></span>

### <span data-ttu-id="1e55c-116">Esempio 2: ottenere l'oggetto Workspace e creare un'origine dati dell'applicazione-Insights dall'ID delle risorse dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1e55c-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="1e55c-117">Questo comando illustra come ottenere un oggetto area di lavoro analisi log e quindi passare l'output per creare un'origine dati dell'applicazione associata-Insights dall'ID risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e55c-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="1e55c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e55c-118">PARAMETERS</span></span>

### <span data-ttu-id="1e55c-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1e55c-119">-ApplicationName</span></span>
<span data-ttu-id="1e55c-120">Nome dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="1e55c-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="1e55c-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e55c-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="1e55c-122">Nome del gruppo di risorse dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="1e55c-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="1e55c-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="1e55c-123">-ApplicationResourceId</span></span>
<span data-ttu-id="1e55c-124">ID risorsa applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="1e55c-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="1e55c-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e55c-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="1e55c-126">ID sottoscrizione dell'applicazione collegata.</span><span class="sxs-lookup"><span data-stu-id="1e55c-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="1e55c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e55c-127">-DefaultProfile</span></span>
<span data-ttu-id="1e55c-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e55c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e55c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="1e55c-129">-Force</span></span>
<span data-ttu-id="1e55c-130">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1e55c-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1e55c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e55c-131">-ResourceGroupName</span></span>
<span data-ttu-id="1e55c-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e55c-132">The resource group name.</span></span>

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

### <span data-ttu-id="1e55c-133">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1e55c-133">-Workspace</span></span>
<span data-ttu-id="1e55c-134">Area di lavoro che conterrà l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="1e55c-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="1e55c-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e55c-135">-WorkspaceName</span></span>
<span data-ttu-id="1e55c-136">Nome dell'area di lavoro che conterrà l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="1e55c-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="1e55c-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e55c-137">-Confirm</span></span>
<span data-ttu-id="1e55c-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e55c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e55c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e55c-139">-WhatIf</span></span>
<span data-ttu-id="1e55c-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e55c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e55c-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e55c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e55c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e55c-142">CommonParameters</span></span>
<span data-ttu-id="1e55c-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e55c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e55c-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e55c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e55c-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e55c-145">INPUTS</span></span>

### <span data-ttu-id="1e55c-146">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e55c-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1e55c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1e55c-147">System.String</span></span>

## <span data-ttu-id="1e55c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e55c-148">OUTPUTS</span></span>

### <span data-ttu-id="1e55c-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1e55c-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1e55c-150">Note</span><span class="sxs-lookup"><span data-stu-id="1e55c-150">NOTES</span></span>

## <span data-ttu-id="1e55c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e55c-151">RELATED LINKS</span></span>