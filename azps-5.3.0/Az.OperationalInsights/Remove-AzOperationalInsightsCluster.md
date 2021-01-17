---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488801"
---
# <span data-ttu-id="1d432-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="1d432-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="1d432-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d432-102">SYNOPSIS</span></span>
<span data-ttu-id="1d432-103">Eliminare un cluster</span><span class="sxs-lookup"><span data-stu-id="1d432-103">Delete cluster</span></span>

## <span data-ttu-id="1d432-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d432-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d432-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d432-105">DESCRIPTION</span></span>
<span data-ttu-id="1d432-106">Elimina cluster, applica solo ai cluster con lo stato di provisioning "succeeded"</span><span class="sxs-lookup"><span data-stu-id="1d432-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="1d432-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d432-107">EXAMPLES</span></span>

### <span data-ttu-id="1d432-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d432-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="1d432-109">Eliminare un cluster</span><span class="sxs-lookup"><span data-stu-id="1d432-109">Delete cluster</span></span>

## <span data-ttu-id="1d432-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d432-110">PARAMETERS</span></span>

### <span data-ttu-id="1d432-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d432-111">-AsJob</span></span>
<span data-ttu-id="1d432-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1d432-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d432-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1d432-113">-ClusterName</span></span>
<span data-ttu-id="1d432-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="1d432-114">The cluster name.</span></span>

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

### <span data-ttu-id="1d432-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d432-115">-DefaultProfile</span></span>
<span data-ttu-id="1d432-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d432-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d432-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d432-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d432-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d432-118">The resource group name.</span></span>

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

### <span data-ttu-id="1d432-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d432-119">-Confirm</span></span>
<span data-ttu-id="1d432-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d432-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d432-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d432-121">-WhatIf</span></span>
<span data-ttu-id="1d432-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d432-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d432-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d432-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d432-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d432-124">CommonParameters</span></span>
<span data-ttu-id="1d432-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d432-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d432-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d432-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d432-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d432-127">INPUTS</span></span>

### <span data-ttu-id="1d432-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d432-128">System.String</span></span>

## <span data-ttu-id="1d432-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d432-129">OUTPUTS</span></span>

### <span data-ttu-id="1d432-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d432-130">System.Boolean</span></span>

## <span data-ttu-id="1d432-131">Note</span><span class="sxs-lookup"><span data-stu-id="1d432-131">NOTES</span></span>

## <span data-ttu-id="1d432-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d432-132">RELATED LINKS</span></span>
