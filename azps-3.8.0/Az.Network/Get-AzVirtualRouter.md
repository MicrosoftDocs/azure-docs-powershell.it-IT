---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019322"
---
# <span data-ttu-id="3673c-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3673c-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="3673c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3673c-102">SYNOPSIS</span></span>
<span data-ttu-id="3673c-103">Ottenere un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3673c-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="3673c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3673c-104">SYNTAX</span></span>

### <span data-ttu-id="3673c-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3673c-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3673c-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3673c-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3673c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3673c-107">DESCRIPTION</span></span>
<span data-ttu-id="3673c-108">Il cmdlet **Get-AzVirtualRouter** ottiene un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="3673c-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="3673c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3673c-109">EXAMPLES</span></span>

### <span data-ttu-id="3673c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3673c-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="3673c-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3673c-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="3673c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3673c-112">PARAMETERS</span></span>

### <span data-ttu-id="3673c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3673c-113">-DefaultProfile</span></span>
<span data-ttu-id="3673c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3673c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3673c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3673c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3673c-116">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="3673c-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3673c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3673c-117">-ResourceId</span></span>
<span data-ttu-id="3673c-118">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="3673c-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3673c-119">-Routername</span><span class="sxs-lookup"><span data-stu-id="3673c-119">-RouterName</span></span>
<span data-ttu-id="3673c-120">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="3673c-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3673c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3673c-121">CommonParameters</span></span>
<span data-ttu-id="3673c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3673c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3673c-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3673c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3673c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3673c-124">INPUTS</span></span>

### <span data-ttu-id="3673c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3673c-125">System.String</span></span>

## <span data-ttu-id="3673c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3673c-126">OUTPUTS</span></span>

### <span data-ttu-id="3673c-127">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3673c-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="3673c-128">Note</span><span class="sxs-lookup"><span data-stu-id="3673c-128">NOTES</span></span>

## <span data-ttu-id="3673c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3673c-129">RELATED LINKS</span></span>
