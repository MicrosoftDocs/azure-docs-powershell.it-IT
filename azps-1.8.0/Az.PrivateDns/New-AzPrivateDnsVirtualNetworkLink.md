---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 7d2a9a399e6582e2ff3815447570548ac62f6676
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677739"
---
# <span data-ttu-id="48629-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="48629-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="48629-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48629-102">SYNOPSIS</span></span>
<span data-ttu-id="48629-103">Crea un nuovo collegamento alla rete virtuale DNS privata.</span><span class="sxs-lookup"><span data-stu-id="48629-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="48629-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48629-104">SYNTAX</span></span>

### <span data-ttu-id="48629-105">VirtualNetworkId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48629-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48629-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="48629-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48629-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48629-107">DESCRIPTION</span></span>
<span data-ttu-id="48629-108">Il cmdlet **New-AzPrivateDnsVirtualNetworkLink** crea un nuovo collegamento di rete virtuale DNS (private Domain Name System) nel gruppo di risorse e nell'area privata specificati.</span><span class="sxs-lookup"><span data-stu-id="48629-108">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="48629-109">Devi specificare un nome di collegamento univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="48629-109">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="48629-110">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="48629-110">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="48629-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48629-111">EXAMPLES</span></span>

### <span data-ttu-id="48629-112">Esempio 1: creare un collegamento alla rete virtuale DNS privata</span><span class="sxs-lookup"><span data-stu-id="48629-112">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="48629-113">Questo comando crea un nuovo collegamento di rete virtuale associato alla zona DNS privata denominata myzone.com e Virtual Network "myvirtualnetwork" (che è già stato creato nel gruppo risorse) nel gruppo di risorse specificato e lo archivia nella variabile $Link.</span><span class="sxs-lookup"><span data-stu-id="48629-113">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="48629-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48629-114">PARAMETERS</span></span>

### <span data-ttu-id="48629-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48629-115">-DefaultProfile</span></span>
<span data-ttu-id="48629-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="48629-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48629-117">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="48629-117">-EnableRegistration</span></span>
<span data-ttu-id="48629-118">Parametro switch che rappresenta se il collegamento è abilitato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="48629-118">Switch parameter that represents if the link is registration enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48629-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="48629-119">-Name</span></span>
<span data-ttu-id="48629-120">Specifica il nome del collegamento alla rete virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="48629-120">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="48629-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48629-121">-ResourceGroupName</span></span>
<span data-ttu-id="48629-122">Specifica il gruppo di risorse in cui creare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="48629-122">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="48629-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="48629-123">-Tag</span></span>
<span data-ttu-id="48629-124">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="48629-124">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48629-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48629-125">-VirtualNetwork</span></span>
<span data-ttu-id="48629-126">Oggetto di rete virtuale associato al collegamento.</span><span class="sxs-lookup"><span data-stu-id="48629-126">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48629-127">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="48629-127">-VirtualNetworkId</span></span>
<span data-ttu-id="48629-128">ID risorsa della rete virtuale associata al collegamento.</span><span class="sxs-lookup"><span data-stu-id="48629-128">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48629-129">-Zonename</span><span class="sxs-lookup"><span data-stu-id="48629-129">-ZoneName</span></span>
<span data-ttu-id="48629-130">Specifica il nome della zona che verrà collegata al collegamento alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="48629-130">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="48629-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48629-131">-Confirm</span></span>
<span data-ttu-id="48629-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48629-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48629-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48629-133">-WhatIf</span></span>
<span data-ttu-id="48629-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48629-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48629-135">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48629-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48629-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48629-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48629-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48629-137">CommonParameters</span></span>
<span data-ttu-id="48629-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48629-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48629-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48629-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48629-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48629-140">INPUTS</span></span>

### <span data-ttu-id="48629-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="48629-141">None</span></span>

## <span data-ttu-id="48629-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48629-142">OUTPUTS</span></span>

### <span data-ttu-id="48629-143">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="48629-143">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="48629-144">Note</span><span class="sxs-lookup"><span data-stu-id="48629-144">NOTES</span></span>

## <span data-ttu-id="48629-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48629-145">RELATED LINKS</span></span>

[<span data-ttu-id="48629-146">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="48629-146">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="48629-147">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="48629-147">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="48629-148">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="48629-148">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
