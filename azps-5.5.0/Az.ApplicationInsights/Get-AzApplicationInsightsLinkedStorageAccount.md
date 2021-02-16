---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195286"
---
# <span data-ttu-id="437f9-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="437f9-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="437f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="437f9-102">SYNOPSIS</span></span>
<span data-ttu-id="437f9-103">Ottenere informazioni dettagliate sull'applicazione per l'account di archiviazione collegato</span><span class="sxs-lookup"><span data-stu-id="437f9-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="437f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="437f9-104">SYNTAX</span></span>

### <span data-ttu-id="437f9-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="437f9-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="437f9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="437f9-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="437f9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="437f9-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="437f9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="437f9-108">DESCRIPTION</span></span>
<span data-ttu-id="437f9-109">Ottenere informazioni dettagliate sull'applicazione per l'account di archiviazione collegato</span><span class="sxs-lookup"><span data-stu-id="437f9-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="437f9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="437f9-110">EXAMPLES</span></span>

### <span data-ttu-id="437f9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="437f9-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="437f9-112">Ottenere l'account di archiviazione collegato associato al componente "componentName"</span><span class="sxs-lookup"><span data-stu-id="437f9-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="437f9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="437f9-113">PARAMETERS</span></span>

### <span data-ttu-id="437f9-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="437f9-114">-ComponentName</span></span>
<span data-ttu-id="437f9-115">Nome componente</span><span class="sxs-lookup"><span data-stu-id="437f9-115">Component Name</span></span>

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

### <span data-ttu-id="437f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="437f9-116">-DefaultProfile</span></span>
<span data-ttu-id="437f9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="437f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="437f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="437f9-118">-InputObject</span></span>
<span data-ttu-id="437f9-119">PSApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="437f9-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="437f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="437f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="437f9-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="437f9-121">Resource Group Name</span></span>

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

### <span data-ttu-id="437f9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="437f9-122">-ResourceId</span></span>
<span data-ttu-id="437f9-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="437f9-123">Component ResourceId</span></span>

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

### <span data-ttu-id="437f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437f9-124">CommonParameters</span></span>
<span data-ttu-id="437f9-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="437f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437f9-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="437f9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437f9-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="437f9-127">INPUTS</span></span>

### <span data-ttu-id="437f9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="437f9-128">System.String</span></span>

### <span data-ttu-id="437f9-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="437f9-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="437f9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="437f9-130">OUTPUTS</span></span>

### <span data-ttu-id="437f9-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSEgLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="437f9-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="437f9-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="437f9-132">NOTES</span></span>

## <span data-ttu-id="437f9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="437f9-133">RELATED LINKS</span></span>
