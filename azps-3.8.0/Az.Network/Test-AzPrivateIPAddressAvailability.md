---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864638"
---
# <span data-ttu-id="72144-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="72144-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="72144-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72144-102">SYNOPSIS</span></span>
<span data-ttu-id="72144-103">Verificare la disponibilità di un indirizzo IP privato in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="72144-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="72144-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72144-104">SYNTAX</span></span>

### <span data-ttu-id="72144-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="72144-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72144-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="72144-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72144-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72144-107">DESCRIPTION</span></span>
<span data-ttu-id="72144-108">Il cmdlet **test-AzPrivateIPAddressAvailability** verifica se un indirizzo IP privato specificato è disponibile in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="72144-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="72144-109">Questo cmdlet restituisce un elenco di indirizzi IP privati disponibili se l'indirizzo IP privato richiesto viene acquisito.</span><span class="sxs-lookup"><span data-stu-id="72144-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="72144-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72144-110">EXAMPLES</span></span>

### <span data-ttu-id="72144-111">Esempio 1: verificare se un indirizzo IP è disponibile tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="72144-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="72144-112">Questo comando ottiene una rete virtuale e usa l'operatore pipeline per passarlo a **test-AzPrivateIPAddressAvailability** , che verifica se è disponibile l'indirizzo IP privato specificato.</span><span class="sxs-lookup"><span data-stu-id="72144-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="72144-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72144-113">PARAMETERS</span></span>

### <span data-ttu-id="72144-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72144-114">-DefaultProfile</span></span>
<span data-ttu-id="72144-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72144-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72144-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="72144-116">-IPAddress</span></span>
<span data-ttu-id="72144-117">Specifica l'indirizzo IP da testare.</span><span class="sxs-lookup"><span data-stu-id="72144-117">Specifies the IP address to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72144-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72144-118">-ResourceGroupName</span></span>
<span data-ttu-id="72144-119">Specifica il nome del gruppo di risorse per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="72144-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72144-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="72144-120">-VirtualNetwork</span></span>
<span data-ttu-id="72144-121">Specifica un oggetto **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="72144-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72144-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="72144-122">-VirtualNetworkName</span></span>
<span data-ttu-id="72144-123">Specifica il nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="72144-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72144-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72144-124">CommonParameters</span></span>
<span data-ttu-id="72144-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72144-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72144-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72144-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72144-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72144-127">INPUTS</span></span>

### <span data-ttu-id="72144-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="72144-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="72144-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72144-129">OUTPUTS</span></span>

### <span data-ttu-id="72144-130">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="72144-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="72144-131">Note</span><span class="sxs-lookup"><span data-stu-id="72144-131">NOTES</span></span>

## <span data-ttu-id="72144-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72144-132">RELATED LINKS</span></span>

[<span data-ttu-id="72144-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="72144-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


