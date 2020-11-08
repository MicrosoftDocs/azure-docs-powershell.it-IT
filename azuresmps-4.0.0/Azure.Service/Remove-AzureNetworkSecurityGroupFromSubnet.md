---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029612"
---
# <span data-ttu-id="7e64d-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="7e64d-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="7e64d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e64d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e64d-103">Dissocia un gruppo di sicurezza di rete da una subnet.</span><span class="sxs-lookup"><span data-stu-id="7e64d-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="7e64d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e64d-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e64d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e64d-105">DESCRIPTION</span></span>
<span data-ttu-id="7e64d-106">Il cmdlet **Remove-AzureNetworkSecurityGroupFromSubnet** dissocia un gruppo di sicurezza di rete di Azure da una subnet.</span><span class="sxs-lookup"><span data-stu-id="7e64d-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="7e64d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e64d-107">EXAMPLES</span></span>

## <span data-ttu-id="7e64d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e64d-108">PARAMETERS</span></span>

### <span data-ttu-id="7e64d-109">-Force</span><span class="sxs-lookup"><span data-stu-id="7e64d-109">-Force</span></span>
<span data-ttu-id="7e64d-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7e64d-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e64d-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e64d-111">-Name</span></span>
<span data-ttu-id="7e64d-112">Specifica il nome del gruppo di sicurezza della rete che questo cmdlet dissocia da una subnet.</span><span class="sxs-lookup"><span data-stu-id="7e64d-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="7e64d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e64d-113">-PassThru</span></span>
<span data-ttu-id="7e64d-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7e64d-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="7e64d-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7e64d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e64d-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="7e64d-116">-Profile</span></span>
<span data-ttu-id="7e64d-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e64d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7e64d-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7e64d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e64d-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7e64d-119">-SubnetName</span></span>
<span data-ttu-id="7e64d-120">Specifica il nome di una subnet da cui questo cmdlet dissocia un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="7e64d-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="7e64d-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7e64d-121">-VirtualNetworkName</span></span>
<span data-ttu-id="7e64d-122">Specifica il nome di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e64d-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="7e64d-123">Questo cmdlet Annulla l'associazione di un gruppo di sicurezza di rete da una subnet nella rete virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7e64d-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="7e64d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e64d-124">CommonParameters</span></span>
<span data-ttu-id="7e64d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e64d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e64d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e64d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e64d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e64d-127">INPUTS</span></span>

## <span data-ttu-id="7e64d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e64d-128">OUTPUTS</span></span>

## <span data-ttu-id="7e64d-129">Note</span><span class="sxs-lookup"><span data-stu-id="7e64d-129">NOTES</span></span>

## <span data-ttu-id="7e64d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e64d-130">RELATED LINKS</span></span>

[<span data-ttu-id="7e64d-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="7e64d-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="7e64d-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="7e64d-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


