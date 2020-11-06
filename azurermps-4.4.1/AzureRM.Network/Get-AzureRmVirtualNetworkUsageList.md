---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 618fdf2ebe32f365bce72353f6e148fa3059cf66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522110"
---
# <span data-ttu-id="81505-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="81505-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="81505-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81505-102">SYNOPSIS</span></span>
<span data-ttu-id="81505-103">Ottiene l'utilizzo corrente della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="81505-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81505-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81505-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81505-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81505-105">DESCRIPTION</span></span>
<span data-ttu-id="81505-106">Il cmdlet **Get-AzureRmVirtualNetworkUsageList** Ottiene l'utilizzo per ogni subnet per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="81505-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="81505-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81505-107">EXAMPLES</span></span>

### <span data-ttu-id="81505-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81505-108">Example 1</span></span>
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

<span data-ttu-id="81505-109">Ottiene i valori correnti per la subnet per l'utilizzo per la rete virtuale usagetest.</span><span class="sxs-lookup"><span data-stu-id="81505-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="81505-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81505-110">PARAMETERS</span></span>

### <span data-ttu-id="81505-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="81505-111">-Name</span></span>
<span data-ttu-id="81505-112">Specifica il nome della rete virtuale per cui visualizzare gli utilizzi.</span><span class="sxs-lookup"><span data-stu-id="81505-112">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="81505-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81505-113">-ResourceGroupName</span></span>
<span data-ttu-id="81505-114">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="81505-114">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="81505-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81505-115">-DefaultProfile</span></span>
<span data-ttu-id="81505-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81505-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81505-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81505-117">CommonParameters</span></span>
<span data-ttu-id="81505-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81505-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81505-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81505-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81505-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81505-120">INPUTS</span></span>

### <span data-ttu-id="81505-121">System. String</span><span class="sxs-lookup"><span data-stu-id="81505-121">System.String</span></span>

## <span data-ttu-id="81505-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81505-122">OUTPUTS</span></span>

### <span data-ttu-id="81505-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="81505-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="81505-124">Note</span><span class="sxs-lookup"><span data-stu-id="81505-124">NOTES</span></span>

## <span data-ttu-id="81505-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81505-125">RELATED LINKS</span></span>

