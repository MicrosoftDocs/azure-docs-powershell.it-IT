---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 659281d1f78ea984a3db30817d15a6e92f31cbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677743"
---
# <span data-ttu-id="64d1c-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64d1c-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="64d1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="64d1c-103">Ottiene una zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="64d1c-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="64d1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64d1c-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64d1c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="64d1c-106">Il cmdlet **Get-AzPrivateDnsZone** ottiene una zona DNS (private Domain Name System) dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="64d1c-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="64d1c-107">Se specifichi il parametro *Name* , viene restituito un singolo oggetto **PrivateDnsZone** .</span><span class="sxs-lookup"><span data-stu-id="64d1c-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="64d1c-108">Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutte le aree del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="64d1c-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="64d1c-109">Puoi usare l'oggetto **PrivateDnsZone** per aggiornare la zona, ad esempio puoi aggiungere oggetti **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="64d1c-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="64d1c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64d1c-110">EXAMPLES</span></span>

### <span data-ttu-id="64d1c-111">Esempio 1: ottenere una zona</span><span class="sxs-lookup"><span data-stu-id="64d1c-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="64d1c-112">Esempio 2: ottenere tutte le aree di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="64d1c-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="64d1c-113">Questo esempio recupera tutte le aree DNS private nel gruppo di risorse specificato e lo archivia nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="64d1c-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="64d1c-114">Esempio 3: ottenere tutte le aree di un abbonamento</span><span class="sxs-lookup"><span data-stu-id="64d1c-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="64d1c-115">Questo esempio consente di ottenere tutte le aree DNS private nell'abbonamento Azure corrente e quindi di archiviarle nella variabile $Zones.</span><span class="sxs-lookup"><span data-stu-id="64d1c-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="64d1c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64d1c-116">PARAMETERS</span></span>

### <span data-ttu-id="64d1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d1c-117">-DefaultProfile</span></span>
<span data-ttu-id="64d1c-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="64d1c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64d1c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="64d1c-119">-Name</span></span>
<span data-ttu-id="64d1c-120">Specifica il nome dell'area DNS privata da ottenere.</span><span class="sxs-lookup"><span data-stu-id="64d1c-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="64d1c-121">Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutte le aree DNS private nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="64d1c-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="64d1c-122">Se si omette anche il parametro *ResourceGroupName* , questo cmdlet ottiene tutte le aree DNS private nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="64d1c-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="64d1c-124">Specifica il nome del gruppo di risorse che contiene la zona privata DNS da ottenere.</span><span class="sxs-lookup"><span data-stu-id="64d1c-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="64d1c-125">Se non specifichi *ResourceGroupName* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="64d1c-125">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="64d1c-126">In questo caso, questo cmdlet ottiene tutte le aree DNS private nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="64d1c-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d1c-127">CommonParameters</span></span>
<span data-ttu-id="64d1c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d1c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d1c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d1c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64d1c-130">INPUTS</span></span>

### <span data-ttu-id="64d1c-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="64d1c-131">None</span></span>

## <span data-ttu-id="64d1c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64d1c-132">OUTPUTS</span></span>

### <span data-ttu-id="64d1c-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64d1c-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="64d1c-134">Note</span><span class="sxs-lookup"><span data-stu-id="64d1c-134">NOTES</span></span>

## <span data-ttu-id="64d1c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64d1c-135">RELATED LINKS</span></span>

[<span data-ttu-id="64d1c-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64d1c-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="64d1c-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64d1c-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="64d1c-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="64d1c-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)