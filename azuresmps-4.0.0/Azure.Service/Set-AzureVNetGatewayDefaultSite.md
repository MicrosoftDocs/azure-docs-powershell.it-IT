---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029875"
---
# <span data-ttu-id="c9fbf-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c9fbf-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="c9fbf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fbf-103">Imposta il sito predefinito per il traffico di tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="c9fbf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9fbf-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9fbf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9fbf-105">DESCRIPTION</span></span>
<span data-ttu-id="c9fbf-106">Il cmdlet **set-AzureVNetGatewayDefaultSite** imposta la route predefinita per il sito locale per il traffico di tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="c9fbf-107">Questo comando imposta la route su un gateway di rete privata virtuale (VPN) di Azure per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="c9fbf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9fbf-108">EXAMPLES</span></span>

## <span data-ttu-id="c9fbf-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9fbf-109">PARAMETERS</span></span>

### <span data-ttu-id="c9fbf-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="c9fbf-110">-DefaultSite</span></span>
<span data-ttu-id="c9fbf-111">Specifica il nome del sito di rete locale locali per il traffico di tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="c9fbf-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9fbf-112">-Profile</span></span>
<span data-ttu-id="c9fbf-113">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9fbf-114">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9fbf-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c9fbf-115">-VNetName</span></span>
<span data-ttu-id="c9fbf-116">Specifica una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-116">Specifies a virtual network.</span></span>
<span data-ttu-id="c9fbf-117">Questo cmdlet imposta la route predefinita del gateway VPN per il traffico di tunneling forzato per la rete virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="c9fbf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fbf-118">CommonParameters</span></span>
<span data-ttu-id="c9fbf-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9fbf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fbf-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fbf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fbf-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9fbf-121">INPUTS</span></span>

## <span data-ttu-id="c9fbf-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9fbf-122">OUTPUTS</span></span>

## <span data-ttu-id="c9fbf-123">Note</span><span class="sxs-lookup"><span data-stu-id="c9fbf-123">NOTES</span></span>

## <span data-ttu-id="c9fbf-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9fbf-124">RELATED LINKS</span></span>

[<span data-ttu-id="c9fbf-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c9fbf-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
