---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 377a2b967058de9c0cdae1d4c07ceffc73b1bfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001886"
---
# <span data-ttu-id="46183-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46183-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="46183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46183-102">SYNOPSIS</span></span>
<span data-ttu-id="46183-103">Eliminare l'account di archiviazione collegato di Application Insights</span><span class="sxs-lookup"><span data-stu-id="46183-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="46183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46183-104">SYNTAX</span></span>

### <span data-ttu-id="46183-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="46183-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46183-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46183-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46183-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46183-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46183-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="46183-108">DESCRIPTION</span></span>
<span data-ttu-id="46183-109">Eliminare l'account di archiviazione collegato di Application Insights</span><span class="sxs-lookup"><span data-stu-id="46183-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="46183-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46183-110">EXAMPLES</span></span>

### <span data-ttu-id="46183-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46183-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="46183-112">Eliminare l'account di archiviazione collegato associato al componente Application Insights "componentName"</span><span class="sxs-lookup"><span data-stu-id="46183-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="46183-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46183-113">PARAMETERS</span></span>

### <span data-ttu-id="46183-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="46183-114">-ComponentName</span></span>
<span data-ttu-id="46183-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="46183-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46183-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46183-116">-DefaultProfile</span></span>
<span data-ttu-id="46183-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46183-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46183-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46183-118">-InputObject</span></span>
<span data-ttu-id="46183-119">PSApplicationInsightsApplication</span><span class="sxs-lookup"><span data-stu-id="46183-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46183-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46183-120">-ResourceGroupName</span></span>
<span data-ttu-id="46183-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="46183-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46183-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46183-122">-ResourceId</span></span>
<span data-ttu-id="46183-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="46183-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46183-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46183-124">-Confirm</span></span>
<span data-ttu-id="46183-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46183-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46183-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46183-126">-WhatIf</span></span>
<span data-ttu-id="46183-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46183-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46183-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46183-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46183-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46183-129">CommonParameters</span></span>
<span data-ttu-id="46183-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46183-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46183-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46183-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46183-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="46183-132">INPUTS</span></span>

### <span data-ttu-id="46183-133">System.String</span><span class="sxs-lookup"><span data-stu-id="46183-133">System.String</span></span>

### <span data-ttu-id="46183-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="46183-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="46183-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46183-135">OUTPUTS</span></span>

### <span data-ttu-id="46183-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46183-136">System.Boolean</span></span>

## <span data-ttu-id="46183-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="46183-137">NOTES</span></span>

## <span data-ttu-id="46183-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46183-138">RELATED LINKS</span></span>
