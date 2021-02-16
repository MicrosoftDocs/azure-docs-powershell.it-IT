---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186710"
---
# <span data-ttu-id="98db0-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="98db0-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="98db0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98db0-102">SYNOPSIS</span></span>
<span data-ttu-id="98db0-103">Servizio di collegamento per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="98db0-103">link service for workspace</span></span>

## <span data-ttu-id="98db0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98db0-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98db0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98db0-105">DESCRIPTION</span></span>
<span data-ttu-id="98db0-106">Servizio di collegamento per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="98db0-106">link service for workspace</span></span>

## <span data-ttu-id="98db0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98db0-107">EXAMPLES</span></span>

### <span data-ttu-id="98db0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98db0-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="98db0-109">Cluster di collegamenti per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="98db0-109">link cluster for workspace</span></span>

## <span data-ttu-id="98db0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98db0-110">PARAMETERS</span></span>

### <span data-ttu-id="98db0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98db0-111">-AsJob</span></span>
<span data-ttu-id="98db0-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="98db0-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98db0-113">-DefaultProfile</span></span>
<span data-ttu-id="98db0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98db0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="98db0-115">-LinkedServiceName</span></span>
<span data-ttu-id="98db0-116">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="98db0-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98db0-117">-ResourceGroupName</span></span>
<span data-ttu-id="98db0-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="98db0-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98db0-119">-ResourceId</span></span>
<span data-ttu-id="98db0-120">ID risorsa della risorsa che verrà collegata all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="98db0-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="98db0-121">Deve essere usato per collegare risorse che richiedono l'accesso in lettura</span><span class="sxs-lookup"><span data-stu-id="98db0-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="98db0-122">-Tags</span></span>
<span data-ttu-id="98db0-123">Tag.</span><span class="sxs-lookup"><span data-stu-id="98db0-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98db0-124">-WorkspaceName</span></span>
<span data-ttu-id="98db0-125">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="98db0-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="98db0-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="98db0-127">ID risorsa della risorsa che verrà collegata all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="98db0-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="98db0-128">Deve essere usato per collegare risorse che richiedono l'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="98db0-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="98db0-129">Il cluster deve avere lo stato di provisioning "Succeeded" e le proprietà keyvault valide.</span><span class="sxs-lookup"><span data-stu-id="98db0-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98db0-130">-Confirm</span></span>
<span data-ttu-id="98db0-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98db0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98db0-132">-WhatIf</span></span>
<span data-ttu-id="98db0-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98db0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98db0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98db0-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98db0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98db0-135">CommonParameters</span></span>
<span data-ttu-id="98db0-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98db0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98db0-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98db0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98db0-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="98db0-138">INPUTS</span></span>

### <span data-ttu-id="98db0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="98db0-139">System.String</span></span>

## <span data-ttu-id="98db0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98db0-140">OUTPUTS</span></span>

### <span data-ttu-id="98db0-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="98db0-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="98db0-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="98db0-142">NOTES</span></span>

## <span data-ttu-id="98db0-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98db0-143">RELATED LINKS</span></span>
