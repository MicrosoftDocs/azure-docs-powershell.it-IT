---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866696"
---
# <span data-ttu-id="a42c8-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a42c8-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="a42c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a42c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a42c8-103">Ottiene una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a42c8-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a42c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a42c8-104">SYNTAX</span></span>

### <span data-ttu-id="a42c8-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a42c8-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="a42c8-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a42c8-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="a42c8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a42c8-107">DESCRIPTION</span></span>
<span data-ttu-id="a42c8-108">Il cmdlet **Get-AzureRmDnsZone** ottiene una zona DNS (Domain Name System) dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a42c8-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="a42c8-109">Se specifichi il parametro *Name* , viene restituito un singolo oggetto **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="a42c8-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="a42c8-110">Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutte le aree del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a42c8-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="a42c8-111">Puoi usare l'oggetto **dnsZone** per aggiornare la zona, ad esempio puoi aggiungere oggetti **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a42c8-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="a42c8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a42c8-112">EXAMPLES</span></span>

### <span data-ttu-id="a42c8-113">Esempio 1: ottenere una zona</span><span class="sxs-lookup"><span data-stu-id="a42c8-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="a42c8-114">Questo esempio recupera la zona DNS denominata myzone.com dal gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="a42c8-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a42c8-115">Esempio 2: ottenere tutte le aree di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a42c8-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a42c8-116">Questo esempio recupera tutte le aree DNS nel gruppo di risorse specificato e lo archivia nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="a42c8-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="a42c8-117">Esempio 3: ottenere tutte le aree di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a42c8-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="a42c8-118">Questo esempio consente di ottenere tutte le aree DNS nell'abbonamento Azure corrente e quindi di archiviarle nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="a42c8-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="a42c8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a42c8-119">PARAMETERS</span></span>

### <span data-ttu-id="a42c8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a42c8-120">-Name</span></span>
<span data-ttu-id="a42c8-121">Specifica il nome della zona DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a42c8-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="a42c8-122">Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutte le aree DNS nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a42c8-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="a42c8-123">Se si omette anche il parametro *ResourceGroupName* , questo cmdlet recupera tutte le aree DNS nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a42c8-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a42c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="a42c8-125">Specifica il nome del gruppo di risorse che contiene la zona DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a42c8-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="a42c8-126">Se non specifichi *ResourceGroupName* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="a42c8-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="a42c8-127">In questo caso, questo cmdlet ottiene tutte le aree DNS nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="a42c8-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a42c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42c8-128">CommonParameters</span></span>
<span data-ttu-id="a42c8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42c8-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42c8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a42c8-131">INPUTS</span></span>

### <span data-ttu-id="a42c8-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a42c8-132">None</span></span>
<span data-ttu-id="a42c8-133">Questo cmdlet non consente di reindirizzare l'input.</span><span class="sxs-lookup"><span data-stu-id="a42c8-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="a42c8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a42c8-134">OUTPUTS</span></span>

### <span data-ttu-id="a42c8-135">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a42c8-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a42c8-136">Questo cmdlet restituisce un oggetto che rappresenta la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a42c8-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="a42c8-137">Se il nome della zona non è specificato, viene restituita una matrice di oggetti zone.</span><span class="sxs-lookup"><span data-stu-id="a42c8-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="a42c8-138">Note</span><span class="sxs-lookup"><span data-stu-id="a42c8-138">NOTES</span></span>

## <span data-ttu-id="a42c8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a42c8-139">RELATED LINKS</span></span>

[<span data-ttu-id="a42c8-140">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a42c8-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="a42c8-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a42c8-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="a42c8-142">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a42c8-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
