---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192088"
---
# <span data-ttu-id="fd558-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fd558-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="fd558-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd558-102">SYNOPSIS</span></span>
<span data-ttu-id="fd558-103">Ottenere un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fd558-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="fd558-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd558-104">SYNTAX</span></span>

### <span data-ttu-id="fd558-105">VirtualRouterSubscriptionIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd558-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd558-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd558-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd558-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd558-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd558-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd558-108">DESCRIPTION</span></span>
<span data-ttu-id="fd558-109">Il cmdlet **Get-AzVirtualRouter** ottiene un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="fd558-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="fd558-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd558-110">EXAMPLES</span></span>

### <span data-ttu-id="fd558-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd558-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="fd558-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fd558-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="fd558-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd558-113">PARAMETERS</span></span>

### <span data-ttu-id="fd558-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd558-114">-DefaultProfile</span></span>
<span data-ttu-id="fd558-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd558-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd558-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd558-116">-ResourceGroupName</span></span>
<span data-ttu-id="fd558-117">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd558-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="fd558-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd558-118">-ResourceId</span></span>
<span data-ttu-id="fd558-119">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd558-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="fd558-120">-Routername</span><span class="sxs-lookup"><span data-stu-id="fd558-120">-RouterName</span></span>
<span data-ttu-id="fd558-121">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd558-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="fd558-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd558-122">CommonParameters</span></span>
<span data-ttu-id="fd558-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd558-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd558-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd558-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd558-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd558-125">INPUTS</span></span>

### <span data-ttu-id="fd558-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fd558-126">System.String</span></span>

## <span data-ttu-id="fd558-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd558-127">OUTPUTS</span></span>

### <span data-ttu-id="fd558-128">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="fd558-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="fd558-129">Note</span><span class="sxs-lookup"><span data-stu-id="fd558-129">NOTES</span></span>

## <span data-ttu-id="fd558-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd558-130">RELATED LINKS</span></span>
