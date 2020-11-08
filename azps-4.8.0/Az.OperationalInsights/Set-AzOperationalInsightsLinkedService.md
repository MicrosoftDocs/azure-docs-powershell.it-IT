---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032265"
---
# <span data-ttu-id="03fa8-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="03fa8-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="03fa8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="03fa8-103">collegamento al servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="03fa8-103">link service for workspace</span></span>

## <span data-ttu-id="03fa8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03fa8-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03fa8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="03fa8-106">collegamento al servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="03fa8-106">link service for workspace</span></span>

## <span data-ttu-id="03fa8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="03fa8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03fa8-108">Example 1</span></span>
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

<span data-ttu-id="03fa8-109">collegamento del cluster per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="03fa8-109">link cluster for workspace</span></span>

## <span data-ttu-id="03fa8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="03fa8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03fa8-111">-AsJob</span></span>
<span data-ttu-id="03fa8-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="03fa8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03fa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fa8-113">-DefaultProfile</span></span>
<span data-ttu-id="03fa8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03fa8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fa8-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="03fa8-115">-LinkedServiceName</span></span>
<span data-ttu-id="03fa8-116">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03fa8-116">The Workspace name.</span></span>

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

### <span data-ttu-id="03fa8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fa8-117">-ResourceGroupName</span></span>
<span data-ttu-id="03fa8-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03fa8-118">The resource group name.</span></span>

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

### <span data-ttu-id="03fa8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03fa8-119">-ResourceId</span></span>
<span data-ttu-id="03fa8-120">ID risorsa della risorsa che verrà collegata all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03fa8-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="03fa8-121">Questa operazione deve essere usata per collegare risorse che richiedono l'accesso in lettura</span><span class="sxs-lookup"><span data-stu-id="03fa8-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="03fa8-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="03fa8-122">-Tags</span></span>
<span data-ttu-id="03fa8-123">Tag.</span><span class="sxs-lookup"><span data-stu-id="03fa8-123">Tags.</span></span>

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

### <span data-ttu-id="03fa8-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03fa8-124">-WorkspaceName</span></span>
<span data-ttu-id="03fa8-125">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03fa8-125">The Workspace name.</span></span>

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

### <span data-ttu-id="03fa8-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="03fa8-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="03fa8-127">ID risorsa della risorsa che verrà collegata all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03fa8-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="03fa8-128">Questa operazione deve essere usata per collegare le risorse che richiedono l'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="03fa8-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="03fa8-129">Il cluster deve avere lo stato di provisioning "succeeded" e le proprietà di un Vault valido.</span><span class="sxs-lookup"><span data-stu-id="03fa8-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="03fa8-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03fa8-130">-Confirm</span></span>
<span data-ttu-id="03fa8-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03fa8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fa8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fa8-132">-WhatIf</span></span>
<span data-ttu-id="03fa8-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03fa8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fa8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03fa8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fa8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fa8-135">CommonParameters</span></span>
<span data-ttu-id="03fa8-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fa8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fa8-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03fa8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fa8-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03fa8-138">INPUTS</span></span>

### <span data-ttu-id="03fa8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="03fa8-139">System.String</span></span>

## <span data-ttu-id="03fa8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03fa8-140">OUTPUTS</span></span>

### <span data-ttu-id="03fa8-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="03fa8-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="03fa8-142">Note</span><span class="sxs-lookup"><span data-stu-id="03fa8-142">NOTES</span></span>

## <span data-ttu-id="03fa8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03fa8-143">RELATED LINKS</span></span>
