---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 2cccbc06095f9ff71f4b16d40bca16d91e91dda0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997259"
---
# <span data-ttu-id="70ae5-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="70ae5-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="70ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="70ae5-103">Ottenere un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="70ae5-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="70ae5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70ae5-104">SYNTAX</span></span>

### <span data-ttu-id="70ae5-105">VirtualRouterSubscriptionIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70ae5-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="70ae5-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70ae5-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ae5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70ae5-108">DESCRIPTION</span></span>
<span data-ttu-id="70ae5-109">Il cmdlet **Get-AzVirtualRouter** ottiene un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="70ae5-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="70ae5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70ae5-110">EXAMPLES</span></span>

### <span data-ttu-id="70ae5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70ae5-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="70ae5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="70ae5-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="70ae5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70ae5-113">PARAMETERS</span></span>

### <span data-ttu-id="70ae5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ae5-114">-DefaultProfile</span></span>
<span data-ttu-id="70ae5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70ae5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ae5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ae5-116">-ResourceGroupName</span></span>
<span data-ttu-id="70ae5-117">Nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="70ae5-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="70ae5-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70ae5-118">-ResourceId</span></span>
<span data-ttu-id="70ae5-119">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="70ae5-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="70ae5-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="70ae5-120">-RouterName</span></span>
<span data-ttu-id="70ae5-121">Il nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="70ae5-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="70ae5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ae5-122">CommonParameters</span></span>
<span data-ttu-id="70ae5-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ae5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ae5-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70ae5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ae5-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="70ae5-125">INPUTS</span></span>

### <span data-ttu-id="70ae5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="70ae5-126">System.String</span></span>

## <span data-ttu-id="70ae5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70ae5-127">OUTPUTS</span></span>

### <span data-ttu-id="70ae5-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="70ae5-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="70ae5-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="70ae5-129">NOTES</span></span>

## <span data-ttu-id="70ae5-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70ae5-130">RELATED LINKS</span></span>
