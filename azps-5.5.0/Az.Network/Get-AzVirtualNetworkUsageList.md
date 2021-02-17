---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184615"
---
# <span data-ttu-id="94c1c-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="94c1c-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="94c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="94c1c-103">Ottiene l'utilizzo corrente della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="94c1c-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="94c1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94c1c-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94c1c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="94c1c-106">Il **cmdlet Get-AzVirtualNetworkUsageList** ottiene l'uso della subnet per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="94c1c-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="94c1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="94c1c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94c1c-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="94c1c-109">Ottiene i valori di utilizzo correnti della subnet per la rete virtuale usagetest.</span><span class="sxs-lookup"><span data-stu-id="94c1c-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="94c1c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94c1c-110">PARAMETERS</span></span>

### <span data-ttu-id="94c1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c1c-111">-DefaultProfile</span></span>
<span data-ttu-id="94c1c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94c1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94c1c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="94c1c-113">-Name</span></span>
<span data-ttu-id="94c1c-114">Specifica il nome della rete virtuale per cui visualizzare gli utilizzi.</span><span class="sxs-lookup"><span data-stu-id="94c1c-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c1c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c1c-115">-ResourceGroupName</span></span>
<span data-ttu-id="94c1c-116">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="94c1c-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c1c-117">CommonParameters</span></span>
<span data-ttu-id="94c1c-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c1c-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94c1c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c1c-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="94c1c-120">INPUTS</span></span>

### <span data-ttu-id="94c1c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="94c1c-121">System.String</span></span>

## <span data-ttu-id="94c1c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94c1c-122">OUTPUTS</span></span>

### <span data-ttu-id="94c1c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="94c1c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="94c1c-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="94c1c-124">NOTES</span></span>

## <span data-ttu-id="94c1c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94c1c-125">RELATED LINKS</span></span>
