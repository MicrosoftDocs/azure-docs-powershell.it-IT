---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033104"
---
# <span data-ttu-id="bb799-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb799-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="bb799-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb799-102">SYNOPSIS</span></span>
<span data-ttu-id="bb799-103">Ottiene una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="bb799-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="bb799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb799-104">SYNTAX</span></span>

### <span data-ttu-id="bb799-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb799-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb799-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb799-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb799-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb799-107">DESCRIPTION</span></span>
<span data-ttu-id="bb799-108">Il cmdlet **Get-AzDnsZone** ottiene una zona DNS (Domain Name System) dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="bb799-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="bb799-109">Se specifichi il parametro *Name* , viene restituito un singolo oggetto **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="bb799-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="bb799-110">Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutte le aree del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="bb799-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="bb799-111">Puoi usare l'oggetto **dnsZone** per aggiornare la zona, ad esempio puoi aggiungere oggetti **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="bb799-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="bb799-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb799-112">EXAMPLES</span></span>

### <span data-ttu-id="bb799-113">Esempio 1: ottenere una zona</span><span class="sxs-lookup"><span data-stu-id="bb799-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="bb799-114">Questo esempio recupera la zona DNS denominata myzone.com dal gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="bb799-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="bb799-115">Esempio 2: ottenere tutte le aree di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bb799-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="bb799-116">Questo esempio recupera tutte le aree DNS nel gruppo di risorse specificato e lo archivia nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="bb799-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="bb799-117">Esempio 3: ottenere tutte le aree di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="bb799-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="bb799-118">Questo esempio consente di ottenere tutte le aree DNS nell'abbonamento Azure corrente e quindi di archiviarle nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="bb799-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="bb799-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb799-119">PARAMETERS</span></span>

### <span data-ttu-id="bb799-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb799-120">-DefaultProfile</span></span>
<span data-ttu-id="bb799-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb799-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb799-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb799-122">-Name</span></span>
<span data-ttu-id="bb799-123">Specifica il nome della zona DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bb799-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="bb799-124">Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutte le aree DNS nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="bb799-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="bb799-125">Se si omette anche il parametro *ResourceGroupName* , questo cmdlet recupera tutte le aree DNS nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="bb799-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="bb799-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb799-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb799-127">Specifica il nome del gruppo di risorse che contiene la zona DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bb799-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="bb799-128">Se non specifichi *ResourceGroupName* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="bb799-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="bb799-129">In questo caso, questo cmdlet ottiene tutte le aree DNS nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="bb799-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="bb799-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb799-130">CommonParameters</span></span>
<span data-ttu-id="bb799-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb799-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb799-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb799-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb799-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb799-133">INPUTS</span></span>

### <span data-ttu-id="bb799-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bb799-134">System.String</span></span>

## <span data-ttu-id="bb799-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb799-135">OUTPUTS</span></span>

### <span data-ttu-id="bb799-136">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="bb799-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="bb799-137">Note</span><span class="sxs-lookup"><span data-stu-id="bb799-137">NOTES</span></span>

## <span data-ttu-id="bb799-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb799-138">RELATED LINKS</span></span>

[<span data-ttu-id="bb799-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb799-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="bb799-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb799-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="bb799-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb799-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
