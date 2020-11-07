---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 367e5d74b9d2c1d29199a7af3c132e147b5ae620
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866251"
---
# <span data-ttu-id="6e95e-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6e95e-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="6e95e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e95e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e95e-103">Crea una configurazione del pool di indirizzi back-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6e95e-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e95e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e95e-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e95e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e95e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e95e-106">Il cmdlet **New-AzureRmLoadBalancerBackendAddressPoolConfig** crea una configurazione del pool di indirizzi back-end per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="6e95e-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="6e95e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e95e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e95e-108">Esempio 1: creare una configurazione del pool di indirizzi back-end per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6e95e-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="6e95e-109">Questo comando crea una configurazione del pool di indirizzi back-end denominata BackendAddressPool02 per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6e95e-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="6e95e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e95e-110">PARAMETERS</span></span>

### <span data-ttu-id="6e95e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e95e-111">-DefaultProfile</span></span>
<span data-ttu-id="6e95e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e95e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e95e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e95e-113">-Name</span></span>
<span data-ttu-id="6e95e-114">Specifica il nome della configurazione del pool di indirizzi da creare.</span><span class="sxs-lookup"><span data-stu-id="6e95e-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e95e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e95e-115">CommonParameters</span></span>
<span data-ttu-id="6e95e-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e95e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e95e-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e95e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e95e-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e95e-118">INPUTS</span></span>

## <span data-ttu-id="6e95e-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e95e-119">OUTPUTS</span></span>

### <span data-ttu-id="6e95e-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6e95e-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="6e95e-121">Note</span><span class="sxs-lookup"><span data-stu-id="6e95e-121">NOTES</span></span>

## <span data-ttu-id="6e95e-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e95e-122">RELATED LINKS</span></span>

[<span data-ttu-id="6e95e-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6e95e-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6e95e-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6e95e-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="6e95e-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="6e95e-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


