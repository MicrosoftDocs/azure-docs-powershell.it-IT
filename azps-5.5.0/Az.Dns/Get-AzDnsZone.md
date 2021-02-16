---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204155"
---
# <span data-ttu-id="5f978-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5f978-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="5f978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f978-102">SYNOPSIS</span></span>
<span data-ttu-id="5f978-103">Ottiene un'area DNS.</span><span class="sxs-lookup"><span data-stu-id="5f978-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="5f978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f978-104">SYNTAX</span></span>

### <span data-ttu-id="5f978-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f978-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f978-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5f978-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f978-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f978-107">DESCRIPTION</span></span>
<span data-ttu-id="5f978-108">Il cmdlet **Get-AzDnsZone** ottiene un'area DNS (Domain Name System) dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f978-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="5f978-109">Se si specifica il *parametro Name,* viene restituito **un singolo oggetto DnsZone.**</span><span class="sxs-lookup"><span data-stu-id="5f978-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="5f978-110">Se non si specifica il *parametro Name,* verrà restituita una matrice contenente tutte le aree del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f978-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="5f978-111">È possibile usare **l'oggetto DnsZone** per aggiornare l'area, ad esempio è possibile aggiungervi oggetti **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="5f978-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="5f978-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f978-112">EXAMPLES</span></span>

### <span data-ttu-id="5f978-113">Esempio 1: Ottenere un'area</span><span class="sxs-lookup"><span data-stu-id="5f978-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="5f978-114">Questo esempio recupera l'area DNS myzone.com denominata dns dal gruppo di risorse specificato e quindi la archivia nella $Zone variabile.</span><span class="sxs-lookup"><span data-stu-id="5f978-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="5f978-115">Esempio 2: Recuperare tutte le aree in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5f978-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5f978-116">Questo esempio recupera tutte le zone DNS del gruppo di risorse specificato e quindi le archivia nella $Zones variabile.</span><span class="sxs-lookup"><span data-stu-id="5f978-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="5f978-117">Esempio 3: Ottenere tutte le aree in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="5f978-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="5f978-118">Questo esempio recupera tutte le aree DNS nella sottoscrizione di Azure corrente e quindi le archivia nella variabile $Zones dominio.</span><span class="sxs-lookup"><span data-stu-id="5f978-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="5f978-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f978-119">PARAMETERS</span></span>

### <span data-ttu-id="5f978-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f978-120">-DefaultProfile</span></span>
<span data-ttu-id="5f978-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5f978-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f978-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5f978-122">-Name</span></span>
<span data-ttu-id="5f978-123">Specifica il nome dell'area DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5f978-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="5f978-124">Se non si specifica un valore per il parametro *Name,* questo cmdlet ottiene tutte le zone DNS del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f978-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="5f978-125">Se si omette anche il *parametro ResourceGroupName,* questo cmdlet ottiene tutte le zone DNS nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="5f978-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="5f978-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f978-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f978-127">Specifica il nome del gruppo di risorse che contiene l'area DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5f978-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="5f978-128">Se non si specifica *ResourceGroupName,* è necessario omettere anche il *parametro Name.*</span><span class="sxs-lookup"><span data-stu-id="5f978-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="5f978-129">In questo caso, questo cmdlet ottiene tutte le aree DNS nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="5f978-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="5f978-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f978-130">CommonParameters</span></span>
<span data-ttu-id="5f978-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f978-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f978-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f978-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f978-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f978-133">INPUTS</span></span>

### <span data-ttu-id="5f978-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5f978-134">System.String</span></span>

## <span data-ttu-id="5f978-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f978-135">OUTPUTS</span></span>

### <span data-ttu-id="5f978-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="5f978-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="5f978-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f978-137">NOTES</span></span>

## <span data-ttu-id="5f978-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f978-138">RELATED LINKS</span></span>

[<span data-ttu-id="5f978-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5f978-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="5f978-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5f978-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="5f978-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5f978-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
