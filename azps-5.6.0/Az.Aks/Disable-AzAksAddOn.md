---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 5d0cc543d5ec893ecb1f83b8fd62f25bcb32f5b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966973"
---
# <span data-ttu-id="176e0-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="176e0-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="176e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176e0-102">SYNOPSIS</span></span>
<span data-ttu-id="176e0-103">Disabilitare i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="176e0-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="176e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="176e0-104">SYNTAX</span></span>

### <span data-ttu-id="176e0-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="176e0-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176e0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="176e0-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176e0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="176e0-107">DESCRIPTION</span></span>
<span data-ttu-id="176e0-108">Disabilitare i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="176e0-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="176e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="176e0-109">EXAMPLES</span></span>

### <span data-ttu-id="176e0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="176e0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="176e0-111">Disabilitare i `HttpApplicationRouting` componenti `Monitoring` `AzurePolicy` aggiuntivi, , e per gli `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="176e0-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="176e0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176e0-112">PARAMETERS</span></span>

### <span data-ttu-id="176e0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="176e0-113">-ClusterName</span></span>
<span data-ttu-id="176e0-114">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="176e0-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="176e0-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="176e0-115">-ClusterObject</span></span>
<span data-ttu-id="176e0-116">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="176e0-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="176e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176e0-117">-DefaultProfile</span></span>
<span data-ttu-id="176e0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="176e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176e0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="176e0-119">-Name</span></span>
<span data-ttu-id="176e0-120">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="176e0-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="176e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="176e0-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="176e0-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="176e0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="176e0-123">-Confirm</span></span>
<span data-ttu-id="176e0-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176e0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176e0-125">-WhatIf</span></span>
<span data-ttu-id="176e0-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="176e0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176e0-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="176e0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176e0-128">CommonParameters</span></span>
<span data-ttu-id="176e0-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176e0-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="176e0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176e0-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="176e0-131">INPUTS</span></span>

### <span data-ttu-id="176e0-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="176e0-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="176e0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="176e0-133">System.String</span></span>

## <span data-ttu-id="176e0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="176e0-134">OUTPUTS</span></span>

### <span data-ttu-id="176e0-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="176e0-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="176e0-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="176e0-136">NOTES</span></span>

## <span data-ttu-id="176e0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="176e0-137">RELATED LINKS</span></span>
