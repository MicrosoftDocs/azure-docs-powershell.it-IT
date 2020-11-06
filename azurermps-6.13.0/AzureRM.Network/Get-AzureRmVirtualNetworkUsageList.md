---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 855385b55922f6255b407ceafef7422113968516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513748"
---
# <span data-ttu-id="53efc-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="53efc-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="53efc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53efc-102">SYNOPSIS</span></span>
<span data-ttu-id="53efc-103">Ottiene l'utilizzo corrente della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="53efc-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53efc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53efc-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53efc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53efc-105">DESCRIPTION</span></span>
<span data-ttu-id="53efc-106">Il cmdlet **Get-AzureRmVirtualNetworkUsageList** Ottiene l'utilizzo per ogni subnet per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="53efc-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="53efc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53efc-107">EXAMPLES</span></span>

### <span data-ttu-id="53efc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53efc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="53efc-109">Ottiene i valori correnti per la subnet per l'utilizzo per la rete virtuale usagetest.</span><span class="sxs-lookup"><span data-stu-id="53efc-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="53efc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53efc-110">PARAMETERS</span></span>

### <span data-ttu-id="53efc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53efc-111">-DefaultProfile</span></span>
<span data-ttu-id="53efc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53efc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53efc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="53efc-113">-Name</span></span>
<span data-ttu-id="53efc-114">Specifica il nome della rete virtuale per cui visualizzare gli utilizzi.</span><span class="sxs-lookup"><span data-stu-id="53efc-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="53efc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53efc-115">-ResourceGroupName</span></span>
<span data-ttu-id="53efc-116">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="53efc-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="53efc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53efc-117">CommonParameters</span></span>
<span data-ttu-id="53efc-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53efc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53efc-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53efc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53efc-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53efc-120">INPUTS</span></span>

### <span data-ttu-id="53efc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="53efc-121">System.String</span></span>

## <span data-ttu-id="53efc-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53efc-122">OUTPUTS</span></span>

### <span data-ttu-id="53efc-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="53efc-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="53efc-124">Note</span><span class="sxs-lookup"><span data-stu-id="53efc-124">NOTES</span></span>

## <span data-ttu-id="53efc-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53efc-125">RELATED LINKS</span></span>
