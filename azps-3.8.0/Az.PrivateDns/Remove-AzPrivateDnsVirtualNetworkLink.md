---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018970"
---
# <span data-ttu-id="71cb0-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="71cb0-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="71cb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="71cb0-103">Rimuove un collegamento di rete virtuale da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71cb0-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="71cb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71cb0-104">SYNTAX</span></span>

### <span data-ttu-id="71cb0-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71cb0-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71cb0-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="71cb0-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71cb0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="71cb0-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71cb0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71cb0-108">DESCRIPTION</span></span>
<span data-ttu-id="71cb0-109">Il cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** Elimina definitivamente un collegamento DNS (Domain Name System) privato da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="71cb0-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="71cb0-110">Puoi passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *link* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="71cb0-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="71cb0-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="71cb0-112">Quando specifichi il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), il collegamento non viene eliminato se è stato modificato in Azure private DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="71cb0-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="71cb0-113">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="71cb0-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="71cb0-114">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="71cb0-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="71cb0-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71cb0-115">EXAMPLES</span></span>

### <span data-ttu-id="71cb0-116">Esempio 1: rimuovere un collegamento</span><span class="sxs-lookup"><span data-stu-id="71cb0-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="71cb0-117">Questo comando consente di rimuovere il collegamento denominato collegamento collegato a zona myzone.com dal gruppo risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71cb0-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="71cb0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71cb0-118">PARAMETERS</span></span>

### <span data-ttu-id="71cb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cb0-119">-DefaultProfile</span></span>
<span data-ttu-id="71cb0-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71cb0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71cb0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71cb0-121">-InputObject</span></span>
<span data-ttu-id="71cb0-122">Oggetto collegamento di rete virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="71cb0-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="71cb0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="71cb0-123">-Name</span></span>
<span data-ttu-id="71cb0-124">Specifica il nome del collegamento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="71cb0-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="71cb0-125">Devi anche specificare il parametro *ResourceGroupName* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="71cb0-126">In alternativa, puoi specificare il collegamento usando il parametro *link* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="71cb0-127">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="71cb0-127">-Overwrite</span></span>
<span data-ttu-id="71cb0-128">Quando specifichi la zona usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite il parametro pipeline o *link* ), la zona non viene eliminata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="71cb0-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="71cb0-129">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="71cb0-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="71cb0-130">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="71cb0-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="71cb0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71cb0-131">-PassThru</span></span>
<span data-ttu-id="71cb0-132">Usato per passare il risultato (booleano) dell'operazione elimina il collegamento alla rete virtuale più avanti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="71cb0-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="71cb0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cb0-133">-ResourceGroupName</span></span>
<span data-ttu-id="71cb0-134">Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="71cb0-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="71cb0-135">Devi anche specificare il parametro *zonename* e *Name* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="71cb0-136">In alternativa, puoi specificare la zona DNS usando un oggetto **PSPrivateDnsVirtualNetworkLink** , passato tramite la pipeline o il parametro *link* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="71cb0-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71cb0-137">-ResourceId</span></span>
<span data-ttu-id="71cb0-138">Specifica l'ID delle risorse ARM del collegamento.</span><span class="sxs-lookup"><span data-stu-id="71cb0-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="71cb0-139">-Zonename</span><span class="sxs-lookup"><span data-stu-id="71cb0-139">-ZoneName</span></span>
<span data-ttu-id="71cb0-140">Specifica il nome dell'area DNS privata a cui è associato il collegamento.</span><span class="sxs-lookup"><span data-stu-id="71cb0-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="71cb0-141">Devi anche specificare il parametro *ResourceGroupName* e *Name* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="71cb0-142">In alternativa, puoi specificare il collegamento usando il parametro *link* .</span><span class="sxs-lookup"><span data-stu-id="71cb0-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="71cb0-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71cb0-143">-Confirm</span></span>
<span data-ttu-id="71cb0-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71cb0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cb0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cb0-145">-WhatIf</span></span>
<span data-ttu-id="71cb0-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71cb0-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71cb0-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71cb0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cb0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cb0-148">CommonParameters</span></span>
<span data-ttu-id="71cb0-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71cb0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cb0-150">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71cb0-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cb0-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71cb0-151">INPUTS</span></span>

### <span data-ttu-id="71cb0-152">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="71cb0-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="71cb0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="71cb0-153">System.String</span></span>

## <span data-ttu-id="71cb0-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71cb0-154">OUTPUTS</span></span>

### <span data-ttu-id="71cb0-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71cb0-155">System.Boolean</span></span>

## <span data-ttu-id="71cb0-156">Note</span><span class="sxs-lookup"><span data-stu-id="71cb0-156">NOTES</span></span>

## <span data-ttu-id="71cb0-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71cb0-157">RELATED LINKS</span></span>

[<span data-ttu-id="71cb0-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="71cb0-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="71cb0-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="71cb0-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="71cb0-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="71cb0-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
