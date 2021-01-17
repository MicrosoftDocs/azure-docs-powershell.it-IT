---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479132"
---
# <span data-ttu-id="52dbe-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="52dbe-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="52dbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="52dbe-103">Disabilitare l'addons per AKS.</span><span class="sxs-lookup"><span data-stu-id="52dbe-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="52dbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52dbe-104">SYNTAX</span></span>

### <span data-ttu-id="52dbe-105">defaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52dbe-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52dbe-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52dbe-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52dbe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52dbe-107">DESCRIPTION</span></span>
<span data-ttu-id="52dbe-108">Disabilitare l'addons per AKS.</span><span class="sxs-lookup"><span data-stu-id="52dbe-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="52dbe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52dbe-109">EXAMPLES</span></span>

### <span data-ttu-id="52dbe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52dbe-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="52dbe-111">Disabilitare l'addons `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` e `KubeDashboard` per AKS.</span><span class="sxs-lookup"><span data-stu-id="52dbe-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="52dbe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52dbe-112">PARAMETERS</span></span>

### <span data-ttu-id="52dbe-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="52dbe-113">-ClusterName</span></span>
<span data-ttu-id="52dbe-114">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="52dbe-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="52dbe-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="52dbe-115">-ClusterObject</span></span>
<span data-ttu-id="52dbe-116">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="52dbe-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="52dbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52dbe-117">-DefaultProfile</span></span>
<span data-ttu-id="52dbe-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52dbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52dbe-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="52dbe-119">-Name</span></span>
<span data-ttu-id="52dbe-120">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="52dbe-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="52dbe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52dbe-121">-ResourceGroupName</span></span>
<span data-ttu-id="52dbe-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52dbe-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="52dbe-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52dbe-123">-Confirm</span></span>
<span data-ttu-id="52dbe-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52dbe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52dbe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52dbe-125">-WhatIf</span></span>
<span data-ttu-id="52dbe-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52dbe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52dbe-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52dbe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52dbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52dbe-128">CommonParameters</span></span>
<span data-ttu-id="52dbe-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52dbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52dbe-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52dbe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52dbe-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52dbe-131">INPUTS</span></span>

### <span data-ttu-id="52dbe-132">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="52dbe-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="52dbe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52dbe-133">System.String</span></span>

## <span data-ttu-id="52dbe-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52dbe-134">OUTPUTS</span></span>

### <span data-ttu-id="52dbe-135">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="52dbe-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="52dbe-136">Note</span><span class="sxs-lookup"><span data-stu-id="52dbe-136">NOTES</span></span>

## <span data-ttu-id="52dbe-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52dbe-137">RELATED LINKS</span></span>
