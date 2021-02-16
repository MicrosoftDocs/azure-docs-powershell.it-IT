---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 616695e60d945e545cfbb8c1b2fb7ba81ae9caa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190399"
---
# <span data-ttu-id="941a2-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="941a2-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="941a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="941a2-102">SYNOPSIS</span></span>
<span data-ttu-id="941a2-103">Disabilitare i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="941a2-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="941a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="941a2-104">SYNTAX</span></span>

### <span data-ttu-id="941a2-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="941a2-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="941a2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="941a2-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="941a2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="941a2-107">DESCRIPTION</span></span>
<span data-ttu-id="941a2-108">Disabilitare i componenti aggiuntivi per gli aks.</span><span class="sxs-lookup"><span data-stu-id="941a2-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="941a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="941a2-109">EXAMPLES</span></span>

### <span data-ttu-id="941a2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="941a2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="941a2-111">Disabilitare i `HttpApplicationRouting` componenti `Monitoring` `AzurePolicy` aggiuntivi, , e per gli `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="941a2-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="941a2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="941a2-112">PARAMETERS</span></span>

### <span data-ttu-id="941a2-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="941a2-113">-ClusterName</span></span>
<span data-ttu-id="941a2-114">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="941a2-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="941a2-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="941a2-115">-ClusterObject</span></span>
<span data-ttu-id="941a2-116">Oggetto PSKubernetesCluster, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="941a2-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="941a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941a2-117">-DefaultProfile</span></span>
<span data-ttu-id="941a2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="941a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="941a2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="941a2-119">-Name</span></span>
<span data-ttu-id="941a2-120">Nome cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="941a2-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="941a2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="941a2-121">-ResourceGroupName</span></span>
<span data-ttu-id="941a2-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="941a2-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="941a2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="941a2-123">-Confirm</span></span>
<span data-ttu-id="941a2-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="941a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="941a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="941a2-125">-WhatIf</span></span>
<span data-ttu-id="941a2-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="941a2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="941a2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="941a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="941a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941a2-128">CommonParameters</span></span>
<span data-ttu-id="941a2-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941a2-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="941a2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941a2-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="941a2-131">INPUTS</span></span>

### <span data-ttu-id="941a2-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="941a2-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="941a2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="941a2-133">System.String</span></span>

## <span data-ttu-id="941a2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="941a2-134">OUTPUTS</span></span>

### <span data-ttu-id="941a2-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="941a2-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="941a2-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="941a2-136">NOTES</span></span>

## <span data-ttu-id="941a2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="941a2-137">RELATED LINKS</span></span>
