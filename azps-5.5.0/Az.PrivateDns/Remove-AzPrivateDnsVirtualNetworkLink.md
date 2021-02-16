---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179062"
---
# <span data-ttu-id="e84d5-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e84d5-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e84d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e84d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e84d5-103">Rimuove un collegamento di rete virtuale da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e84d5-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="e84d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e84d5-104">SYNTAX</span></span>

### <span data-ttu-id="e84d5-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e84d5-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e84d5-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="e84d5-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e84d5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e84d5-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e84d5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e84d5-108">DESCRIPTION</span></span>
<span data-ttu-id="e84d5-109">Il cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** elimina definitivamente un collegamento DNS (Domain Name System) privato da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e84d5-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="e84d5-110">È possibile passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *Link* o usando l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *Name* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e84d5-111">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="e84d5-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e84d5-112">Quando si specifica il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *link),* il collegamento non viene eliminato se è stato modificato nel DNS privato di Azure perché è stato recuperato l'oggetto **LOCALE PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="e84d5-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="e84d5-113">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="e84d5-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="e84d5-114">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="e84d5-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="e84d5-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e84d5-115">EXAMPLES</span></span>

### <span data-ttu-id="e84d5-116">Esempio 1: Rimuovere un collegamento</span><span class="sxs-lookup"><span data-stu-id="e84d5-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="e84d5-117">Questo comando rimuove il collegamento denominato mylink collegato all'myzone.com di risorse dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e84d5-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e84d5-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e84d5-118">PARAMETERS</span></span>

### <span data-ttu-id="e84d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84d5-119">-DefaultProfile</span></span>
<span data-ttu-id="e84d5-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e84d5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e84d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e84d5-121">-InputObject</span></span>
<span data-ttu-id="e84d5-122">L'oggetto collegamento di rete virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e84d5-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="e84d5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e84d5-123">-Name</span></span>
<span data-ttu-id="e84d5-124">Specifica il nome del collegamento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e84d5-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="e84d5-125">È anche necessario specificare il *parametro ResourceGroupName* *e ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="e84d5-126">In alternativa, è possibile specificare il collegamento usando il *parametro Link.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="e84d5-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e84d5-127">-Overwrite</span></span>
<span data-ttu-id="e84d5-128">Quando si specifica l'area usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *Link),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché è stato recuperato l'oggetto **PSPrivateDnsVirtualNetworkLink** locale.</span><span class="sxs-lookup"><span data-stu-id="e84d5-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="e84d5-129">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="e84d5-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="e84d5-130">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="e84d5-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e84d5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e84d5-131">-PassThru</span></span>
<span data-ttu-id="e84d5-132">Consente di passare il risultato (booleano) dell'operazione di eliminazione del collegamento di rete virtuale più avanti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="e84d5-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="e84d5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e84d5-133">-ResourceGroupName</span></span>
<span data-ttu-id="e84d5-134">Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e84d5-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="e84d5-135">È anche necessario specificare il *parametro ZoneName* *e Name.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="e84d5-136">In alternativa, è possibile specificare l'area DNS usando un oggetto **PSPrivateDnsVirtualNetworkLink,** passato tramite la pipeline o il *parametro Link.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="e84d5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e84d5-137">-ResourceId</span></span>
<span data-ttu-id="e84d5-138">Specifica l'ARM ID risorsa del collegamento.</span><span class="sxs-lookup"><span data-stu-id="e84d5-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="e84d5-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="e84d5-139">-ZoneName</span></span>
<span data-ttu-id="e84d5-140">Specifica il nome dell'area DNS privata a cui è associato il collegamento.</span><span class="sxs-lookup"><span data-stu-id="e84d5-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="e84d5-141">È anche necessario specificare il *parametro ResourceGroupName* *e Name.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="e84d5-142">In alternativa, è possibile specificare il collegamento usando il *parametro Link.*</span><span class="sxs-lookup"><span data-stu-id="e84d5-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="e84d5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e84d5-143">-Confirm</span></span>
<span data-ttu-id="e84d5-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e84d5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e84d5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e84d5-145">-WhatIf</span></span>
<span data-ttu-id="e84d5-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e84d5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e84d5-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e84d5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e84d5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84d5-148">CommonParameters</span></span>
<span data-ttu-id="e84d5-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84d5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84d5-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e84d5-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84d5-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="e84d5-151">INPUTS</span></span>

### <span data-ttu-id="e84d5-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e84d5-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="e84d5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e84d5-153">System.String</span></span>

## <span data-ttu-id="e84d5-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e84d5-154">OUTPUTS</span></span>

### <span data-ttu-id="e84d5-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e84d5-155">System.Boolean</span></span>

## <span data-ttu-id="e84d5-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="e84d5-156">NOTES</span></span>

## <span data-ttu-id="e84d5-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e84d5-157">RELATED LINKS</span></span>

[<span data-ttu-id="e84d5-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e84d5-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e84d5-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e84d5-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e84d5-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e84d5-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
