---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: 8c8e7059a6c23c928180b8d6fab3cfdbbfd9ed5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970413"
---
# <span data-ttu-id="ae1bd-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ae1bd-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="ae1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1bd-103">Rimuove un'area DNS privata da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="ae1bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae1bd-104">SYNTAX</span></span>

### <span data-ttu-id="ae1bd-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae1bd-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae1bd-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ae1bd-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae1bd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae1bd-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae1bd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae1bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ae1bd-109">Il cmdlet **Remove-AzPrivateDnsZone** elimina definitivamente un'area DNS (Domain Name System) privata da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="ae1bd-110">Vengono eliminati anche tutti i set di record contenuti nell'area.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="ae1bd-111">È possibile passare un **oggetto PrivateDnsZone** usando il parametro *PrivateZone* o l'operatore della pipeline oppure in alternativa è possibile specificare i parametri *Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ae1bd-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ae1bd-112">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ae1bd-113">Quando si specifica l'area usando un oggetto **PrivateDnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene eliminata se è stata modificata nel DNS di Azure dopo il recupero dell'oggetto **PrivateDnsZone** locale (solo le operazioni direttamente sul numero di risorse dell'area DNS vengono conteggiati come modifiche, mentre le operazioni sui set di record all'interno dell'area non vengono eseguite).</span><span class="sxs-lookup"><span data-stu-id="ae1bd-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="ae1bd-114">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="ae1bd-115">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="ae1bd-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae1bd-116">EXAMPLES</span></span>

### <span data-ttu-id="ae1bd-117">Esempio 1: Rimuovere un'area privata</span><span class="sxs-lookup"><span data-stu-id="ae1bd-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ae1bd-118">Questo comando rimuove l'area myzone.com denominata risorse dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ae1bd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae1bd-119">PARAMETERS</span></span>

### <span data-ttu-id="ae1bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1bd-120">-DefaultProfile</span></span>
<span data-ttu-id="ae1bd-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ae1bd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae1bd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ae1bd-122">-Name</span></span>
<span data-ttu-id="ae1bd-123">Specifica il nome dell'area DNS privata rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="ae1bd-124">È anche necessario specificare il *parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ae1bd-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ae1bd-125">In alternativa, è possibile specificare l'area DNS usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="ae1bd-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ae1bd-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ae1bd-126">-Overwrite</span></span>
<span data-ttu-id="ae1bd-127">Quando si specifica l'area usando un oggetto **PrivateDnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene eliminata se è stata modificata nel DNS di Azure dopo il recupero dell'oggetto **PrivateDnsZone** locale (solo le operazioni direttamente sul numero di risorse dell'area DNS vengono conteggiati come modifiche, mentre le operazioni sui set di record all'interno dell'area non vengono eseguite).</span><span class="sxs-lookup"><span data-stu-id="ae1bd-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="ae1bd-128">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="ae1bd-129">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ae1bd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae1bd-130">-PassThru</span></span>
<span data-ttu-id="ae1bd-131">Consente di passare il risultato (booleano) dell'operazione di eliminazione dell'area privata più in basso nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="ae1bd-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="ae1bd-132">-PrivateZone</span></span>
<span data-ttu-id="ae1bd-133">L'oggetto area privata da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae1bd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1bd-134">-ResourceGroupName</span></span>
<span data-ttu-id="ae1bd-135">Specifica il nome del gruppo di risorse che contiene l'area da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="ae1bd-136">È anche necessario specificare il *parametro ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="ae1bd-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="ae1bd-137">In alternativa, è possibile specificare l'area DNS usando un **oggetto PrivateDnsZone,** passato tramite la pipeline o il parametro *Zone.*</span><span class="sxs-lookup"><span data-stu-id="ae1bd-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ae1bd-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae1bd-138">-ResourceId</span></span>
<span data-ttu-id="ae1bd-139">ID Risorsa area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="ae1bd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae1bd-140">-Confirm</span></span>
<span data-ttu-id="ae1bd-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae1bd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae1bd-142">-WhatIf</span></span>
<span data-ttu-id="ae1bd-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1bd-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae1bd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1bd-145">CommonParameters</span></span>
<span data-ttu-id="ae1bd-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1bd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1bd-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1bd-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1bd-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae1bd-148">INPUTS</span></span>

### <span data-ttu-id="ae1bd-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ae1bd-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="ae1bd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="ae1bd-150">System.String</span></span>

## <span data-ttu-id="ae1bd-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae1bd-151">OUTPUTS</span></span>

### <span data-ttu-id="ae1bd-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae1bd-152">System.Boolean</span></span>

## <span data-ttu-id="ae1bd-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae1bd-153">NOTES</span></span>

## <span data-ttu-id="ae1bd-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae1bd-154">RELATED LINKS</span></span>

[<span data-ttu-id="ae1bd-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ae1bd-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="ae1bd-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ae1bd-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="ae1bd-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ae1bd-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
