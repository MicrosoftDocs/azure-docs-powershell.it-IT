---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: c08a148d1c58e08daa2fce8cd1e195887a264f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956909"
---
# <span data-ttu-id="c36ec-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c36ec-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="c36ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c36ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c36ec-103">Ottiene una ipAllocation di Azure.</span><span class="sxs-lookup"><span data-stu-id="c36ec-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="c36ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c36ec-104">SYNTAX</span></span>

### <span data-ttu-id="c36ec-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c36ec-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c36ec-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="c36ec-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c36ec-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c36ec-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36ec-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c36ec-108">DESCRIPTION</span></span>
<span data-ttu-id="c36ec-109">Il cmdlet **Get-AzIpAllocation** ottiene una ipAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="c36ec-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="c36ec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c36ec-110">EXAMPLES</span></span>

### <span data-ttu-id="c36ec-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c36ec-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="c36ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c36ec-112">PARAMETERS</span></span>

### <span data-ttu-id="c36ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36ec-113">-DefaultProfile</span></span>
<span data-ttu-id="c36ec-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c36ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36ec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c36ec-115">-Name</span></span>
<span data-ttu-id="c36ec-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c36ec-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="c36ec-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c36ec-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c36ec-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c36ec-119">-ResourceId</span></span>
<span data-ttu-id="c36ec-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="c36ec-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36ec-121">CommonParameters</span></span>
<span data-ttu-id="c36ec-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36ec-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c36ec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36ec-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="c36ec-124">INPUTS</span></span>

### <span data-ttu-id="c36ec-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c36ec-125">System.String</span></span>

## <span data-ttu-id="c36ec-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c36ec-126">OUTPUTS</span></span>

### <span data-ttu-id="c36ec-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="c36ec-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="c36ec-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="c36ec-128">NOTES</span></span>

## <span data-ttu-id="c36ec-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c36ec-129">RELATED LINKS</span></span>
