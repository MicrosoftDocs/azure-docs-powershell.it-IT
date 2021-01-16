---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351415"
---
# <span data-ttu-id="9e46c-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="9e46c-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="9e46c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e46c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e46c-103">Rimuove il sito predefinito da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e46c-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="9e46c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e46c-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e46c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e46c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e46c-106">Il cmdlet **Remove-AzVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito per il tunneling forzato da un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e46c-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="9e46c-107">Il tunneling forzato consente di reindirizzare il traffico associato a Internet da macchine virtuali di Azure alla rete locale; in questo modo è possibile ispezionare e controllare il traffico prima di rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="9e46c-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="9e46c-108">Il tunneling forzato viene eseguito usando un tunnel VPN (Virtual Private Network); Questo tunnel richiede un sito predefinito, un gateway locale in cui viene reindirizzato tutto il traffico associato a Internet di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e46c-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="9e46c-109">**Remove-AzVirtualNetworkGatewayDefaultSite** rimuove il sito predefinito assegnato a un gateway.</span><span class="sxs-lookup"><span data-stu-id="9e46c-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="9e46c-110">Se si esegue questa operazione, sarà necessario usare Set-AzVirtualNetworkGatewayDefaultSite per assegnare un nuovo sito predefinito prima che il gateway possa essere usato per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="9e46c-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="9e46c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e46c-111">EXAMPLES</span></span>

### <span data-ttu-id="9e46c-112">Esempio 1: rimuovere il sito predefinito assegnato a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="9e46c-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="9e46c-113">In questo esempio viene rimosso il sito predefinito attualmente assegnato a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="9e46c-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="9e46c-114">Il primo comando USA **Get-AzVirtualNetworkGateway** per creare un riferimento a un oggetto al gateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9e46c-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="9e46c-115">Il secondo comando usa quindi **Remove-AzVirtualNetworkGatewayDefaultSite** per rimuovere il sito predefinito assegnato a tale gateway.</span><span class="sxs-lookup"><span data-stu-id="9e46c-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="9e46c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e46c-116">PARAMETERS</span></span>

### <span data-ttu-id="9e46c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e46c-117">-DefaultProfile</span></span>
<span data-ttu-id="9e46c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e46c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e46c-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e46c-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="9e46c-120">Specifica un riferimento a un oggetto al gateway di rete virtuale che contiene il sito predefinito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9e46c-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="9e46c-121">Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando la Get-AzVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="9e46c-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="9e46c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e46c-122">CommonParameters</span></span>
<span data-ttu-id="9e46c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e46c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e46c-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e46c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e46c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e46c-125">INPUTS</span></span>

### <span data-ttu-id="9e46c-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e46c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e46c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e46c-127">OUTPUTS</span></span>

### <span data-ttu-id="9e46c-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e46c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="9e46c-129">Note</span><span class="sxs-lookup"><span data-stu-id="9e46c-129">NOTES</span></span>

## <span data-ttu-id="9e46c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e46c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e46c-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9e46c-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="9e46c-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="9e46c-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


