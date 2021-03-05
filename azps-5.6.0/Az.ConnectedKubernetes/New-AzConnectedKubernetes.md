---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: f6610b86f96602619f12323e7300c66ed39a9f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012509"
---
# <span data-ttu-id="6b4e1-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="6b4e1-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="6b4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4e1-103">API per registrare un nuovo cluster K8s e quindi creare una risorsa tracciata in ARM</span><span class="sxs-lookup"><span data-stu-id="6b4e1-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="6b4e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b4e1-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b4e1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6b4e1-105">DESCRIPTION</span></span>
<span data-ttu-id="6b4e1-106">API per registrare un nuovo cluster K8s e quindi creare una risorsa tracciata in ARM</span><span class="sxs-lookup"><span data-stu-id="6b4e1-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="6b4e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b4e1-107">EXAMPLES</span></span>

### <span data-ttu-id="6b4e1-108">Esempio 1: Creare un kubernet connesso</span><span class="sxs-lookup"><span data-stu-id="6b4e1-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6b4e1-109">Questo comando crea un kubernet connesso.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="6b4e1-110">Esempio 1: Creare un kubernet connesso con i parametri kubeConfig e kubeContext</span><span class="sxs-lookup"><span data-stu-id="6b4e1-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6b4e1-111">Questo comando crea un kubernetes connesso con i parametri kubeConfig e kubeContext.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="6b4e1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b4e1-112">PARAMETERS</span></span>

### <span data-ttu-id="6b4e1-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6b4e1-113">-ClusterName</span></span>
<span data-ttu-id="6b4e1-114">Il nome del cluster Kubernetes su cui si chiama get.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b4e1-115">-DefaultProfile</span></span>
<span data-ttu-id="6b4e1-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="6b4e1-117">-KubeConfig</span></span>
<span data-ttu-id="6b4e1-118">Percorso del file di configurazione del kube</span><span class="sxs-lookup"><span data-stu-id="6b4e1-118">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="6b4e1-119">-KubeContext</span></span>
<span data-ttu-id="6b4e1-120">Contesto Kubconfig dal computer corrente</span><span class="sxs-lookup"><span data-stu-id="6b4e1-120">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-121">-Location</span><span class="sxs-lookup"><span data-stu-id="6b4e1-121">-Location</span></span>
<span data-ttu-id="6b4e1-122">Posizione del cluster</span><span class="sxs-lookup"><span data-stu-id="6b4e1-122">Location of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b4e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b4e1-124">Nome del gruppo di risorse in cui è registrato il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b4e1-125">-SubscriptionId</span></span>
<span data-ttu-id="6b4e1-126">ID della sottoscrizione in cui è registrato il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4e1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b4e1-127">-Confirm</span></span>
<span data-ttu-id="6b4e1-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b4e1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b4e1-129">-WhatIf</span></span>
<span data-ttu-id="6b4e1-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b4e1-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b4e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4e1-132">CommonParameters</span></span>
<span data-ttu-id="6b4e1-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4e1-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b4e1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4e1-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="6b4e1-135">INPUTS</span></span>

## <span data-ttu-id="6b4e1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b4e1-136">OUTPUTS</span></span>

### <span data-ttu-id="6b4e1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="6b4e1-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="6b4e1-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="6b4e1-138">NOTES</span></span>

<span data-ttu-id="6b4e1-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6b4e1-139">ALIASES</span></span>

## <span data-ttu-id="6b4e1-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b4e1-140">RELATED LINKS</span></span>

