---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023423"
---
# <span data-ttu-id="a6a91-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a6a91-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="a6a91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6a91-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a91-103">Reimposta un gateway VPN di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a6a91-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="a6a91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6a91-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6a91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6a91-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a91-106">Il cmdlet **Reset-AzureVNetGateway** Reimposta e riavvia un gateway di rete virtuale (VPN) Virtual Private Network.</span><span class="sxs-lookup"><span data-stu-id="a6a91-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="a6a91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6a91-107">EXAMPLES</span></span>

### <span data-ttu-id="a6a91-108">Esempio 1: reimpostare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a6a91-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="a6a91-109">Questo comando Reimposta il gateway di rete virtuale dalla rete virtuale denominata ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="a6a91-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="a6a91-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6a91-110">PARAMETERS</span></span>

### <span data-ttu-id="a6a91-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="a6a91-111">-Profile</span></span>
<span data-ttu-id="a6a91-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6a91-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a6a91-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a6a91-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6a91-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a6a91-114">-VNetName</span></span>
<span data-ttu-id="a6a91-115">Specifica la rete virtuale che contiene il gateway di rete virtuale che questo cmdlet Reimposta.</span><span class="sxs-lookup"><span data-stu-id="a6a91-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="a6a91-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a91-116">CommonParameters</span></span>
<span data-ttu-id="a6a91-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a91-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a91-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a91-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a91-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6a91-119">INPUTS</span></span>

## <span data-ttu-id="a6a91-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6a91-120">OUTPUTS</span></span>

## <span data-ttu-id="a6a91-121">Note</span><span class="sxs-lookup"><span data-stu-id="a6a91-121">NOTES</span></span>

## <span data-ttu-id="a6a91-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6a91-122">RELATED LINKS</span></span>

[<span data-ttu-id="a6a91-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a6a91-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="a6a91-124">New-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a6a91-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="a6a91-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a6a91-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="a6a91-126">Ridimensionare-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="a6a91-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="a6a91-127">Set-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="a6a91-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


