---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348139"
---
# <span data-ttu-id="add2e-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="add2e-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="add2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="add2e-102">SYNOPSIS</span></span>
<span data-ttu-id="add2e-103">collegamento al servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="add2e-103">link service for workspace</span></span>

## <span data-ttu-id="add2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="add2e-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add2e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="add2e-105">DESCRIPTION</span></span>
<span data-ttu-id="add2e-106">collegamento al servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="add2e-106">link service for workspace</span></span>

## <span data-ttu-id="add2e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="add2e-107">EXAMPLES</span></span>

### <span data-ttu-id="add2e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="add2e-108">Example 1</span></span>
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

<span data-ttu-id="add2e-109">collegamento del cluster per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="add2e-109">link cluster for workspace</span></span>

## <span data-ttu-id="add2e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="add2e-110">PARAMETERS</span></span>

### <span data-ttu-id="add2e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="add2e-111">-AsJob</span></span>
<span data-ttu-id="add2e-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="add2e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="add2e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add2e-113">-DefaultProfile</span></span>
<span data-ttu-id="add2e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="add2e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="add2e-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="add2e-115">-LinkedServiceName</span></span>
<span data-ttu-id="add2e-116">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="add2e-116">The Workspace name.</span></span>

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

### <span data-ttu-id="add2e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add2e-117">-ResourceGroupName</span></span>
<span data-ttu-id="add2e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="add2e-118">The resource group name.</span></span>

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

### <span data-ttu-id="add2e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="add2e-119">-ResourceId</span></span>
<span data-ttu-id="add2e-120">ID risorsa della risorsa che verrà collegata all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="add2e-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="add2e-121">Questa operazione deve essere usata per collegare risorse che richiedono l'accesso in lettura</span><span class="sxs-lookup"><span data-stu-id="add2e-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="add2e-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="add2e-122">-Tags</span></span>
<span data-ttu-id="add2e-123">Tag.</span><span class="sxs-lookup"><span data-stu-id="add2e-123">Tags.</span></span>

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

### <span data-ttu-id="add2e-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="add2e-124">-WorkspaceName</span></span>
<span data-ttu-id="add2e-125">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="add2e-125">The Workspace name.</span></span>

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

### <span data-ttu-id="add2e-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="add2e-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="add2e-127">ID risorsa della risorsa che verrà collegata all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="add2e-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="add2e-128">Questa operazione deve essere usata per collegare le risorse che richiedono l'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="add2e-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="add2e-129">Il cluster deve avere lo stato di provisioning "succeeded" e le proprietà di un Vault valido.</span><span class="sxs-lookup"><span data-stu-id="add2e-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="add2e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="add2e-130">-Confirm</span></span>
<span data-ttu-id="add2e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="add2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="add2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add2e-132">-WhatIf</span></span>
<span data-ttu-id="add2e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="add2e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="add2e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="add2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="add2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add2e-135">CommonParameters</span></span>
<span data-ttu-id="add2e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add2e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="add2e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add2e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="add2e-138">INPUTS</span></span>

### <span data-ttu-id="add2e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="add2e-139">System.String</span></span>

## <span data-ttu-id="add2e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="add2e-140">OUTPUTS</span></span>

### <span data-ttu-id="add2e-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="add2e-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="add2e-142">Note</span><span class="sxs-lookup"><span data-stu-id="add2e-142">NOTES</span></span>

## <span data-ttu-id="add2e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="add2e-143">RELATED LINKS</span></span>
