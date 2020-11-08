---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201360"
---
# <span data-ttu-id="6ffac-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="6ffac-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="6ffac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ffac-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffac-103">Abilitare l'addons per AKS.</span><span class="sxs-lookup"><span data-stu-id="6ffac-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="6ffac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ffac-104">SYNTAX</span></span>

### <span data-ttu-id="6ffac-105">defaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ffac-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ffac-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffac-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ffac-107">DESCRIPTION</span></span>
<span data-ttu-id="6ffac-108">Abilitare l'addons per AKS.</span><span class="sxs-lookup"><span data-stu-id="6ffac-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="6ffac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ffac-109">EXAMPLES</span></span>

### <span data-ttu-id="6ffac-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ffac-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="6ffac-111">Abilitare l'addons `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` `VirtualNode` e `KubeDashboard` per AKS.</span><span class="sxs-lookup"><span data-stu-id="6ffac-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="6ffac-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ffac-112">PARAMETERS</span></span>

### <span data-ttu-id="6ffac-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6ffac-113">-ClusterName</span></span>
<span data-ttu-id="6ffac-114">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6ffac-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="6ffac-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="6ffac-115">-ClusterObject</span></span>
<span data-ttu-id="6ffac-116">Un oggetto PSKubernetesCluster, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ffac-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ffac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffac-117">-DefaultProfile</span></span>
<span data-ttu-id="6ffac-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffac-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ffac-119">-Name</span></span>
<span data-ttu-id="6ffac-120">Nome del cluster gestito Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6ffac-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="6ffac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffac-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ffac-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ffac-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ffac-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6ffac-123">-SubnetName</span></span>
<span data-ttu-id="6ffac-124">Nome subnet di VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="6ffac-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="6ffac-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffac-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="6ffac-126">ID risorsa dell'area di lavoro di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6ffac-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="6ffac-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ffac-127">-Confirm</span></span>
<span data-ttu-id="6ffac-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffac-129">-WhatIf</span></span>
<span data-ttu-id="6ffac-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ffac-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ffac-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ffac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffac-132">CommonParameters</span></span>
<span data-ttu-id="6ffac-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffac-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ffac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffac-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ffac-135">INPUTS</span></span>

### <span data-ttu-id="6ffac-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffac-136">System.String</span></span>

### <span data-ttu-id="6ffac-137">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6ffac-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="6ffac-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ffac-138">OUTPUTS</span></span>

### <span data-ttu-id="6ffac-139">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6ffac-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="6ffac-140">Note</span><span class="sxs-lookup"><span data-stu-id="6ffac-140">NOTES</span></span>

## <span data-ttu-id="6ffac-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ffac-141">RELATED LINKS</span></span>
