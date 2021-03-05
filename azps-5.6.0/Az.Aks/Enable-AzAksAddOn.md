---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 1280f65659f986d0fd8402da0d3db5b1c5a92b58
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966957"
---
# <span data-ttu-id="8e369-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="8e369-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="8e369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e369-102">SYNOPSIS</span></span>
<span data-ttu-id="8e369-103">Abilita i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="8e369-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="8e369-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e369-104">SYNTAX</span></span>

### <span data-ttu-id="8e369-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8e369-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e369-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e369-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e369-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e369-107">DESCRIPTION</span></span>
<span data-ttu-id="8e369-108">Abilita i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="8e369-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="8e369-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e369-109">EXAMPLES</span></span>

### <span data-ttu-id="8e369-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e369-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="8e369-111">Abilita i componenti `HttpApplicationRouting` `Monitoring` `AzurePolicy` aggiuntivi, , e `VirtualNode` per gli `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="8e369-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="8e369-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e369-112">PARAMETERS</span></span>

### <span data-ttu-id="8e369-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8e369-113">-ClusterName</span></span>
<span data-ttu-id="8e369-114">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8e369-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e369-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="8e369-115">-ClusterObject</span></span>
<span data-ttu-id="8e369-116">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e369-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e369-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e369-117">-DefaultProfile</span></span>
<span data-ttu-id="8e369-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e369-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e369-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e369-119">-Name</span></span>
<span data-ttu-id="8e369-120">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8e369-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e369-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e369-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e369-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e369-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e369-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8e369-123">-SubnetName</span></span>
<span data-ttu-id="8e369-124">Nome subnet di VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="8e369-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e369-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8e369-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="8e369-126">ID risorsa dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8e369-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e369-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e369-127">-Confirm</span></span>
<span data-ttu-id="8e369-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e369-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e369-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e369-129">-WhatIf</span></span>
<span data-ttu-id="8e369-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e369-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e369-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e369-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e369-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e369-132">CommonParameters</span></span>
<span data-ttu-id="8e369-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e369-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e369-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e369-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e369-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e369-135">INPUTS</span></span>

### <span data-ttu-id="8e369-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8e369-136">System.String</span></span>

### <span data-ttu-id="8e369-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8e369-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="8e369-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e369-138">OUTPUTS</span></span>

### <span data-ttu-id="8e369-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8e369-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="8e369-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e369-140">NOTES</span></span>

## <span data-ttu-id="8e369-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e369-141">RELATED LINKS</span></span>
