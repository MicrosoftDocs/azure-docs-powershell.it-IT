---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300300"
---
# <span data-ttu-id="ae3f6-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="ae3f6-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="ae3f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3f6-103">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="ae3f6-103">Create cluster</span></span>

## <span data-ttu-id="ae3f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae3f6-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae3f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae3f6-105">DESCRIPTION</span></span>

<span data-ttu-id="ae3f6-106">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="ae3f6-106">Create cluster</span></span>

## <span data-ttu-id="ae3f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ae3f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae3f6-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="ae3f6-109">Creare un cluster</span><span class="sxs-lookup"><span data-stu-id="ae3f6-109">Create cluster</span></span>

## <span data-ttu-id="ae3f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae3f6-110">PARAMETERS</span></span>

### <span data-ttu-id="ae3f6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae3f6-111">-AsJob</span></span>
<span data-ttu-id="ae3f6-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ae3f6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae3f6-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ae3f6-113">-ClusterName</span></span>
<span data-ttu-id="ae3f6-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-114">The cluster name.</span></span>

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

### <span data-ttu-id="ae3f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3f6-115">-DefaultProfile</span></span>
<span data-ttu-id="ae3f6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae3f6-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ae3f6-117">-IdentityType</span></span>
<span data-ttu-id="ae3f6-118">il tipo di identità, value può essere "SystemAssigned", "None".</span><span class="sxs-lookup"><span data-stu-id="ae3f6-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3f6-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ae3f6-119">-Location</span></span>
<span data-ttu-id="ae3f6-120">Area geografica in cui verrà distribuito il cluster.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="ae3f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae3f6-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-122">The resource group name.</span></span>

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

### <span data-ttu-id="ae3f6-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ae3f6-123">-SkuCapacity</span></span>
<span data-ttu-id="ae3f6-124">Capacità SKU, il valore deve essere multiplo di 100 e nell'intervallo di 1000-2000.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3f6-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ae3f6-125">-SkuName</span></span>
<span data-ttu-id="ae3f6-126">Nome Usk, ora può essere solo ' CapacityReservation '</span><span class="sxs-lookup"><span data-stu-id="ae3f6-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3f6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae3f6-127">-Tags</span></span>
<span data-ttu-id="ae3f6-128">Tag del cluster</span><span class="sxs-lookup"><span data-stu-id="ae3f6-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3f6-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae3f6-129">-Confirm</span></span>
<span data-ttu-id="ae3f6-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3f6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3f6-131">-WhatIf</span></span>
<span data-ttu-id="ae3f6-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae3f6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3f6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3f6-134">CommonParameters</span></span>
<span data-ttu-id="ae3f6-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3f6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3f6-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae3f6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3f6-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae3f6-137">INPUTS</span></span>

### <span data-ttu-id="ae3f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ae3f6-138">System.String</span></span>

## <span data-ttu-id="ae3f6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae3f6-139">OUTPUTS</span></span>

### <span data-ttu-id="ae3f6-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ae3f6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="ae3f6-141">Note</span><span class="sxs-lookup"><span data-stu-id="ae3f6-141">NOTES</span></span>

## <span data-ttu-id="ae3f6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae3f6-142">RELATED LINKS</span></span>
