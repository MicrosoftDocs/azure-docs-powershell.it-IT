---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 50391bcd4356f24db6107a64ee5bdec9827407f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972238"
---
# <span data-ttu-id="16d4b-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="16d4b-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="16d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="16d4b-103">Aggiornare l'account di archiviazione collegato di Approfondimenti applicazioni</span><span class="sxs-lookup"><span data-stu-id="16d4b-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="16d4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16d4b-104">SYNTAX</span></span>

### <span data-ttu-id="16d4b-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="16d4b-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16d4b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d4b-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16d4b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d4b-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16d4b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16d4b-108">DESCRIPTION</span></span>
<span data-ttu-id="16d4b-109">Aggiornare l'account di archiviazione collegato di Application Insights</span><span class="sxs-lookup"><span data-stu-id="16d4b-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="16d4b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16d4b-110">EXAMPLES</span></span>

### <span data-ttu-id="16d4b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16d4b-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="16d4b-112">Aggiornare l'account di archiviazione collegato nel componente "componentName" da associare $account</span><span class="sxs-lookup"><span data-stu-id="16d4b-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="16d4b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16d4b-113">PARAMETERS</span></span>

### <span data-ttu-id="16d4b-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="16d4b-114">-ComponentName</span></span>
<span data-ttu-id="16d4b-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="16d4b-115">Component Name</span></span>

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

### <span data-ttu-id="16d4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d4b-116">-DefaultProfile</span></span>
<span data-ttu-id="16d4b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16d4b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d4b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16d4b-118">-InputObject</span></span>
<span data-ttu-id="16d4b-119">PSApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="16d4b-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="16d4b-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="16d4b-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="16d4b-121">ResourceId dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="16d4b-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="16d4b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d4b-122">-ResourceGroupName</span></span>
<span data-ttu-id="16d4b-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="16d4b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="16d4b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16d4b-124">-ResourceId</span></span>
<span data-ttu-id="16d4b-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="16d4b-125">Component ResourceId</span></span>

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

### <span data-ttu-id="16d4b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16d4b-126">-Confirm</span></span>
<span data-ttu-id="16d4b-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16d4b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d4b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d4b-128">-WhatIf</span></span>
<span data-ttu-id="16d4b-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16d4b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16d4b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16d4b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d4b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d4b-131">CommonParameters</span></span>
<span data-ttu-id="16d4b-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d4b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d4b-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16d4b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d4b-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="16d4b-134">INPUTS</span></span>

### <span data-ttu-id="16d4b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="16d4b-135">System.String</span></span>

### <span data-ttu-id="16d4b-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="16d4b-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="16d4b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16d4b-137">OUTPUTS</span></span>

### <span data-ttu-id="16d4b-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSEgLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="16d4b-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="16d4b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="16d4b-139">NOTES</span></span>

## <span data-ttu-id="16d4b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16d4b-140">RELATED LINKS</span></span>
