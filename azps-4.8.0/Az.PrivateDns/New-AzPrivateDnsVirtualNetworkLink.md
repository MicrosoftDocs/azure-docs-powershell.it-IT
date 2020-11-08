---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192224"
---
# <span data-ttu-id="60ca6-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="60ca6-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="60ca6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="60ca6-103">Crea un nuovo collegamento alla rete virtuale DNS privata.</span><span class="sxs-lookup"><span data-stu-id="60ca6-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="60ca6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60ca6-104">SYNTAX</span></span>

### <span data-ttu-id="60ca6-105">VirtualNetworkId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60ca6-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ca6-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="60ca6-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ca6-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="60ca6-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60ca6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="60ca6-109">Il cmdlet **New-AzPrivateDnsVirtualNetworkLink** crea un nuovo collegamento di rete virtuale DNS (private Domain Name System) nel gruppo di risorse e nell'area privata specificati.</span><span class="sxs-lookup"><span data-stu-id="60ca6-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="60ca6-110">Devi specificare un nome di collegamento univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="60ca6-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="60ca6-111">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="60ca6-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="60ca6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60ca6-112">EXAMPLES</span></span>

### <span data-ttu-id="60ca6-113">Esempio 1: creare un collegamento alla rete virtuale DNS privata</span><span class="sxs-lookup"><span data-stu-id="60ca6-113">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="60ca6-114">Questo comando crea un nuovo collegamento di rete virtuale associato alla zona DNS privata denominata myzone.com e Virtual Network "myvirtualnetwork" (che è già stato creato nel gruppo risorse) nel gruppo di risorse specificato e lo archivia nella variabile $Link.</span><span class="sxs-lookup"><span data-stu-id="60ca6-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="60ca6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60ca6-115">PARAMETERS</span></span>

### <span data-ttu-id="60ca6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ca6-116">-DefaultProfile</span></span>
<span data-ttu-id="60ca6-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="60ca6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60ca6-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="60ca6-118">-EnableRegistration</span></span>
<span data-ttu-id="60ca6-119">Parametro switch che rappresenta se il collegamento è abilitato per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="60ca6-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="60ca6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60ca6-120">-Name</span></span>
<span data-ttu-id="60ca6-121">Specifica il nome del collegamento alla rete virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="60ca6-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="60ca6-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="60ca6-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="60ca6-123">ID risorsa della rete virtuale in un altro tenant.</span><span class="sxs-lookup"><span data-stu-id="60ca6-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ca6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ca6-124">-ResourceGroupName</span></span>
<span data-ttu-id="60ca6-125">Specifica il gruppo di risorse in cui creare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="60ca6-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="60ca6-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="60ca6-126">-Tag</span></span>
<span data-ttu-id="60ca6-127">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="60ca6-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="60ca6-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="60ca6-128">-VirtualNetwork</span></span>
<span data-ttu-id="60ca6-129">Oggetto di rete virtuale associato al collegamento.</span><span class="sxs-lookup"><span data-stu-id="60ca6-129">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="60ca6-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="60ca6-130">-VirtualNetworkId</span></span>
<span data-ttu-id="60ca6-131">ID risorsa della rete virtuale associata al collegamento.</span><span class="sxs-lookup"><span data-stu-id="60ca6-131">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="60ca6-132">-Zonename</span><span class="sxs-lookup"><span data-stu-id="60ca6-132">-ZoneName</span></span>
<span data-ttu-id="60ca6-133">Specifica il nome della zona che verrà collegata al collegamento alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="60ca6-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="60ca6-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60ca6-134">-Confirm</span></span>
<span data-ttu-id="60ca6-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60ca6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60ca6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60ca6-136">-WhatIf</span></span>
<span data-ttu-id="60ca6-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60ca6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60ca6-138">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60ca6-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60ca6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60ca6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60ca6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ca6-140">CommonParameters</span></span>
<span data-ttu-id="60ca6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ca6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ca6-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60ca6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ca6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60ca6-143">INPUTS</span></span>

### <span data-ttu-id="60ca6-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="60ca6-144">None</span></span>

## <span data-ttu-id="60ca6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60ca6-145">OUTPUTS</span></span>

### <span data-ttu-id="60ca6-146">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="60ca6-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="60ca6-147">Note</span><span class="sxs-lookup"><span data-stu-id="60ca6-147">NOTES</span></span>

## <span data-ttu-id="60ca6-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60ca6-148">RELATED LINKS</span></span>

[<span data-ttu-id="60ca6-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="60ca6-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="60ca6-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="60ca6-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="60ca6-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="60ca6-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
