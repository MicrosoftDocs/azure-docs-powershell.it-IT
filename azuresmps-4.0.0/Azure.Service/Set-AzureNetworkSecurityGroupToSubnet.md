---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023787"
---
# <span data-ttu-id="3269a-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="3269a-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="3269a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3269a-102">SYNOPSIS</span></span>
<span data-ttu-id="3269a-103">Associa un gruppo di sicurezza di rete a una subnet.</span><span class="sxs-lookup"><span data-stu-id="3269a-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="3269a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3269a-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3269a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3269a-105">DESCRIPTION</span></span>
<span data-ttu-id="3269a-106">Il cmdlet **set-AzureNetworkSecurityGroupToSubnet** associa un gruppo di sicurezza di rete Azure a una subnet.</span><span class="sxs-lookup"><span data-stu-id="3269a-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="3269a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3269a-107">EXAMPLES</span></span>

## <span data-ttu-id="3269a-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3269a-108">PARAMETERS</span></span>

### <span data-ttu-id="3269a-109">-Force</span><span class="sxs-lookup"><span data-stu-id="3269a-109">-Force</span></span>
<span data-ttu-id="3269a-110">Indica che questo cmdlet non chiede di confermare la rimozione di un gruppo di sicurezza di rete precedente dalla subnet.</span><span class="sxs-lookup"><span data-stu-id="3269a-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="3269a-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="3269a-111">-Name</span></span>
<span data-ttu-id="3269a-112">Specifica il nome del gruppo di sicurezza della rete che questo cmdlet associa a una subnet.</span><span class="sxs-lookup"><span data-stu-id="3269a-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3269a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3269a-113">-PassThru</span></span>
<span data-ttu-id="3269a-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3269a-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3269a-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3269a-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3269a-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="3269a-116">-Profile</span></span>
<span data-ttu-id="3269a-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3269a-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3269a-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3269a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3269a-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3269a-119">-SubnetName</span></span>
<span data-ttu-id="3269a-120">Specifica il nome di una subnet a cui questo cmdlet associa un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="3269a-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="3269a-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3269a-121">-VirtualNetworkName</span></span>
<span data-ttu-id="3269a-122">Specifica il nome di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3269a-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="3269a-123">Questo cmdlet associa un gruppo di sicurezza di rete a una subnet nella rete virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3269a-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="3269a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3269a-124">CommonParameters</span></span>
<span data-ttu-id="3269a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3269a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3269a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3269a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3269a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3269a-127">INPUTS</span></span>

## <span data-ttu-id="3269a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3269a-128">OUTPUTS</span></span>

## <span data-ttu-id="3269a-129">Note</span><span class="sxs-lookup"><span data-stu-id="3269a-129">NOTES</span></span>

## <span data-ttu-id="3269a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3269a-130">RELATED LINKS</span></span>

[<span data-ttu-id="3269a-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="3269a-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="3269a-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="3269a-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


