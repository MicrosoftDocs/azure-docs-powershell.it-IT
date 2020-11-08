---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023447"
---
# <span data-ttu-id="5d5cd-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5d5cd-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="5d5cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5cd-103">Rimuove la route predefinita per il traffico di tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="5d5cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d5cd-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5d5cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d5cd-105">DESCRIPTION</span></span>
<span data-ttu-id="5d5cd-106">Il cmdlet **Remove-AzureVNetGatewayDefaultSite** rimuove la route predefinita al sito locale per il traffico di tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="5d5cd-107">Questo cmdlet consente di rimuovere la route da un gateway di rete privata virtuale (VPN) di Azure per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="5d5cd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d5cd-108">EXAMPLES</span></span>

### <span data-ttu-id="5d5cd-109">Esempio 1: rimuovere una route per il sito predefinito</span><span class="sxs-lookup"><span data-stu-id="5d5cd-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="5d5cd-110">Questo comando consente di rimuovere la route al sito predefinito dalla VPN della rete virtuale denominata ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="5d5cd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d5cd-111">PARAMETERS</span></span>

### <span data-ttu-id="5d5cd-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="5d5cd-112">-Profile</span></span>
<span data-ttu-id="5d5cd-113">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d5cd-114">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5cd-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5d5cd-115">-VNetName</span></span>
<span data-ttu-id="5d5cd-116">Specifica una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-116">Specifies a virtual network.</span></span>
<span data-ttu-id="5d5cd-117">Questo cmdlet consente di rimuovere la route predefinita dal gateway VPN per la rete virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="5d5cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5cd-118">CommonParameters</span></span>
<span data-ttu-id="5d5cd-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5cd-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5cd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5cd-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d5cd-121">INPUTS</span></span>

## <span data-ttu-id="5d5cd-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d5cd-122">OUTPUTS</span></span>

## <span data-ttu-id="5d5cd-123">Note</span><span class="sxs-lookup"><span data-stu-id="5d5cd-123">NOTES</span></span>

## <span data-ttu-id="5d5cd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d5cd-124">RELATED LINKS</span></span>

[<span data-ttu-id="5d5cd-125">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5d5cd-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
