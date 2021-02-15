---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182223"
---
# <span data-ttu-id="d8d00-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8d00-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d8d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d00-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d00-103">Aggiornare l'account di archiviazione collegato di Approfondimenti applicazioni</span><span class="sxs-lookup"><span data-stu-id="d8d00-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="d8d00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8d00-104">SYNTAX</span></span>

### <span data-ttu-id="d8d00-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="d8d00-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8d00-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8d00-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8d00-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8d00-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d00-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8d00-108">DESCRIPTION</span></span>
<span data-ttu-id="d8d00-109">Aggiornare l'account di archiviazione collegato di Approfondimenti applicazioni</span><span class="sxs-lookup"><span data-stu-id="d8d00-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="d8d00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8d00-110">EXAMPLES</span></span>

### <span data-ttu-id="d8d00-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8d00-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="d8d00-112">Aggiornare l'account di archiviazione collegato nel componente "componentName" da associare alla $account</span><span class="sxs-lookup"><span data-stu-id="d8d00-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="d8d00-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d00-113">PARAMETERS</span></span>

### <span data-ttu-id="d8d00-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d8d00-114">-ComponentName</span></span>
<span data-ttu-id="d8d00-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="d8d00-115">Component Name</span></span>

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

### <span data-ttu-id="d8d00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d00-116">-DefaultProfile</span></span>
<span data-ttu-id="d8d00-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d00-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d00-118">-InputObject</span></span>
<span data-ttu-id="d8d00-119">PSApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="d8d00-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="d8d00-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d8d00-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="d8d00-121">ResourceId dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d8d00-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="d8d00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d00-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8d00-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d8d00-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d8d00-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8d00-124">-ResourceId</span></span>
<span data-ttu-id="d8d00-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8d00-125">Component ResourceId</span></span>

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

### <span data-ttu-id="d8d00-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8d00-126">-Confirm</span></span>
<span data-ttu-id="d8d00-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d00-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d00-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d00-128">-WhatIf</span></span>
<span data-ttu-id="d8d00-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8d00-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d00-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8d00-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d00-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d00-131">CommonParameters</span></span>
<span data-ttu-id="d8d00-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d00-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d00-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8d00-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d00-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8d00-134">INPUTS</span></span>

### <span data-ttu-id="d8d00-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d8d00-135">System.String</span></span>

### <span data-ttu-id="d8d00-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="d8d00-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="d8d00-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8d00-137">OUTPUTS</span></span>

### <span data-ttu-id="d8d00-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSEgLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d8d00-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="d8d00-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8d00-139">NOTES</span></span>

## <span data-ttu-id="d8d00-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8d00-140">RELATED LINKS</span></span>
