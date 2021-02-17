---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191598"
---
# <span data-ttu-id="5aeed-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5aeed-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="5aeed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aeed-102">SYNOPSIS</span></span>
<span data-ttu-id="5aeed-103">Imposta il sito predefinito per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5aeed-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="5aeed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5aeed-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aeed-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5aeed-105">DESCRIPTION</span></span>
<span data-ttu-id="5aeed-106">Il cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** assegna un sito predefinito di tunneling forzato a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5aeed-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="5aeed-107">Il tunneling forzato consente di reindirizzare il traffico associato a Internet dalle macchine virtuali di Azure alla rete locale; in questo modo è possibile controllare e controllare il traffico prima di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="5aeed-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="5aeed-108">Il tunneling forzato viene eseguito usando un tunnel VPN; questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.</span><span class="sxs-lookup"><span data-stu-id="5aeed-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="5aeed-109">**Set-AzVirtualNetworkGatewayDefaultSite** consente di cambiare il sito predefinito assegnato a un gateway.</span><span class="sxs-lookup"><span data-stu-id="5aeed-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="5aeed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5aeed-110">EXAMPLES</span></span>

### <span data-ttu-id="5aeed-111">Esempio 1: Assegnare un sito predefinito a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="5aeed-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="5aeed-112">Questo esempio assegna un sito predefinito a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5aeed-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="5aeed-113">Il primo comando crea un riferimento a un oggetto a un gateway locale denominato ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="5aeed-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="5aeed-114">Questo riferimento all'oggetto archiviato nella variabile $LocalGateway rappresenta il gateway da configurare come sito predefinito.</span><span class="sxs-lookup"><span data-stu-id="5aeed-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="5aeed-115">Il secondo comando crea quindi un riferimento a un oggetto al gateway di rete virtuale e archivia il risultato nella variabile $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5aeed-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="5aeed-116">Il terzo comando usa il cmdlet **Set-AzVirtualNetworkGatewayDefaultSite** per assegnare il sito predefinito a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5aeed-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="5aeed-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aeed-117">PARAMETERS</span></span>

### <span data-ttu-id="5aeed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aeed-118">-DefaultProfile</span></span>
<span data-ttu-id="5aeed-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5aeed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aeed-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5aeed-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="5aeed-121">Specifica un riferimento a un oggetto al gateway di rete locale da assegnare come sito predefinito per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="5aeed-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="5aeed-122">È possibile usare il cmdlet Get-AzLocalNetworkGateway per creare un riferimento a un oggetto a un gateway locale.</span><span class="sxs-lookup"><span data-stu-id="5aeed-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aeed-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5aeed-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5aeed-124">Specifica un riferimento a un oggetto al gateway di rete virtuale a cui verrà assegnato il sito predefinito.</span><span class="sxs-lookup"><span data-stu-id="5aeed-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="5aeed-125">È possibile creare un riferimento a un oggetto a un gateway di rete virtuale usando **Get-AzVirtualNetworkGateway** e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="5aeed-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="5aeed-126">La variabile $VirtualGateway può essere usata come valore del parametro *VirtualNetworkGateway:*</span><span class="sxs-lookup"><span data-stu-id="5aeed-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5aeed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aeed-127">CommonParameters</span></span>
<span data-ttu-id="5aeed-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aeed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aeed-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aeed-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aeed-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="5aeed-130">INPUTS</span></span>

### <span data-ttu-id="5aeed-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5aeed-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="5aeed-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5aeed-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="5aeed-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5aeed-133">OUTPUTS</span></span>

### <span data-ttu-id="5aeed-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5aeed-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="5aeed-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="5aeed-135">NOTES</span></span>

## <span data-ttu-id="5aeed-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5aeed-136">RELATED LINKS</span></span>

[<span data-ttu-id="5aeed-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5aeed-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="5aeed-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5aeed-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5aeed-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5aeed-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


