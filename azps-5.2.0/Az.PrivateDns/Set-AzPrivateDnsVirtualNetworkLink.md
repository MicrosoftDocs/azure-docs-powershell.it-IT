---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341779"
---
# <span data-ttu-id="4337b-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4337b-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4337b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4337b-102">SYNOPSIS</span></span>
<span data-ttu-id="4337b-103">Aggiorna/imposta un collegamento di rete virtuale associato a un'area privata e a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4337b-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="4337b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4337b-104">SYNTAX</span></span>

### <span data-ttu-id="4337b-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4337b-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4337b-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="4337b-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4337b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4337b-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4337b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4337b-108">DESCRIPTION</span></span>
<span data-ttu-id="4337b-109">Il cmdlet **set-AzPrivateDnsVirtualNetworkLink** aggiorna un collegamento associato a una zona da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4337b-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="4337b-110">Puoi passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *link* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4337b-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4337b-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="4337b-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4337b-112">Quando specifichi la zona usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), il collegamento non viene aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="4337b-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="4337b-113">Ciò offre protezione per le modifiche simultanee del collegamento.</span><span class="sxs-lookup"><span data-stu-id="4337b-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="4337b-114">Questa operazione può essere eliminata usando il parametro *overwrite* , che aggiorna il collegamento indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="4337b-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="4337b-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4337b-115">EXAMPLES</span></span>

### <span data-ttu-id="4337b-116">Esempio 1: impostare un collegamento</span><span class="sxs-lookup"><span data-stu-id="4337b-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

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

<span data-ttu-id="4337b-117">Questo comando imposta IsRegistrationEnabled su true per il collegamento denominato link, collegato all'area denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4337b-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4337b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4337b-118">PARAMETERS</span></span>

### <span data-ttu-id="4337b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4337b-119">-DefaultProfile</span></span>
<span data-ttu-id="4337b-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4337b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4337b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4337b-121">-InputObject</span></span>
<span data-ttu-id="4337b-122">Oggetto collegamento di rete virtuale da impostare.</span><span class="sxs-lookup"><span data-stu-id="4337b-122">The virtual network link object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="4337b-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="4337b-124">Valore booleano che rappresenta se è abilitata la registrazione nel collegamento alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4337b-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4337b-125">-Name</span></span>
<span data-ttu-id="4337b-126">Specifica il nome del collegamento rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4337b-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="4337b-127">Devi anche specificare il parametro *ResourceGroupName* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="4337b-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="4337b-128">In alternativa, puoi specificare il collegamento DNS privato usando il parametro *link* .</span><span class="sxs-lookup"><span data-stu-id="4337b-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-129">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="4337b-129">-Overwrite</span></span>
<span data-ttu-id="4337b-130">Quando specifichi il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), il collegamento non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="4337b-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="4337b-131">Ciò offre protezione per le modifiche simultanee del collegamento.</span><span class="sxs-lookup"><span data-stu-id="4337b-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="4337b-132">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina il collegamento indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="4337b-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4337b-133">-ResourceGroupName</span></span>
<span data-ttu-id="4337b-134">Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4337b-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="4337b-135">Devi anche specificare il parametro *zonename* e *Name* .</span><span class="sxs-lookup"><span data-stu-id="4337b-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="4337b-136">In alternativa, puoi specificare il collegamento alla rete virtuale usando un oggetto **PSPrivateDnsVirtualNetworkLink** , passato tramite la pipeline o il parametro *link* .</span><span class="sxs-lookup"><span data-stu-id="4337b-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4337b-137">-ResourceId</span></span>
<span data-ttu-id="4337b-138">Area DNS privata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="4337b-138">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="4337b-139">-Tag</span></span>
<span data-ttu-id="4337b-140">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4337b-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4337b-141">-Zonename</span><span class="sxs-lookup"><span data-stu-id="4337b-141">-ZoneName</span></span>
<span data-ttu-id="4337b-142">Specifica il nome dell'area DNS rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4337b-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="4337b-143">Devi anche specificare il *nome* e il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4337b-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="4337b-144">In alternativa, puoi specificare il collegamento DNS privato usando il parametro *link* .</span><span class="sxs-lookup"><span data-stu-id="4337b-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4337b-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4337b-145">-Confirm</span></span>
<span data-ttu-id="4337b-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4337b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4337b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4337b-147">-WhatIf</span></span>
<span data-ttu-id="4337b-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4337b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4337b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4337b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4337b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4337b-150">CommonParameters</span></span>
<span data-ttu-id="4337b-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4337b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4337b-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4337b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4337b-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4337b-153">INPUTS</span></span>

### <span data-ttu-id="4337b-154">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4337b-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="4337b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4337b-155">System.String</span></span>

## <span data-ttu-id="4337b-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4337b-156">OUTPUTS</span></span>

### <span data-ttu-id="4337b-157">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4337b-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4337b-158">Note</span><span class="sxs-lookup"><span data-stu-id="4337b-158">NOTES</span></span>

## <span data-ttu-id="4337b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4337b-159">RELATED LINKS</span></span>

[<span data-ttu-id="4337b-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4337b-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4337b-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4337b-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4337b-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4337b-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
