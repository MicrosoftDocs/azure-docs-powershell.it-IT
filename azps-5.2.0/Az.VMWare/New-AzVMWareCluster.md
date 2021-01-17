---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335068"
---
# <span data-ttu-id="1409d-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="1409d-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="1409d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1409d-102">SYNOPSIS</span></span>
<span data-ttu-id="1409d-103">Creare o aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="1409d-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="1409d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1409d-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1409d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1409d-105">DESCRIPTION</span></span>
<span data-ttu-id="1409d-106">Creare o aggiornare un cluster in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="1409d-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="1409d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1409d-107">EXAMPLES</span></span>

### <span data-ttu-id="1409d-108">Esempio 1: creare un cluster</span><span class="sxs-lookup"><span data-stu-id="1409d-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="1409d-109">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="1409d-109">Create cluster</span></span>

## <span data-ttu-id="1409d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1409d-110">PARAMETERS</span></span>

### <span data-ttu-id="1409d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1409d-111">-AsJob</span></span>
<span data-ttu-id="1409d-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1409d-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1409d-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="1409d-113">-ClusterSize</span></span>
<span data-ttu-id="1409d-114">Dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="1409d-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1409d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1409d-115">-DefaultProfile</span></span>
<span data-ttu-id="1409d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1409d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1409d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1409d-117">-Name</span></span>
<span data-ttu-id="1409d-118">Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="1409d-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1409d-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="1409d-119">-NoWait</span></span>
<span data-ttu-id="1409d-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1409d-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1409d-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1409d-121">-PrivateCloudName</span></span>
<span data-ttu-id="1409d-122">Nome del cloud privato.</span><span class="sxs-lookup"><span data-stu-id="1409d-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="1409d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1409d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1409d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1409d-124">The name of the resource group.</span></span>
<span data-ttu-id="1409d-125">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1409d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1409d-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1409d-126">-SkuName</span></span>
<span data-ttu-id="1409d-127">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="1409d-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="1409d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1409d-128">-SubscriptionId</span></span>
<span data-ttu-id="1409d-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1409d-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1409d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1409d-130">-Confirm</span></span>
<span data-ttu-id="1409d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1409d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1409d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1409d-132">-WhatIf</span></span>
<span data-ttu-id="1409d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1409d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1409d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1409d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1409d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1409d-135">CommonParameters</span></span>
<span data-ttu-id="1409d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1409d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1409d-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1409d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1409d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1409d-138">INPUTS</span></span>

## <span data-ttu-id="1409d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1409d-139">OUTPUTS</span></span>

### <span data-ttu-id="1409d-140">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="1409d-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="1409d-141">Note</span><span class="sxs-lookup"><span data-stu-id="1409d-141">NOTES</span></span>

<span data-ttu-id="1409d-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1409d-142">ALIASES</span></span>

## <span data-ttu-id="1409d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1409d-143">RELATED LINKS</span></span>

