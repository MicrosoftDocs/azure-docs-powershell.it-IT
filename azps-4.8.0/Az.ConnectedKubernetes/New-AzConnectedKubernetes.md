---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033239"
---
# <span data-ttu-id="40ef0-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="40ef0-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="40ef0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="40ef0-103">API per registrare un nuovo cluster di K8s e quindi creare una risorsa rilevata in ARM</span><span class="sxs-lookup"><span data-stu-id="40ef0-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="40ef0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40ef0-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40ef0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="40ef0-106">API per registrare un nuovo cluster di K8s e quindi creare una risorsa rilevata in ARM</span><span class="sxs-lookup"><span data-stu-id="40ef0-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="40ef0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40ef0-107">EXAMPLES</span></span>

### <span data-ttu-id="40ef0-108">Esempio 1: creare un kubernetes connesso</span><span class="sxs-lookup"><span data-stu-id="40ef0-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="40ef0-109">Questo comando crea un kubernetes connesso.</span><span class="sxs-lookup"><span data-stu-id="40ef0-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="40ef0-110">Esempio 1: creare un kubernetes connesso con i parametri kubeConfig e kubeContext</span><span class="sxs-lookup"><span data-stu-id="40ef0-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="40ef0-111">Questo comando crea un kubernetes connesso con i parametri kubeConfig e kubeContext.</span><span class="sxs-lookup"><span data-stu-id="40ef0-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="40ef0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40ef0-112">PARAMETERS</span></span>

### <span data-ttu-id="40ef0-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="40ef0-113">-ClusterName</span></span>
<span data-ttu-id="40ef0-114">Nome del cluster Kubernetes in cui viene chiamato Get.</span><span class="sxs-lookup"><span data-stu-id="40ef0-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="40ef0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ef0-115">-DefaultProfile</span></span>
<span data-ttu-id="40ef0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40ef0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ef0-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="40ef0-117">-KubeConfig</span></span>
<span data-ttu-id="40ef0-118">Percorso del file di configurazione Kube</span><span class="sxs-lookup"><span data-stu-id="40ef0-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="40ef0-119">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="40ef0-119">-KubeContext</span></span>
<span data-ttu-id="40ef0-120">Contesto Kubconfig dal computer corrente</span><span class="sxs-lookup"><span data-stu-id="40ef0-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="40ef0-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="40ef0-121">-Location</span></span>
<span data-ttu-id="40ef0-122">Posizione del cluster</span><span class="sxs-lookup"><span data-stu-id="40ef0-122">Location of the cluster</span></span>

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

### <span data-ttu-id="40ef0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ef0-123">-ResourceGroupName</span></span>
<span data-ttu-id="40ef0-124">Nome del gruppo di risorse a cui è registrato il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="40ef0-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="40ef0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40ef0-125">-SubscriptionId</span></span>
<span data-ttu-id="40ef0-126">ID dell'abbonamento a cui è registrato il cluster kubernetes.</span><span class="sxs-lookup"><span data-stu-id="40ef0-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="40ef0-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40ef0-127">-Confirm</span></span>
<span data-ttu-id="40ef0-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ef0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ef0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ef0-129">-WhatIf</span></span>
<span data-ttu-id="40ef0-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40ef0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ef0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40ef0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ef0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ef0-132">CommonParameters</span></span>
<span data-ttu-id="40ef0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ef0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ef0-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40ef0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ef0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40ef0-135">INPUTS</span></span>

## <span data-ttu-id="40ef0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40ef0-136">OUTPUTS</span></span>

### <span data-ttu-id="40ef0-137">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="40ef0-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="40ef0-138">Note</span><span class="sxs-lookup"><span data-stu-id="40ef0-138">NOTES</span></span>

<span data-ttu-id="40ef0-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="40ef0-139">ALIASES</span></span>

## <span data-ttu-id="40ef0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40ef0-140">RELATED LINKS</span></span>

