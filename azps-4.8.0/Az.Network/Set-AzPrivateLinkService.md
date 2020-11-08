---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188380"
---
# <span data-ttu-id="7bc14-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="7bc14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bc14-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc14-103">Aggiorna un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7bc14-103">Updates a private link service.</span></span>

## <span data-ttu-id="7bc14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bc14-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bc14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bc14-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc14-106">Il cmdlet **set-AzPrivateLinkService** aggiorna un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7bc14-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="7bc14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bc14-107">EXAMPLES</span></span>

### <span data-ttu-id="7bc14-108">1: crea un servizio di collegamento privato e lo aggiorna</span><span class="sxs-lookup"><span data-stu-id="7bc14-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="7bc14-109">Questo esempio crea un servizio di collegamento privato denominato mypls.</span><span class="sxs-lookup"><span data-stu-id="7bc14-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="7bc14-110">Quindi sostituisce il relativo ipConfigurations dall'oggetto ipConfiguratiuon in memoria.</span><span class="sxs-lookup"><span data-stu-id="7bc14-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="7bc14-111">Il cmdlet Set-AzPrivateLinkService viene quindi usato per scrivere lo stato del servizio di collegamento privato modificato sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="7bc14-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="7bc14-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bc14-112">PARAMETERS</span></span>

### <span data-ttu-id="7bc14-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bc14-113">-AsJob</span></span>
<span data-ttu-id="7bc14-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7bc14-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc14-115">-DefaultProfile</span></span>
<span data-ttu-id="7bc14-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc14-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc14-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-117">-PrivateLinkService</span></span>
<span data-ttu-id="7bc14-118">Specifica un oggetto del servizio di collegamento privato che rappresenta lo stato in cui deve essere impostato il servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="7bc14-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc14-119">CommonParameters</span></span>
<span data-ttu-id="7bc14-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc14-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bc14-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc14-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bc14-122">INPUTS</span></span>

### <span data-ttu-id="7bc14-123">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7bc14-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bc14-124">OUTPUTS</span></span>

### <span data-ttu-id="7bc14-125">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7bc14-126">Note</span><span class="sxs-lookup"><span data-stu-id="7bc14-126">NOTES</span></span>

## <span data-ttu-id="7bc14-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bc14-127">RELATED LINKS</span></span>

[<span data-ttu-id="7bc14-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="7bc14-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="7bc14-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7bc14-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

