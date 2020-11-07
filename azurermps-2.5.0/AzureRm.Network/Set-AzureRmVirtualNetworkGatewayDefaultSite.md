---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: 463951ca6b6679671f330a3ddb0f9460a878a3d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866648"
---
# <span data-ttu-id="1d041-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1d041-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="1d041-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d041-102">SYNOPSIS</span></span>
<span data-ttu-id="1d041-103">Imposta il sito predefinito per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d041-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d041-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d041-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d041-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d041-105">DESCRIPTION</span></span>
<span data-ttu-id="1d041-106">Il cmdlet **set-AzureRmVirtualNetworkGatewayDefaultSite** assegna un sito predefinito per il tunneling forzato a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d041-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="1d041-107">Il tunneling forzato consente di reindirizzare il traffico associato a Internet da macchine virtuali di Azure alla rete locale; in questo modo è possibile ispezionare e controllare il traffico prima di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="1d041-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="1d041-108">Il tunneling forzato viene eseguito usando un tunnel VPN (Virtual Private Network); Questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d041-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="1d041-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** offre un modo per cambiare il sito predefinito assegnato a un gateway.</span><span class="sxs-lookup"><span data-stu-id="1d041-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="1d041-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d041-110">EXAMPLES</span></span>

### <span data-ttu-id="1d041-111">Esempio 1: assegnare un sito predefinito a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1d041-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="1d041-112">Questo esempio assegna un sito predefinito a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1d041-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="1d041-113">Il primo comando crea un riferimento a un oggetto gateway locale denominato ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="1d041-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="1d041-114">Questo riferimento oggetto archiviato nella variabile denominata $LocalGateway rappresenta il gateway da configurare come sito predefinito</span><span class="sxs-lookup"><span data-stu-id="1d041-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="1d041-115">.</span><span class="sxs-lookup"><span data-stu-id="1d041-115">.</span></span>
<span data-ttu-id="1d041-116">Il secondo comando crea quindi un riferimento a un oggetto al gateway di rete virtuale e archivia il risultato nella variabile denominata $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1d041-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="1d041-117">Il terzo comando usa il cmdlet **set-AzureRmVirtualNetworkGatewayDefaultSite** per assegnare il sito predefinito a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="1d041-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="1d041-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d041-118">PARAMETERS</span></span>

### <span data-ttu-id="1d041-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d041-119">-DefaultProfile</span></span>
<span data-ttu-id="1d041-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d041-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d041-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1d041-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="1d041-122">Specifica un riferimento a un oggetto al gateway di rete locale da assegnare come sito predefinito per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="1d041-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="1d041-123">Puoi usare il cmdlet Get-AzureRmLocalNetworkGateway per creare un riferimento a un oggetto in un gateway locale.</span><span class="sxs-lookup"><span data-stu-id="1d041-123">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d041-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d041-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1d041-125">Specifica un riferimento a un oggetto al gateway di rete virtuale in cui verrà assegnato il sito predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d041-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="1d041-126">Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando il **Get-AzureRmVirtualNetworkGateway** e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="1d041-126">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="1d041-127">La variabile $VirtualGateway può quindi essere usata come valore di parametro per il parametro *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="1d041-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d041-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d041-128">CommonParameters</span></span>
<span data-ttu-id="1d041-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d041-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d041-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d041-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d041-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d041-131">INPUTS</span></span>

###  
<span data-ttu-id="1d041-132">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="1d041-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="1d041-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d041-133">OUTPUTS</span></span>

###  
<span data-ttu-id="1d041-134">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="1d041-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="1d041-135">Note</span><span class="sxs-lookup"><span data-stu-id="1d041-135">NOTES</span></span>

## <span data-ttu-id="1d041-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d041-136">RELATED LINKS</span></span>

[<span data-ttu-id="1d041-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d041-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="1d041-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1d041-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="1d041-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1d041-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


