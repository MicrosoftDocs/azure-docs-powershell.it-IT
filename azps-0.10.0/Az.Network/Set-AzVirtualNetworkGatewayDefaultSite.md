---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862721"
---
# <span data-ttu-id="35d81-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="35d81-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="35d81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35d81-102">SYNOPSIS</span></span>
<span data-ttu-id="35d81-103">Imposta il sito predefinito per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="35d81-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="35d81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35d81-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35d81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35d81-105">DESCRIPTION</span></span>
<span data-ttu-id="35d81-106">Il cmdlet **set-AzVirtualNetworkGatewayDefaultSite** assegna un sito predefinito per il tunneling forzato a un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="35d81-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="35d81-107">Il tunneling forzato consente di reindirizzare il traffico associato a Internet da macchine virtuali di Azure alla rete locale; in questo modo è possibile ispezionare e controllare il traffico prima di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="35d81-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="35d81-108">Il tunneling forzato viene eseguito usando un tunnel VPN (Virtual Private Network); Questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.</span><span class="sxs-lookup"><span data-stu-id="35d81-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="35d81-109">**Set-AzVirtualNetworkGatewayDefaultSite** offre un modo per cambiare il sito predefinito assegnato a un gateway.</span><span class="sxs-lookup"><span data-stu-id="35d81-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="35d81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35d81-110">EXAMPLES</span></span>

### <span data-ttu-id="35d81-111">Esempio 1: assegnare un sito predefinito a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="35d81-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="35d81-112">Questo esempio assegna un sito predefinito a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="35d81-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="35d81-113">Il primo comando crea un riferimento a un oggetto gateway locale denominato ContosoLocalGateway.</span><span class="sxs-lookup"><span data-stu-id="35d81-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="35d81-114">Questo riferimento oggetto archiviato nella variabile denominata $LocalGateway rappresenta il gateway da configurare come sito predefinito</span><span class="sxs-lookup"><span data-stu-id="35d81-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="35d81-115">.</span><span class="sxs-lookup"><span data-stu-id="35d81-115">.</span></span>
<span data-ttu-id="35d81-116">Il secondo comando crea quindi un riferimento a un oggetto al gateway di rete virtuale e archivia il risultato nella variabile denominata $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="35d81-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="35d81-117">Il terzo comando usa il cmdlet **set-AzVirtualNetworkGatewayDefaultSite** per assegnare il sito predefinito a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="35d81-117">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="35d81-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35d81-118">PARAMETERS</span></span>

### <span data-ttu-id="35d81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d81-119">-DefaultProfile</span></span>
<span data-ttu-id="35d81-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35d81-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35d81-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="35d81-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="35d81-122">Specifica un riferimento a un oggetto al gateway di rete locale da assegnare come sito predefinito per la rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="35d81-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="35d81-123">Puoi usare il cmdlet Get-AzLocalNetworkGateway per creare un riferimento a un oggetto in un gateway locale.</span><span class="sxs-lookup"><span data-stu-id="35d81-123">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="35d81-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35d81-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="35d81-125">Specifica un riferimento a un oggetto al gateway di rete virtuale in cui verrà assegnato il sito predefinito.</span><span class="sxs-lookup"><span data-stu-id="35d81-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="35d81-126">Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando il **Get-AzVirtualNetworkGateway** e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="35d81-126">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="35d81-127">La variabile $VirtualGateway può quindi essere usata come valore di parametro per il parametro *VirtualNetworkGateway* :</span><span class="sxs-lookup"><span data-stu-id="35d81-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="35d81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d81-128">CommonParameters</span></span>
<span data-ttu-id="35d81-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d81-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d81-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d81-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35d81-131">INPUTS</span></span>

###  
<span data-ttu-id="35d81-132">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="35d81-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="35d81-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35d81-133">OUTPUTS</span></span>

###  
<span data-ttu-id="35d81-134">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="35d81-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="35d81-135">Note</span><span class="sxs-lookup"><span data-stu-id="35d81-135">NOTES</span></span>

## <span data-ttu-id="35d81-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35d81-136">RELATED LINKS</span></span>

[<span data-ttu-id="35d81-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35d81-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="35d81-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35d81-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="35d81-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="35d81-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


