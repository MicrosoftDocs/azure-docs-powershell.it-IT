---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192099"
---
# <span data-ttu-id="b82a5-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b82a5-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="b82a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b82a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b82a5-103">Ottiene un Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="b82a5-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="b82a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b82a5-104">SYNTAX</span></span>

### <span data-ttu-id="b82a5-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b82a5-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b82a5-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="b82a5-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b82a5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b82a5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b82a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b82a5-108">DESCRIPTION</span></span>
<span data-ttu-id="b82a5-109">Il cmdlet **Get-AzIpAllocation** ottiene un IpAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="b82a5-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="b82a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b82a5-110">EXAMPLES</span></span>

### <span data-ttu-id="b82a5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b82a5-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="b82a5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b82a5-112">PARAMETERS</span></span>

### <span data-ttu-id="b82a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82a5-113">-DefaultProfile</span></span>
<span data-ttu-id="b82a5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b82a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b82a5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b82a5-115">-Name</span></span>
<span data-ttu-id="b82a5-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b82a5-116">The resource name.</span></span>

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

### <span data-ttu-id="b82a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b82a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b82a5-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b82a5-118">The resource group name.</span></span>

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

### <span data-ttu-id="b82a5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b82a5-119">-ResourceId</span></span>
<span data-ttu-id="b82a5-120">ID IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b82a5-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="b82a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82a5-121">CommonParameters</span></span>
<span data-ttu-id="b82a5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b82a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82a5-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b82a5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82a5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b82a5-124">INPUTS</span></span>

### <span data-ttu-id="b82a5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b82a5-125">System.String</span></span>

## <span data-ttu-id="b82a5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b82a5-126">OUTPUTS</span></span>

### <span data-ttu-id="b82a5-127">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b82a5-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b82a5-128">Note</span><span class="sxs-lookup"><span data-stu-id="b82a5-128">NOTES</span></span>

## <span data-ttu-id="b82a5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b82a5-129">RELATED LINKS</span></span>
