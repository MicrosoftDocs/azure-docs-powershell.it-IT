---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965230"
---
# <span data-ttu-id="1324f-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1324f-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="1324f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1324f-102">SYNOPSIS</span></span>
<span data-ttu-id="1324f-103">Ottenere informazioni dettagliate sull'applicazione per l'account di archiviazione collegato</span><span class="sxs-lookup"><span data-stu-id="1324f-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="1324f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1324f-104">SYNTAX</span></span>

### <span data-ttu-id="1324f-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="1324f-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1324f-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1324f-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1324f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1324f-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1324f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1324f-108">DESCRIPTION</span></span>
<span data-ttu-id="1324f-109">Ottenere informazioni dettagliate sull'applicazione per l'account di archiviazione collegato</span><span class="sxs-lookup"><span data-stu-id="1324f-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="1324f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1324f-110">EXAMPLES</span></span>

### <span data-ttu-id="1324f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1324f-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="1324f-112">Ottenere l'account di archiviazione collegato associato al componente "componentName"</span><span class="sxs-lookup"><span data-stu-id="1324f-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="1324f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1324f-113">PARAMETERS</span></span>

### <span data-ttu-id="1324f-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="1324f-114">-ComponentName</span></span>
<span data-ttu-id="1324f-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="1324f-115">Component Name</span></span>

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

### <span data-ttu-id="1324f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1324f-116">-DefaultProfile</span></span>
<span data-ttu-id="1324f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1324f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1324f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1324f-118">-InputObject</span></span>
<span data-ttu-id="1324f-119">PSApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="1324f-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="1324f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1324f-120">-ResourceGroupName</span></span>
<span data-ttu-id="1324f-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1324f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="1324f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1324f-122">-ResourceId</span></span>
<span data-ttu-id="1324f-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="1324f-123">Component ResourceId</span></span>

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

### <span data-ttu-id="1324f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1324f-124">CommonParameters</span></span>
<span data-ttu-id="1324f-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1324f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1324f-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1324f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1324f-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="1324f-127">INPUTS</span></span>

### <span data-ttu-id="1324f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1324f-128">System.String</span></span>

### <span data-ttu-id="1324f-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="1324f-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="1324f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1324f-130">OUTPUTS</span></span>

### <span data-ttu-id="1324f-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSEgLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1324f-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="1324f-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="1324f-132">NOTES</span></span>

## <span data-ttu-id="1324f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1324f-133">RELATED LINKS</span></span>
