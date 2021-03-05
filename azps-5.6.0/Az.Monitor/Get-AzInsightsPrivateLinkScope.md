---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 941b60da0282bdad523b06657639a730d1776ce3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980046"
---
# <span data-ttu-id="b0cdb-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b0cdb-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="b0cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b0cdb-103">Ottenere l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="b0cdb-103">Get private link scope</span></span>

## <span data-ttu-id="b0cdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0cdb-104">SYNTAX</span></span>

### <span data-ttu-id="b0cdb-105">ByResourceGroupParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b0cdb-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0cdb-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0cdb-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0cdb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0cdb-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0cdb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0cdb-108">DESCRIPTION</span></span>
<span data-ttu-id="b0cdb-109">Elencare o ottenere l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="b0cdb-109">List or get private link scope</span></span> 

## <span data-ttu-id="b0cdb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0cdb-110">EXAMPLES</span></span>

### <span data-ttu-id="b0cdb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0cdb-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="b0cdb-112">Elencare gli ambiti dei collegamenti privati nel gruppo di risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="b0cdb-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="b0cdb-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0cdb-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="b0cdb-114">Ottenere l'ambito del collegamento privato con il nome "scope_name" nel gruppo di risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="b0cdb-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="b0cdb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0cdb-115">PARAMETERS</span></span>

### <span data-ttu-id="b0cdb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0cdb-116">-DefaultProfile</span></span>
<span data-ttu-id="b0cdb-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0cdb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b0cdb-118">-Name</span></span>
<span data-ttu-id="b0cdb-119">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="b0cdb-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="b0cdb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0cdb-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0cdb-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b0cdb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b0cdb-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0cdb-122">-ResourceId</span></span>
<span data-ttu-id="b0cdb-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b0cdb-123">Resource Id</span></span>

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

### <span data-ttu-id="b0cdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0cdb-124">CommonParameters</span></span>
<span data-ttu-id="b0cdb-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0cdb-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0cdb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0cdb-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0cdb-127">INPUTS</span></span>

### <span data-ttu-id="b0cdb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b0cdb-128">System.String</span></span>

## <span data-ttu-id="b0cdb-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0cdb-129">OUTPUTS</span></span>

### <span data-ttu-id="b0cdb-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b0cdb-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="b0cdb-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0cdb-131">NOTES</span></span>

## <span data-ttu-id="b0cdb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0cdb-132">RELATED LINKS</span></span>
