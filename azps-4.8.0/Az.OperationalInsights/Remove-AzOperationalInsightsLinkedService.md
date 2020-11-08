---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188336"
---
# <span data-ttu-id="c5f1d-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="c5f1d-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="c5f1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f1d-103">Scollegare il servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c5f1d-103">Unlink service for workspace</span></span>

## <span data-ttu-id="c5f1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5f1d-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5f1d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f1d-106">Scollegare il servizio per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c5f1d-106">Unlink service for workspace</span></span>

## <span data-ttu-id="c5f1d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f1d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5f1d-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="c5f1d-109">Scollegare il servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c5f1d-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="c5f1d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5f1d-110">PARAMETERS</span></span>

### <span data-ttu-id="c5f1d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5f1d-111">-AsJob</span></span>
<span data-ttu-id="c5f1d-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c5f1d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5f1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f1d-113">-DefaultProfile</span></span>
<span data-ttu-id="c5f1d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5f1d-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c5f1d-115">-LinkedServiceName</span></span>
<span data-ttu-id="c5f1d-116">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-116">The Workspace name.</span></span>

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

### <span data-ttu-id="c5f1d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f1d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5f1d-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-118">The resource group name.</span></span>

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

### <span data-ttu-id="c5f1d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5f1d-119">-WorkspaceName</span></span>
<span data-ttu-id="c5f1d-120">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-120">The Workspace name.</span></span>

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

### <span data-ttu-id="c5f1d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5f1d-121">-Confirm</span></span>
<span data-ttu-id="c5f1d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5f1d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5f1d-123">-WhatIf</span></span>
<span data-ttu-id="c5f1d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5f1d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5f1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f1d-126">CommonParameters</span></span>
<span data-ttu-id="c5f1d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f1d-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5f1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f1d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5f1d-129">INPUTS</span></span>

### <span data-ttu-id="c5f1d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c5f1d-130">System.String</span></span>

## <span data-ttu-id="c5f1d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5f1d-131">OUTPUTS</span></span>

### <span data-ttu-id="c5f1d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5f1d-132">System.Boolean</span></span>

## <span data-ttu-id="c5f1d-133">Note</span><span class="sxs-lookup"><span data-stu-id="c5f1d-133">NOTES</span></span>

## <span data-ttu-id="c5f1d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5f1d-134">RELATED LINKS</span></span>