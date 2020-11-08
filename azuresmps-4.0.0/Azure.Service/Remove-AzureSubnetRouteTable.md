---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029918"
---
# <span data-ttu-id="8b893-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b893-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="8b893-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b893-102">SYNOPSIS</span></span>
<span data-ttu-id="8b893-103">Rimuove un'associazione di tabella di route da una subnet.</span><span class="sxs-lookup"><span data-stu-id="8b893-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="8b893-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b893-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8b893-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b893-105">DESCRIPTION</span></span>
<span data-ttu-id="8b893-106">Il cmdlet **Remove-AzureSubnetRouteTable** rimuove un'associazione di tabella di route da una subnet.</span><span class="sxs-lookup"><span data-stu-id="8b893-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="8b893-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b893-107">EXAMPLES</span></span>

### <span data-ttu-id="8b893-108">Esempio 1: rimuovere un'associazione tra una tabella di route e una subnet</span><span class="sxs-lookup"><span data-stu-id="8b893-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="8b893-109">Questo comando consente di rimuovere l'associazione della tabella di route denominata PublicRouteTable alla subnet denominata ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="8b893-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="8b893-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b893-110">PARAMETERS</span></span>

### <span data-ttu-id="8b893-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8b893-111">-Force</span></span>
<span data-ttu-id="8b893-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8b893-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b893-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b893-113">-PassThru</span></span>
<span data-ttu-id="8b893-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8b893-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8b893-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8b893-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b893-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="8b893-116">-Profile</span></span>
<span data-ttu-id="8b893-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b893-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8b893-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8b893-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8b893-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8b893-119">-SubnetName</span></span>
<span data-ttu-id="8b893-120">Specifica la subnet per cui questo cmdlet rimuove la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="8b893-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="8b893-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8b893-121">-VirtualNetworkName</span></span>
<span data-ttu-id="8b893-122">Specifica il nome di una rete virtuale che contiene la subnet per cui questo cmdlet rimuove la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="8b893-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="8b893-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b893-123">CommonParameters</span></span>
<span data-ttu-id="8b893-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b893-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b893-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b893-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b893-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b893-126">INPUTS</span></span>

## <span data-ttu-id="8b893-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b893-127">OUTPUTS</span></span>

## <span data-ttu-id="8b893-128">Note</span><span class="sxs-lookup"><span data-stu-id="8b893-128">NOTES</span></span>

## <span data-ttu-id="8b893-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b893-129">RELATED LINKS</span></span>

[<span data-ttu-id="8b893-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b893-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="8b893-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="8b893-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


