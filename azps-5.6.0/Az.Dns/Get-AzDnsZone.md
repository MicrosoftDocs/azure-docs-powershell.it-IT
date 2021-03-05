---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: a788cf3638d124dac164f19171f1be89afc2e385
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984827"
---
# <span data-ttu-id="3c461-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3c461-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="3c461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c461-102">SYNOPSIS</span></span>
<span data-ttu-id="3c461-103">Ottiene un'area DNS.</span><span class="sxs-lookup"><span data-stu-id="3c461-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="3c461-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c461-104">SYNTAX</span></span>

### <span data-ttu-id="3c461-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c461-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c461-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3c461-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c461-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3c461-107">DESCRIPTION</span></span>
<span data-ttu-id="3c461-108">Il cmdlet **Get-AzDnsZone** ottiene un'area DNS (Domain Name System) dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="3c461-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="3c461-109">Se si specifica il *parametro Name,* viene restituito **un singolo oggetto DnsZone.**</span><span class="sxs-lookup"><span data-stu-id="3c461-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="3c461-110">Se non si specifica il *parametro Name,* verrà restituita una matrice contenente tutte le aree del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="3c461-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="3c461-111">È possibile usare **l'oggetto DnsZone** per aggiornare l'area, ad esempio è possibile aggiungervi oggetti **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="3c461-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="3c461-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c461-112">EXAMPLES</span></span>

### <span data-ttu-id="3c461-113">Esempio 1: Ottenere un'area</span><span class="sxs-lookup"><span data-stu-id="3c461-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="3c461-114">Questo esempio recupera l'area DNS myzone.com denominata dal gruppo di risorse specificato e quindi la archivia nella $Zone variabile.</span><span class="sxs-lookup"><span data-stu-id="3c461-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="3c461-115">Esempio 2: Ottenere tutte le aree in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3c461-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3c461-116">Questo esempio recupera tutte le zone DNS del gruppo di risorse specificato e quindi le archivia nella $Zones variabile.</span><span class="sxs-lookup"><span data-stu-id="3c461-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="3c461-117">Esempio 3: Ottenere tutte le aree in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="3c461-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="3c461-118">Questo esempio recupera tutte le aree DNS nella sottoscrizione di Azure corrente e quindi le archivia nella variabile $Zones dominio.</span><span class="sxs-lookup"><span data-stu-id="3c461-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="3c461-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c461-119">PARAMETERS</span></span>

### <span data-ttu-id="3c461-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c461-120">-DefaultProfile</span></span>
<span data-ttu-id="3c461-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3c461-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c461-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3c461-122">-Name</span></span>
<span data-ttu-id="3c461-123">Specifica il nome dell'area DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3c461-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="3c461-124">Se non si specifica un valore per il parametro *Name,* questo cmdlet ottiene tutte le zone DNS del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="3c461-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="3c461-125">Se si omette anche il *parametro ResourceGroupName,* questo cmdlet ottiene tutte le zone DNS nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="3c461-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="3c461-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c461-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c461-127">Specifica il nome del gruppo di risorse che contiene l'area DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="3c461-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="3c461-128">Se non si specifica *ResourceGroupName,* è necessario omettere anche il *parametro Name.*</span><span class="sxs-lookup"><span data-stu-id="3c461-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="3c461-129">In questo caso, questo cmdlet ottiene tutte le aree DNS nella sottoscrizione di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="3c461-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="3c461-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c461-130">CommonParameters</span></span>
<span data-ttu-id="3c461-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c461-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c461-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c461-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c461-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3c461-133">INPUTS</span></span>

### <span data-ttu-id="3c461-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3c461-134">System.String</span></span>

## <span data-ttu-id="3c461-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c461-135">OUTPUTS</span></span>

### <span data-ttu-id="3c461-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="3c461-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="3c461-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="3c461-137">NOTES</span></span>

## <span data-ttu-id="3c461-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c461-138">RELATED LINKS</span></span>

[<span data-ttu-id="3c461-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3c461-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="3c461-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3c461-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="3c461-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="3c461-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
