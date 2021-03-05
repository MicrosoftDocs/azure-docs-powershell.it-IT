---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965550"
---
# <span data-ttu-id="e4e2c-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4e2c-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="e4e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e2c-103">Rimuove un collegamento di rete virtuale da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="e4e2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4e2c-104">SYNTAX</span></span>

### <span data-ttu-id="e4e2c-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4e2c-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4e2c-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="e4e2c-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4e2c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e2c-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4e2c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4e2c-108">DESCRIPTION</span></span>
<span data-ttu-id="e4e2c-109">Il cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** elimina definitivamente un collegamento DNS (Domain Name System) privato da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="e4e2c-110">È possibile passare un oggetto **PSPrivateDnsVirtualNetworkLink** usando il parametro *Link* o usando l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *Name* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e4e2c-111">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e4e2c-112">Quando si specifica il collegamento usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *link),* il collegamento non viene eliminato se è stato modificato nel DNS privato di Azure perché è stato recuperato l'oggetto **LOCALE PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="e4e2c-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="e4e2c-113">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="e4e2c-114">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="e4e2c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4e2c-115">EXAMPLES</span></span>

### <span data-ttu-id="e4e2c-116">Esempio 1: Rimuovere un collegamento</span><span class="sxs-lookup"><span data-stu-id="e4e2c-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="e4e2c-117">Questo comando rimuove il collegamento denominato mylink collegato all'myzone.com di risorse dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e4e2c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4e2c-118">PARAMETERS</span></span>

### <span data-ttu-id="e4e2c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e2c-119">-DefaultProfile</span></span>
<span data-ttu-id="e4e2c-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e4e2c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4e2c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4e2c-121">-InputObject</span></span>
<span data-ttu-id="e4e2c-122">L'oggetto collegamento di rete virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="e4e2c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e4e2c-123">-Name</span></span>
<span data-ttu-id="e4e2c-124">Specifica il nome del collegamento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="e4e2c-125">È anche necessario specificare il *parametro ResourceGroupName* *e ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="e4e2c-126">In alternativa, è possibile specificare il collegamento usando il *parametro Link.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="e4e2c-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e4e2c-127">-Overwrite</span></span>
<span data-ttu-id="e4e2c-128">Quando si specifica l'area usando un oggetto **PSPrivateDnsVirtualNetworkLink** (passato tramite la pipeline o il parametro *Link),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché è stato recuperato l'oggetto **LOCALE PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="e4e2c-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="e4e2c-129">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="e4e2c-130">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e4e2c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4e2c-131">-PassThru</span></span>
<span data-ttu-id="e4e2c-132">Consente di passare il risultato (booleano) dell'operazione di eliminazione del collegamento di rete virtuale più avanti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="e4e2c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e2c-133">-ResourceGroupName</span></span>
<span data-ttu-id="e4e2c-134">Specifica il nome del gruppo di risorse che contiene il collegamento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="e4e2c-135">È anche necessario specificare il *parametro ZoneName* *e Name.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="e4e2c-136">In alternativa, è possibile specificare l'area DNS usando un oggetto **PSPrivateDnsVirtualNetworkLink,** passato tramite la pipeline o il *parametro Link.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="e4e2c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e2c-137">-ResourceId</span></span>
<span data-ttu-id="e4e2c-138">Specifica l'ARM ID risorsa del collegamento.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="e4e2c-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="e4e2c-139">-ZoneName</span></span>
<span data-ttu-id="e4e2c-140">Specifica il nome dell'area DNS privata a cui è associato il collegamento.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="e4e2c-141">È anche necessario specificare il *parametro ResourceGroupName* *e Name.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="e4e2c-142">In alternativa, è possibile specificare il collegamento usando il *parametro Link.*</span><span class="sxs-lookup"><span data-stu-id="e4e2c-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="e4e2c-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4e2c-143">-Confirm</span></span>
<span data-ttu-id="e4e2c-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e2c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e2c-145">-WhatIf</span></span>
<span data-ttu-id="e4e2c-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4e2c-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e2c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e2c-148">CommonParameters</span></span>
<span data-ttu-id="e4e2c-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e2c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e2c-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e2c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e2c-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4e2c-151">INPUTS</span></span>

### <span data-ttu-id="e4e2c-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4e2c-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="e4e2c-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e4e2c-153">System.String</span></span>

## <span data-ttu-id="e4e2c-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4e2c-154">OUTPUTS</span></span>

### <span data-ttu-id="e4e2c-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4e2c-155">System.Boolean</span></span>

## <span data-ttu-id="e4e2c-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4e2c-156">NOTES</span></span>

## <span data-ttu-id="e4e2c-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4e2c-157">RELATED LINKS</span></span>

[<span data-ttu-id="e4e2c-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4e2c-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e4e2c-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4e2c-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="e4e2c-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="e4e2c-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
