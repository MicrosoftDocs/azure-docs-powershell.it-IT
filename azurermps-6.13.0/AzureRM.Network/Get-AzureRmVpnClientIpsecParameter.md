---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513736"
---
# <span data-ttu-id="bfdcb-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bfdcb-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="bfdcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfdcb-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdcb-103">Ottiene i parametri IPSec VPN impostati sul gateway di rete virtuale per le connessioni punto a sito.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfdcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfdcb-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfdcb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfdcb-105">DESCRIPTION</span></span>
<span data-ttu-id="bfdcb-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="bfdcb-107">Il cmdlet **Get-AzureRmVpnClientIpsecParameter** restituisce l'oggetto dei parametri IPSec VPN impostati nel gateway in Azure in base al nome del gateway e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="bfdcb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfdcb-108">EXAMPLES</span></span>

### <span data-ttu-id="bfdcb-109">1: ottiene i parametri IPSec VPN impostati sul gateway di rete virtuale per le connessioni a un punto.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="bfdcb-110">Restituisce l'oggetto dei parametri IPSec VPN impostati nel gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="bfdcb-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="bfdcb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfdcb-111">PARAMETERS</span></span>

### <span data-ttu-id="bfdcb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdcb-112">-DefaultProfile</span></span>
<span data-ttu-id="bfdcb-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfdcb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfdcb-114">-Name</span></span>
<span data-ttu-id="bfdcb-115">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfdcb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfdcb-116">-ResourceGroupName</span></span>
<span data-ttu-id="bfdcb-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-117">The resource group name.</span></span>

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

### <span data-ttu-id="bfdcb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdcb-118">CommonParameters</span></span>
<span data-ttu-id="bfdcb-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfdcb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdcb-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfdcb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdcb-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfdcb-121">INPUTS</span></span>

### <span data-ttu-id="bfdcb-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bfdcb-122">System.String</span></span>

## <span data-ttu-id="bfdcb-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfdcb-123">OUTPUTS</span></span>

### <span data-ttu-id="bfdcb-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="bfdcb-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="bfdcb-125">Note</span><span class="sxs-lookup"><span data-stu-id="bfdcb-125">NOTES</span></span>

## <span data-ttu-id="bfdcb-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfdcb-126">RELATED LINKS</span></span>
