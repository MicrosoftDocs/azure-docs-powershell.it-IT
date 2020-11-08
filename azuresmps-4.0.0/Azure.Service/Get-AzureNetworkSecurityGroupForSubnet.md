---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023596"
---
# <span data-ttu-id="4cac5-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="4cac5-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="4cac5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cac5-102">SYNOPSIS</span></span>
<span data-ttu-id="4cac5-103">Ottiene il gruppo di sicurezza di rete per una subnet.</span><span class="sxs-lookup"><span data-stu-id="4cac5-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="4cac5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cac5-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4cac5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cac5-105">DESCRIPTION</span></span>
<span data-ttu-id="4cac5-106">Il cmdlet **Get-AzureNetworkSecurityGroupForSubnet** ottiene il gruppo di sicurezza di rete associato a una subnet.</span><span class="sxs-lookup"><span data-stu-id="4cac5-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="4cac5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cac5-107">EXAMPLES</span></span>

## <span data-ttu-id="4cac5-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cac5-108">PARAMETERS</span></span>

### <span data-ttu-id="4cac5-109">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="4cac5-109">-Detailed</span></span>
<span data-ttu-id="4cac5-110">Indica che questo cmdlet Visualizza le regole di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="4cac5-110">Indicates that this cmdlet displays the network security rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cac5-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="4cac5-111">-Profile</span></span>
<span data-ttu-id="4cac5-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cac5-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4cac5-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4cac5-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4cac5-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4cac5-114">-SubnetName</span></span>
<span data-ttu-id="4cac5-115">Specifica il nome di una subnet per cui questo cmdlet ottiene un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4cac5-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="4cac5-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4cac5-116">-VirtualNetworkName</span></span>
<span data-ttu-id="4cac5-117">Specifica il nome di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4cac5-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="4cac5-118">Questo cmdlet consente di ottenere un gruppo di sicurezza di rete per una subnet nella rete virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="4cac5-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cac5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cac5-119">CommonParameters</span></span>
<span data-ttu-id="4cac5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cac5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cac5-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cac5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cac5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cac5-122">INPUTS</span></span>

## <span data-ttu-id="4cac5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cac5-123">OUTPUTS</span></span>

## <span data-ttu-id="4cac5-124">Note</span><span class="sxs-lookup"><span data-stu-id="4cac5-124">NOTES</span></span>

## <span data-ttu-id="4cac5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cac5-125">RELATED LINKS</span></span>

[<span data-ttu-id="4cac5-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="4cac5-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="4cac5-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="4cac5-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
