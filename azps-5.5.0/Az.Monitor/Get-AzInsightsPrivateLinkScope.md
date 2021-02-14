---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203479"
---
# <span data-ttu-id="d1723-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d1723-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="d1723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1723-102">SYNOPSIS</span></span>
<span data-ttu-id="d1723-103">Ottenere l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="d1723-103">Get private link scope</span></span>

## <span data-ttu-id="d1723-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1723-104">SYNTAX</span></span>

### <span data-ttu-id="d1723-105">ByResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1723-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1723-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1723-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1723-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1723-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1723-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1723-108">DESCRIPTION</span></span>
<span data-ttu-id="d1723-109">Elencare o ottenere l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="d1723-109">List or get private link scope</span></span> 

## <span data-ttu-id="d1723-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1723-110">EXAMPLES</span></span>

### <span data-ttu-id="d1723-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1723-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="d1723-112">Elencare gli ambiti dei collegamenti privati nel gruppo di risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="d1723-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="d1723-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d1723-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="d1723-114">Ottenere l'ambito del collegamento privato con il nome "scope_name" nel gruppo di risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="d1723-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="d1723-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1723-115">PARAMETERS</span></span>

### <span data-ttu-id="d1723-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1723-116">-DefaultProfile</span></span>
<span data-ttu-id="d1723-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1723-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1723-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d1723-118">-Name</span></span>
<span data-ttu-id="d1723-119">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="d1723-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d1723-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1723-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1723-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d1723-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="d1723-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1723-122">-ResourceId</span></span>
<span data-ttu-id="d1723-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="d1723-123">Resource Id</span></span>

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

### <span data-ttu-id="d1723-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1723-124">CommonParameters</span></span>
<span data-ttu-id="d1723-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1723-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1723-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1723-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1723-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1723-127">INPUTS</span></span>

### <span data-ttu-id="d1723-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d1723-128">System.String</span></span>

## <span data-ttu-id="d1723-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1723-129">OUTPUTS</span></span>

### <span data-ttu-id="d1723-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d1723-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="d1723-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1723-131">NOTES</span></span>

## <span data-ttu-id="d1723-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1723-132">RELATED LINKS</span></span>
