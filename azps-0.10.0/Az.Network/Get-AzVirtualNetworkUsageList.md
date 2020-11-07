---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 07c7d0e099cb5b83a0f98cfe8404be7e79b0427a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860630"
---
# <span data-ttu-id="3a727-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="3a727-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="3a727-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a727-102">SYNOPSIS</span></span>
<span data-ttu-id="3a727-103">Ottiene l'utilizzo corrente della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a727-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="3a727-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a727-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a727-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a727-105">DESCRIPTION</span></span>
<span data-ttu-id="3a727-106">Il cmdlet **Get-AzVirtualNetworkUsageList** Ottiene l'utilizzo per ogni subnet per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="3a727-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="3a727-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a727-107">EXAMPLES</span></span>

### <span data-ttu-id="3a727-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a727-108">Example 1</span></span>
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

<span data-ttu-id="3a727-109">Ottiene i valori correnti per la subnet per l'utilizzo per la rete virtuale usagetest.</span><span class="sxs-lookup"><span data-stu-id="3a727-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="3a727-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a727-110">PARAMETERS</span></span>

### <span data-ttu-id="3a727-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a727-111">-DefaultProfile</span></span>
<span data-ttu-id="3a727-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a727-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a727-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a727-113">-Name</span></span>
<span data-ttu-id="3a727-114">Specifica il nome della rete virtuale per cui visualizzare gli utilizzi.</span><span class="sxs-lookup"><span data-stu-id="3a727-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a727-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a727-115">-ResourceGroupName</span></span>
<span data-ttu-id="3a727-116">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3a727-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a727-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a727-117">CommonParameters</span></span>
<span data-ttu-id="3a727-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a727-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a727-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a727-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a727-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a727-120">INPUTS</span></span>

### <span data-ttu-id="3a727-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3a727-121">System.String</span></span>

## <span data-ttu-id="3a727-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a727-122">OUTPUTS</span></span>

### <span data-ttu-id="3a727-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="3a727-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="3a727-124">Note</span><span class="sxs-lookup"><span data-stu-id="3a727-124">NOTES</span></span>

## <span data-ttu-id="3a727-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a727-125">RELATED LINKS</span></span>

