---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203318"
---
# <span data-ttu-id="80907-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="80907-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="80907-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80907-102">SYNOPSIS</span></span>
<span data-ttu-id="80907-103">Ottiene l'utilizzo corrente della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="80907-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="80907-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80907-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80907-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80907-105">DESCRIPTION</span></span>
<span data-ttu-id="80907-106">Il cmdlet **Get-AzVirtualNetworkUsageList** Ottiene l'utilizzo per ogni subnet per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="80907-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="80907-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80907-107">EXAMPLES</span></span>

### <span data-ttu-id="80907-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="80907-108">Example 1</span></span>
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

<span data-ttu-id="80907-109">Ottiene i valori correnti per la subnet per l'utilizzo per la rete virtuale usagetest.</span><span class="sxs-lookup"><span data-stu-id="80907-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="80907-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80907-110">PARAMETERS</span></span>

### <span data-ttu-id="80907-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80907-111">-DefaultProfile</span></span>
<span data-ttu-id="80907-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80907-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80907-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="80907-113">-Name</span></span>
<span data-ttu-id="80907-114">Specifica il nome della rete virtuale per cui visualizzare gli utilizzi.</span><span class="sxs-lookup"><span data-stu-id="80907-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="80907-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80907-115">-ResourceGroupName</span></span>
<span data-ttu-id="80907-116">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="80907-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="80907-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80907-117">CommonParameters</span></span>
<span data-ttu-id="80907-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80907-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80907-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80907-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80907-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80907-120">INPUTS</span></span>

### <span data-ttu-id="80907-121">System. String</span><span class="sxs-lookup"><span data-stu-id="80907-121">System.String</span></span>

## <span data-ttu-id="80907-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80907-122">OUTPUTS</span></span>

### <span data-ttu-id="80907-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="80907-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="80907-124">Note</span><span class="sxs-lookup"><span data-stu-id="80907-124">NOTES</span></span>

## <span data-ttu-id="80907-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80907-125">RELATED LINKS</span></span>
