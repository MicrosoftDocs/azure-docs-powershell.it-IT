---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsZone.md
ms.openlocfilehash: eabf0809aebf50458d15b195a5ec9afc4f0b9cf1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687527"
---
# <span data-ttu-id="edff0-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="edff0-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="edff0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edff0-102">SYNOPSIS</span></span>
<span data-ttu-id="edff0-103">Ottiene una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="edff0-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edff0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edff0-104">SYNTAX</span></span>

### <span data-ttu-id="edff0-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="edff0-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edff0-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="edff0-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edff0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edff0-107">DESCRIPTION</span></span>
<span data-ttu-id="edff0-108">Il cmdlet **Get-AzureRmDnsZone** ottiene una zona DNS (Domain Name System) dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="edff0-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="edff0-109">Se specifichi il parametro *Name* , viene restituito un singolo oggetto **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="edff0-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="edff0-110">Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutte le aree del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="edff0-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="edff0-111">Puoi usare l'oggetto **dnsZone** per aggiornare la zona, ad esempio puoi aggiungere oggetti **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="edff0-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="edff0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edff0-112">EXAMPLES</span></span>

### <span data-ttu-id="edff0-113">Esempio 1: ottenere una zona</span><span class="sxs-lookup"><span data-stu-id="edff0-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="edff0-114">Questo esempio recupera la zona DNS denominata myzone.com dal gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="edff0-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="edff0-115">Esempio 2: ottenere tutte le aree di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="edff0-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="edff0-116">Questo esempio recupera tutte le aree DNS nel gruppo di risorse specificato e lo archivia nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="edff0-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="edff0-117">Esempio 3: ottenere tutte le aree di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="edff0-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="edff0-118">Questo esempio consente di ottenere tutte le aree DNS nell'abbonamento Azure corrente e quindi di archiviarle nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="edff0-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="edff0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edff0-119">PARAMETERS</span></span>

### <span data-ttu-id="edff0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="edff0-120">-Name</span></span>
<span data-ttu-id="edff0-121">Specifica il nome della zona DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="edff0-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="edff0-122">Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutte le aree DNS nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="edff0-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="edff0-123">Se si omette anche il parametro *ResourceGroupName* , questo cmdlet recupera tutte le aree DNS nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="edff0-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edff0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edff0-124">-ResourceGroupName</span></span>
<span data-ttu-id="edff0-125">Specifica il nome del gruppo di risorse che contiene la zona DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="edff0-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="edff0-126">Se non specifichi *ResourceGroupName* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="edff0-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="edff0-127">In questo caso, questo cmdlet ottiene tutte le aree DNS nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="edff0-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edff0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edff0-128">-DefaultProfile</span></span>
<span data-ttu-id="edff0-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edff0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edff0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edff0-130">CommonParameters</span></span>
<span data-ttu-id="edff0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edff0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edff0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edff0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edff0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edff0-133">INPUTS</span></span>

### <span data-ttu-id="edff0-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="edff0-134">None</span></span>
<span data-ttu-id="edff0-135">Questo cmdlet non consente di reindirizzare l'input.</span><span class="sxs-lookup"><span data-stu-id="edff0-135">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="edff0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edff0-136">OUTPUTS</span></span>

### <span data-ttu-id="edff0-137">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="edff0-137">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="edff0-138">Questo cmdlet restituisce un oggetto che rappresenta la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="edff0-138">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="edff0-139">Se il nome della zona non è specificato, viene restituita una matrice di oggetti zone.</span><span class="sxs-lookup"><span data-stu-id="edff0-139">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="edff0-140">Note</span><span class="sxs-lookup"><span data-stu-id="edff0-140">NOTES</span></span>

## <span data-ttu-id="edff0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edff0-141">RELATED LINKS</span></span>

[<span data-ttu-id="edff0-142">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="edff0-142">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="edff0-143">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="edff0-143">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="edff0-144">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="edff0-144">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
