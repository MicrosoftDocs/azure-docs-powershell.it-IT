---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: af5e1591e0d5c497b0cfe854235536d7edf404c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191558"
---
# <span data-ttu-id="e7b4c-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="e7b4c-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="e7b4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b4c-103">Testare la disponibilità di un indirizzo IP privato in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="e7b4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7b4c-104">SYNTAX</span></span>

### <span data-ttu-id="e7b4c-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="e7b4c-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7b4c-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b4c-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7b4c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e7b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="e7b4c-108">Il cmdlet **Test-AzPrivateIPAddressAvailability** verifica se un indirizzo IP privato specificato è disponibile in una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="e7b4c-109">Questo cmdlet restituisce un elenco di indirizzi IP privati disponibili se viene restituito l'indirizzo IP privato richiesto.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="e7b4c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7b4c-110">EXAMPLES</span></span>

### <span data-ttu-id="e7b4c-111">Esempio 1: Verificare se un indirizzo IP è disponibile usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="e7b4c-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="e7b4c-112">Questo comando ottiene una rete virtuale e usa l'operatore della pipeline per passare la rete **a Test-AzPrivateIPAddressAvailability,** che verifica se l'indirizzo IP privato specificato è disponibile.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="e7b4c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7b4c-113">PARAMETERS</span></span>

### <span data-ttu-id="e7b4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b4c-114">-DefaultProfile</span></span>
<span data-ttu-id="e7b4c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7b4c-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e7b4c-116">-IPAddress</span></span>
<span data-ttu-id="e7b4c-117">Specifica l'indirizzo IP da testare.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="e7b4c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b4c-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7b4c-119">Specifica il nome del gruppo di risorse per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="e7b4c-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7b4c-120">-VirtualNetwork</span></span>
<span data-ttu-id="e7b4c-121">Specifica un **oggetto PSVirtualNetwork.**</span><span class="sxs-lookup"><span data-stu-id="e7b4c-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="e7b4c-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e7b4c-122">-VirtualNetworkName</span></span>
<span data-ttu-id="e7b4c-123">Specifica il nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="e7b4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b4c-124">CommonParameters</span></span>
<span data-ttu-id="e7b4c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b4c-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b4c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b4c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e7b4c-127">INPUTS</span></span>

### <span data-ttu-id="e7b4c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7b4c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e7b4c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7b4c-129">OUTPUTS</span></span>

### <span data-ttu-id="e7b4c-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="e7b4c-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="e7b4c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e7b4c-131">NOTES</span></span>

## <span data-ttu-id="e7b4c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7b4c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e7b4c-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e7b4c-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


