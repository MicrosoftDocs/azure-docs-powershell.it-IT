---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 6ea456ca5e8d06c1ff732664127ca2e7a62abb2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520691"
---
# <span data-ttu-id="f31c3-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f31c3-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="f31c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f31c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f31c3-103">Rimuove il sito predefinito da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f31c3-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f31c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f31c3-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f31c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f31c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f31c3-106">Il cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito per il tunneling forzato da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f31c3-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="f31c3-107">Il tunneling forzato consente di reindirizzare il traffico associato a Internet da macchine virtuali di Azure alla rete locale; in questo modo è possibile ispezionare e controllare il traffico prima di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="f31c3-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="f31c3-108">Il tunneling forzato viene eseguito usando un tunnel VPN (Virtual Private Network); Questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.</span><span class="sxs-lookup"><span data-stu-id="f31c3-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="f31c3-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito assegnato a un gateway.</span><span class="sxs-lookup"><span data-stu-id="f31c3-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="f31c3-110">Se si esegue questa operazione, sarà necessario usare Set-AzureRmVirtualNetworkGatewayDefaultSite per assegnare un nuovo sito predefinito prima che il gateway possa essere usato per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="f31c3-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="f31c3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f31c3-111">EXAMPLES</span></span>

### <span data-ttu-id="f31c3-112">Esempio 1: rimuovere il sito predefinito assegnato a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f31c3-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="f31c3-113">In questo esempio viene rimosso il sito predefinito attualmente assegnato a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f31c3-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="f31c3-114">Il primo comando USA **Get-AzureRmVirtualNetworkGateway** per creare un riferimento a un oggetto al gateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f31c3-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="f31c3-115">Il secondo comando usa quindi **Remove-AzureRmVirtualNetworkGatewayDefaultSite** per rimuovere il sito predefinito assegnato a tale gateway.</span><span class="sxs-lookup"><span data-stu-id="f31c3-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="f31c3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f31c3-116">PARAMETERS</span></span>

### <span data-ttu-id="f31c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31c3-117">-DefaultProfile</span></span>
<span data-ttu-id="f31c3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f31c3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f31c3-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f31c3-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f31c3-120">Specifica un riferimento a un oggetto al gateway di rete virtuale che contiene il sito predefinito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f31c3-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="f31c3-121">Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando la Get-AzureRmVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="f31c3-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="f31c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31c3-122">CommonParameters</span></span>
<span data-ttu-id="f31c3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31c3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f31c3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31c3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f31c3-125">INPUTS</span></span>

###  
<span data-ttu-id="f31c3-126">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f31c3-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="f31c3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f31c3-127">OUTPUTS</span></span>

###  
<span data-ttu-id="f31c3-128">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="f31c3-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="f31c3-129">Note</span><span class="sxs-lookup"><span data-stu-id="f31c3-129">NOTES</span></span>

## <span data-ttu-id="f31c3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f31c3-130">RELATED LINKS</span></span>

[<span data-ttu-id="f31c3-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f31c3-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f31c3-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f31c3-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


