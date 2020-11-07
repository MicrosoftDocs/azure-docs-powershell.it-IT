---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3aea2414a4b7fdfbc14e65d4d087bb7e31206aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855905"
---
# <span data-ttu-id="edde9-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="edde9-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="edde9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edde9-102">SYNOPSIS</span></span>
<span data-ttu-id="edde9-103">Ottiene un collegamento di rete virtuale associato alla zona DNS privata specificata.</span><span class="sxs-lookup"><span data-stu-id="edde9-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="edde9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edde9-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edde9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edde9-105">DESCRIPTION</span></span>
<span data-ttu-id="edde9-106">Il cmdlet **Get-AzPrivateDnsVirtualNetworkLink** ottiene i collegamenti di rete virtuali associati a una determinata zona privata DNS dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="edde9-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="edde9-107">Se specifichi il parametro *Name* , viene restituito un singolo oggetto **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="edde9-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="edde9-108">Se non specifichi il parametro *Name* , viene restituita una matrice contenente tutti i collegamenti associati alla zona nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="edde9-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="edde9-109">Puoi usare l'oggetto **PSPrivateDnsVirtualNetworkLink** per aggiornare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="edde9-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="edde9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edde9-110">EXAMPLES</span></span>

### <span data-ttu-id="edde9-111">Esempio 1: ottenere un collegamento di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="edde9-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="edde9-112">Questo esempio ottiene il collegamento di rete virtuale associato alla zona DNS privata denominata myzone.com dal gruppo di risorse specificato e lo archivia nella variabile $Link.</span><span class="sxs-lookup"><span data-stu-id="edde9-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="edde9-113">Esempio 2: ottenere tutti i collegamenti associati a un'area di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="edde9-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="edde9-114">Questo esempio recupera tutti i collegamenti di rete virtuali associati alla zona DNS privata "myzone.com" nel gruppo di risorse specificato e lo archivia nella variabile $Links.</span><span class="sxs-lookup"><span data-stu-id="edde9-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="edde9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edde9-115">PARAMETERS</span></span>

### <span data-ttu-id="edde9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edde9-116">-DefaultProfile</span></span>
<span data-ttu-id="edde9-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="edde9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edde9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="edde9-118">-Name</span></span>
<span data-ttu-id="edde9-119">Specifica il nome del collegamento alla rete virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="edde9-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="edde9-120">Se non specifichi un valore per il parametro *Name* , questo cmdlet ottiene tutti i collegamenti associati alla zona DNS privata specificata nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="edde9-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="edde9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edde9-121">-ResourceGroupName</span></span>
<span data-ttu-id="edde9-122">Specifica il nome del gruppo di risorse che contiene il collegamento alla rete virtuale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="edde9-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde9-123">-Zonename</span><span class="sxs-lookup"><span data-stu-id="edde9-123">-ZoneName</span></span>
<span data-ttu-id="edde9-124">Specifica il nome dell'area DNS privata a cui è collegato il collegamento alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="edde9-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edde9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edde9-125">CommonParameters</span></span>
<span data-ttu-id="edde9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edde9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edde9-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edde9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edde9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edde9-128">INPUTS</span></span>

### <span data-ttu-id="edde9-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="edde9-129">None</span></span>

## <span data-ttu-id="edde9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edde9-130">OUTPUTS</span></span>

### <span data-ttu-id="edde9-131">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="edde9-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="edde9-132">Note</span><span class="sxs-lookup"><span data-stu-id="edde9-132">NOTES</span></span>

## <span data-ttu-id="edde9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edde9-133">RELATED LINKS</span></span>

[<span data-ttu-id="edde9-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="edde9-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="edde9-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="edde9-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="edde9-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="edde9-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
