---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202338"
---
# <span data-ttu-id="3b209-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="3b209-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="3b209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b209-102">SYNOPSIS</span></span>
<span data-ttu-id="3b209-103">Elimina cluster</span><span class="sxs-lookup"><span data-stu-id="3b209-103">Delete cluster</span></span>

## <span data-ttu-id="3b209-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b209-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b209-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b209-105">DESCRIPTION</span></span>
<span data-ttu-id="3b209-106">Elimina cluster, applica solo ai cluster con stato di provisioning "Completato"</span><span class="sxs-lookup"><span data-stu-id="3b209-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="3b209-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b209-107">EXAMPLES</span></span>

### <span data-ttu-id="3b209-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b209-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="3b209-109">Elimina cluster</span><span class="sxs-lookup"><span data-stu-id="3b209-109">Delete cluster</span></span>

## <span data-ttu-id="3b209-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b209-110">PARAMETERS</span></span>

### <span data-ttu-id="3b209-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b209-111">-AsJob</span></span>
<span data-ttu-id="3b209-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3b209-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b209-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3b209-113">-ClusterName</span></span>
<span data-ttu-id="3b209-114">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="3b209-114">The cluster name.</span></span>

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

### <span data-ttu-id="3b209-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b209-115">-DefaultProfile</span></span>
<span data-ttu-id="3b209-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b209-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b209-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b209-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b209-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b209-118">The resource group name.</span></span>

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

### <span data-ttu-id="3b209-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b209-119">-Confirm</span></span>
<span data-ttu-id="3b209-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b209-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b209-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b209-121">-WhatIf</span></span>
<span data-ttu-id="3b209-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b209-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b209-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b209-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b209-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b209-124">CommonParameters</span></span>
<span data-ttu-id="3b209-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b209-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b209-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b209-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b209-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b209-127">INPUTS</span></span>

### <span data-ttu-id="3b209-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3b209-128">System.String</span></span>

## <span data-ttu-id="3b209-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b209-129">OUTPUTS</span></span>

### <span data-ttu-id="3b209-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b209-130">System.Boolean</span></span>

## <span data-ttu-id="3b209-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b209-131">NOTES</span></span>

## <span data-ttu-id="3b209-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b209-132">RELATED LINKS</span></span>
