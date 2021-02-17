---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184614"
---
# <span data-ttu-id="acd56-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="acd56-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="acd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd56-102">SYNOPSIS</span></span>
<span data-ttu-id="acd56-103">Ottenere un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="acd56-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="acd56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acd56-104">SYNTAX</span></span>

### <span data-ttu-id="acd56-105">VirtualRouterSubscriptionIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="acd56-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acd56-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd56-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acd56-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd56-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd56-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="acd56-108">DESCRIPTION</span></span>
<span data-ttu-id="acd56-109">Il cmdlet **Get-AzVirtualRouter** ottiene un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="acd56-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="acd56-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acd56-110">EXAMPLES</span></span>

### <span data-ttu-id="acd56-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="acd56-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="acd56-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="acd56-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="acd56-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd56-113">PARAMETERS</span></span>

### <span data-ttu-id="acd56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd56-114">-DefaultProfile</span></span>
<span data-ttu-id="acd56-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acd56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd56-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd56-116">-ResourceGroupName</span></span>
<span data-ttu-id="acd56-117">Nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="acd56-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd56-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acd56-118">-ResourceId</span></span>
<span data-ttu-id="acd56-119">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="acd56-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd56-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="acd56-120">-RouterName</span></span>
<span data-ttu-id="acd56-121">Il nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="acd56-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acd56-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd56-122">CommonParameters</span></span>
<span data-ttu-id="acd56-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd56-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd56-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="acd56-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd56-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="acd56-125">INPUTS</span></span>

### <span data-ttu-id="acd56-126">System.String</span><span class="sxs-lookup"><span data-stu-id="acd56-126">System.String</span></span>

## <span data-ttu-id="acd56-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acd56-127">OUTPUTS</span></span>

### <span data-ttu-id="acd56-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="acd56-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="acd56-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="acd56-129">NOTES</span></span>

## <span data-ttu-id="acd56-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acd56-130">RELATED LINKS</span></span>
