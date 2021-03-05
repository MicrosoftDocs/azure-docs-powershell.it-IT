---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 1e1fa3709e597d220ba8269856f562a8ad8c3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985724"
---
# <span data-ttu-id="e4a8d-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4a8d-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e4a8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a8d-103">Aggiorna/imposta un collegamento di rete virtuale associato a un'area privata e a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="e4a8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4a8d-104">SYNTAX</span></span>

### <span data-ttu-id="e4a8d-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4a8d-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4a8d-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="e4a8d-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4a8d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4a8d-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a8d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4a8d-108">DESCRIPTION</span></span>
<span data-ttu-id="e4a8d-109">Il cmdlet **Set-AzPrivateDnsVirtualNetworkLink** aggiorna un collegamento associato a un'area da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="e4a8d-110">È possibile passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *Link* o usando l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *Name* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e4a8d-111">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e4a8d-112">Quando si specifica l'area usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *link),* il collegamento non viene aggiornato se è stato modificato nel DNS di Azure perché è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="e4a8d-113">Questo fornisce protezione per le modifiche simultanee ai collegamenti.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="e4a8d-114">Questa operazione può essere soppressa con il parametro *Overwrite,* che aggiorna il collegamento indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="e4a8d-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4a8d-115">EXAMPLES</span></span>

### <span data-ttu-id="e4a8d-116">Esempio 1: Impostare un collegamento</span><span class="sxs-lookup"><span data-stu-id="e4a8d-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="e4a8d-117">Questo comando imposta IsRegistrationEnabled su True per il collegamento denominato mylink, collegato all'area denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e4a8d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4a8d-118">PARAMETERS</span></span>

### <span data-ttu-id="e4a8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a8d-119">-DefaultProfile</span></span>
<span data-ttu-id="e4a8d-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e4a8d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4a8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4a8d-121">-InputObject</span></span>
<span data-ttu-id="e4a8d-122">Oggetto collegamento di rete virtuale da impostare.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="e4a8d-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="e4a8d-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="e4a8d-124">Booleano che rappresenta se la registrazione è abilitata sul collegamento di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="e4a8d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e4a8d-125">-Name</span></span>
<span data-ttu-id="e4a8d-126">Specifica il nome del collegamento rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="e4a8d-127">È anche necessario specificare il *parametro ResourceGroupName* *e ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="e4a8d-128">In alternativa, è possibile specificare il collegamento DNS privato usando il *parametro link.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="e4a8d-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e4a8d-129">-Overwrite</span></span>
<span data-ttu-id="e4a8d-130">Quando si specifica il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *link),* il collegamento non viene eliminato se è stato modificato nel DNS di Azure perché è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="e4a8d-131">Questo fornisce protezione per le modifiche simultanee ai collegamenti.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="e4a8d-132">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina il collegamento indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e4a8d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a8d-133">-ResourceGroupName</span></span>
<span data-ttu-id="e4a8d-134">Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="e4a8d-135">È anche necessario specificare il *parametro ZoneName* *e Name.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="e4a8d-136">In alternativa, è possibile specificare il collegamento di rete virtuale usando un oggetto **PSPrivateDnsVirtualNetworkLink,** passato tramite la pipeline o il *parametro link.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="e4a8d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4a8d-137">-ResourceId</span></span>
<span data-ttu-id="e4a8d-138">ID Risorsa area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="e4a8d-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4a8d-139">-Tag</span></span>
<span data-ttu-id="e4a8d-140">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e4a8d-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="e4a8d-141">-ZoneName</span></span>
<span data-ttu-id="e4a8d-142">Specifica il nome dell'area DNS rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="e4a8d-143">È anche necessario specificare il *parametro Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="e4a8d-144">In alternativa, è possibile specificare il collegamento DNS privato usando il *parametro link.*</span><span class="sxs-lookup"><span data-stu-id="e4a8d-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="e4a8d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4a8d-145">-Confirm</span></span>
<span data-ttu-id="e4a8d-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a8d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a8d-147">-WhatIf</span></span>
<span data-ttu-id="e4a8d-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4a8d-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a8d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a8d-150">CommonParameters</span></span>
<span data-ttu-id="e4a8d-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4a8d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a8d-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a8d-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a8d-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4a8d-153">INPUTS</span></span>

### <span data-ttu-id="e4a8d-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4a8d-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="e4a8d-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e4a8d-155">System.String</span></span>

## <span data-ttu-id="e4a8d-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4a8d-156">OUTPUTS</span></span>

### <span data-ttu-id="e4a8d-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4a8d-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e4a8d-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4a8d-158">NOTES</span></span>

## <span data-ttu-id="e4a8d-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4a8d-159">RELATED LINKS</span></span>

[<span data-ttu-id="e4a8d-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4a8d-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e4a8d-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4a8d-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e4a8d-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4a8d-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
