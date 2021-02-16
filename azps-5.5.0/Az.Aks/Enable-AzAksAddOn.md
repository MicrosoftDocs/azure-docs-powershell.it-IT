---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 40fb9f328f0f838f5d76de6de5509c74b0002768
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199910"
---
# <span data-ttu-id="bc2d0-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="bc2d0-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="bc2d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2d0-103">Abilita i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="bc2d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc2d0-104">SYNTAX</span></span>

### <span data-ttu-id="bc2d0-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="bc2d0-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc2d0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc2d0-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc2d0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc2d0-107">DESCRIPTION</span></span>
<span data-ttu-id="bc2d0-108">Abilita i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="bc2d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc2d0-109">EXAMPLES</span></span>

### <span data-ttu-id="bc2d0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc2d0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="bc2d0-111">Abilita i componenti `HttpApplicationRouting` `Monitoring` `AzurePolicy` aggiuntivi, , e `VirtualNode` per gli `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="bc2d0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc2d0-112">PARAMETERS</span></span>

### <span data-ttu-id="bc2d0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bc2d0-113">-ClusterName</span></span>
<span data-ttu-id="bc2d0-114">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="bc2d0-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="bc2d0-115">-ClusterObject</span></span>
<span data-ttu-id="bc2d0-116">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="bc2d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2d0-117">-DefaultProfile</span></span>
<span data-ttu-id="bc2d0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc2d0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bc2d0-119">-Name</span></span>
<span data-ttu-id="bc2d0-120">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="bc2d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc2d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="bc2d0-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="bc2d0-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bc2d0-123">-SubnetName</span></span>
<span data-ttu-id="bc2d0-124">Nome subnet di VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="bc2d0-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="bc2d0-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="bc2d0-126">ID risorsa dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="bc2d0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc2d0-127">-Confirm</span></span>
<span data-ttu-id="bc2d0-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc2d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc2d0-129">-WhatIf</span></span>
<span data-ttu-id="bc2d0-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc2d0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc2d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2d0-132">CommonParameters</span></span>
<span data-ttu-id="bc2d0-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2d0-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2d0-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc2d0-135">INPUTS</span></span>

### <span data-ttu-id="bc2d0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bc2d0-136">System.String</span></span>

### <span data-ttu-id="bc2d0-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="bc2d0-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="bc2d0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc2d0-138">OUTPUTS</span></span>

### <span data-ttu-id="bc2d0-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="bc2d0-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="bc2d0-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc2d0-140">NOTES</span></span>

## <span data-ttu-id="bc2d0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc2d0-141">RELATED LINKS</span></span>
