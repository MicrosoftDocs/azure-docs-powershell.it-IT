---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 8a78fc36e13360babc43b512dccee80550b3fbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989853"
---
# <span data-ttu-id="74d14-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="74d14-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="74d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d14-102">SYNOPSIS</span></span>
<span data-ttu-id="74d14-103">Scollega servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="74d14-103">Unlink service for workspace</span></span>

## <span data-ttu-id="74d14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74d14-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74d14-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="74d14-105">DESCRIPTION</span></span>
<span data-ttu-id="74d14-106">Scollega servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="74d14-106">Unlink service for workspace</span></span>

## <span data-ttu-id="74d14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74d14-107">EXAMPLES</span></span>

### <span data-ttu-id="74d14-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74d14-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="74d14-109">Scollega servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="74d14-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="74d14-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74d14-110">PARAMETERS</span></span>

### <span data-ttu-id="74d14-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74d14-111">-AsJob</span></span>
<span data-ttu-id="74d14-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="74d14-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74d14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d14-113">-DefaultProfile</span></span>
<span data-ttu-id="74d14-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74d14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74d14-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="74d14-115">-LinkedServiceName</span></span>
<span data-ttu-id="74d14-116">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="74d14-116">The Workspace name.</span></span>

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

### <span data-ttu-id="74d14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d14-117">-ResourceGroupName</span></span>
<span data-ttu-id="74d14-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="74d14-118">The resource group name.</span></span>

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

### <span data-ttu-id="74d14-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74d14-119">-WorkspaceName</span></span>
<span data-ttu-id="74d14-120">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="74d14-120">The Workspace name.</span></span>

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

### <span data-ttu-id="74d14-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74d14-121">-Confirm</span></span>
<span data-ttu-id="74d14-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74d14-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d14-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d14-123">-WhatIf</span></span>
<span data-ttu-id="74d14-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74d14-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74d14-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74d14-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d14-126">CommonParameters</span></span>
<span data-ttu-id="74d14-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d14-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74d14-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d14-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="74d14-129">INPUTS</span></span>

### <span data-ttu-id="74d14-130">System.String</span><span class="sxs-lookup"><span data-stu-id="74d14-130">System.String</span></span>

## <span data-ttu-id="74d14-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74d14-131">OUTPUTS</span></span>

### <span data-ttu-id="74d14-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74d14-132">System.Boolean</span></span>

## <span data-ttu-id="74d14-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="74d14-133">NOTES</span></span>

## <span data-ttu-id="74d14-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74d14-134">RELATED LINKS</span></span>
