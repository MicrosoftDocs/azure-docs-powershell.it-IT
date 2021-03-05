---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: fc0e3ad0bcc86a0ad49450393a79c6c60540ba23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001054"
---
# <span data-ttu-id="d325a-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="d325a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d325a-102">SYNOPSIS</span></span>
<span data-ttu-id="d325a-103">Aggiorna un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="d325a-103">Updates a private link service.</span></span>

## <span data-ttu-id="d325a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d325a-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d325a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d325a-105">DESCRIPTION</span></span>
<span data-ttu-id="d325a-106">Il cmdlet **Set-AzPrivateLinkService** aggiorna un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="d325a-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="d325a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d325a-107">EXAMPLES</span></span>

### <span data-ttu-id="d325a-108">1: crea un servizio di collegamento privato e ne aggiorna il</span><span class="sxs-lookup"><span data-stu-id="d325a-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="d325a-109">In questo esempio viene creato un servizio di collegamento privato denominato mypls.</span><span class="sxs-lookup"><span data-stu-id="d325a-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="d325a-110">Quindi sostituisce le sue ipConfigurations dall'oggetto ipConfiguratiuon in memoria.</span><span class="sxs-lookup"><span data-stu-id="d325a-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="d325a-111">Il Set-AzPrivateLinkService cmdlet di collegamento privato viene quindi usato per scrivere lo stato modificato del servizio di collegamento privato sul lato servizio.</span><span class="sxs-lookup"><span data-stu-id="d325a-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="d325a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d325a-112">PARAMETERS</span></span>

### <span data-ttu-id="d325a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d325a-113">-AsJob</span></span>
<span data-ttu-id="d325a-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d325a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d325a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d325a-115">-DefaultProfile</span></span>
<span data-ttu-id="d325a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d325a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d325a-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-117">-PrivateLinkService</span></span>
<span data-ttu-id="d325a-118">Specifica un oggetto servizio di collegamento privato che rappresenta lo stato su cui deve essere impostato il servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="d325a-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="d325a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d325a-119">CommonParameters</span></span>
<span data-ttu-id="d325a-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d325a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d325a-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d325a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d325a-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d325a-122">INPUTS</span></span>

### <span data-ttu-id="d325a-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d325a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d325a-124">OUTPUTS</span></span>

### <span data-ttu-id="d325a-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d325a-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d325a-126">NOTES</span></span>

## <span data-ttu-id="d325a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d325a-127">RELATED LINKS</span></span>

[<span data-ttu-id="d325a-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="d325a-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="d325a-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d325a-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


