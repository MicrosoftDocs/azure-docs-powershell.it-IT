---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 769f8a5f8f95e5a97af8a495e0edbaba6b75a5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515532"
---
# <span data-ttu-id="1b9d5-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="1b9d5-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="1b9d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9d5-103">Verificare la disponibilità di un indirizzo IP privato in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b9d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b9d5-104">SYNTAX</span></span>

### <span data-ttu-id="1b9d5-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="1b9d5-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b9d5-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b9d5-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b9d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b9d5-107">DESCRIPTION</span></span>
<span data-ttu-id="1b9d5-108">Il cmdlet **test-AzureRmPrivateIPAddressAvailability** verifica se un indirizzo IP privato specificato è disponibile in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="1b9d5-109">Questo cmdlet restituisce un elenco di indirizzi IP privati disponibili se l'indirizzo IP privato richiesto viene acquisito.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="1b9d5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b9d5-110">EXAMPLES</span></span>

### <span data-ttu-id="1b9d5-111">Esempio 1: verificare se un indirizzo IP è disponibile tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="1b9d5-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="1b9d5-112">Questo comando ottiene una rete virtuale e usa l'operatore pipeline per passarlo a **test-AzureRmPrivateIPAddressAvailability** , che verifica se è disponibile l'indirizzo IP privato specificato.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="1b9d5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b9d5-113">PARAMETERS</span></span>

### <span data-ttu-id="1b9d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9d5-114">-DefaultProfile</span></span>
<span data-ttu-id="1b9d5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b9d5-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="1b9d5-116">-IPAddress</span></span>
<span data-ttu-id="1b9d5-117">Specifica l'indirizzo IP da testare.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="1b9d5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9d5-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b9d5-119">Specifica il nome del gruppo di risorse per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9d5-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1b9d5-120">-VirtualNetwork</span></span>
<span data-ttu-id="1b9d5-121">Specifica un oggetto **PSVirtualNetwork** .</span><span class="sxs-lookup"><span data-stu-id="1b9d5-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9d5-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1b9d5-122">-VirtualNetworkName</span></span>
<span data-ttu-id="1b9d5-123">Specifica il nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9d5-124">CommonParameters</span></span>
<span data-ttu-id="1b9d5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9d5-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9d5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b9d5-127">INPUTS</span></span>

### <span data-ttu-id="1b9d5-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1b9d5-128">PSVirtualNetwork</span></span>
<span data-ttu-id="1b9d5-129">Il parametro ' VirtualNetwork ' accetta il valore di tipo ' PSVirtualNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1b9d5-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1b9d5-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b9d5-130">OUTPUTS</span></span>

### <span data-ttu-id="1b9d5-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="1b9d5-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="1b9d5-132">Note</span><span class="sxs-lookup"><span data-stu-id="1b9d5-132">NOTES</span></span>

## <span data-ttu-id="1b9d5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b9d5-133">RELATED LINKS</span></span>

[<span data-ttu-id="1b9d5-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1b9d5-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


