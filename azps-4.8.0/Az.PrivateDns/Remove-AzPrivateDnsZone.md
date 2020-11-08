---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188971"
---
# <span data-ttu-id="5e0e2-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e0e2-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="5e0e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e0e2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0e2-103">Rimuove una zona DNS privata da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="5e0e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e0e2-104">SYNTAX</span></span>

### <span data-ttu-id="5e0e2-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e0e2-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e0e2-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="5e0e2-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e0e2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e0e2-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e0e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e0e2-108">DESCRIPTION</span></span>
<span data-ttu-id="5e0e2-109">Il cmdlet **Remove-AzPrivateDnsZone** Elimina definitivamente una zona DNS (private Domain Name System) da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="5e0e2-110">Vengono eliminati anche tutti i set di record contenuti nella zona.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="5e0e2-111">Puoi passare un oggetto **PrivateDnsZone** usando il parametro *PrivateZone* o usando l'operatore pipeline o in alternativa puoi specificare i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="5e0e2-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5e0e2-112">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5e0e2-113">Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="5e0e2-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5e0e2-114">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5e0e2-115">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5e0e2-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e0e2-116">EXAMPLES</span></span>

### <span data-ttu-id="5e0e2-117">Esempio 1: rimuovere un'area privata</span><span class="sxs-lookup"><span data-stu-id="5e0e2-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5e0e2-118">Questo comando rimuove la zona denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5e0e2-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e0e2-119">PARAMETERS</span></span>

### <span data-ttu-id="5e0e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0e2-120">-DefaultProfile</span></span>
<span data-ttu-id="5e0e2-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5e0e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e0e2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e0e2-122">-Name</span></span>
<span data-ttu-id="5e0e2-123">Specifica il nome dell'area DNS privata rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="5e0e2-124">Devi anche specificare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="5e0e2-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="5e0e2-125">In alternativa, puoi specificare la zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="5e0e2-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5e0e2-126">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="5e0e2-126">-Overwrite</span></span>
<span data-ttu-id="5e0e2-127">Quando specifichi la zona usando un oggetto **PrivateDnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **PrivateDnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="5e0e2-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5e0e2-128">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5e0e2-129">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5e0e2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e0e2-130">-PassThru</span></span>
<span data-ttu-id="5e0e2-131">Usato per passare il risultato (booleano) dell'operazione elimina l'area privata più avanti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="5e0e2-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="5e0e2-132">-PrivateZone</span></span>
<span data-ttu-id="5e0e2-133">Oggetto area privata da eliminare.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="5e0e2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0e2-134">-ResourceGroupName</span></span>
<span data-ttu-id="5e0e2-135">Specifica il nome del gruppo di risorse che contiene la zona da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="5e0e2-136">Devi anche specificare il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="5e0e2-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="5e0e2-137">In alternativa, puoi specificare la zona DNS usando un oggetto **PrivateDnsZone** , passato tramite il parametro pipeline o *zone* .</span><span class="sxs-lookup"><span data-stu-id="5e0e2-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5e0e2-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e0e2-138">-ResourceId</span></span>
<span data-ttu-id="5e0e2-139">Area DNS privata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="5e0e2-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e0e2-140">-Confirm</span></span>
<span data-ttu-id="5e0e2-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e0e2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0e2-142">-WhatIf</span></span>
<span data-ttu-id="5e0e2-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0e2-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e0e2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0e2-145">CommonParameters</span></span>
<span data-ttu-id="5e0e2-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e0e2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0e2-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e0e2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0e2-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e0e2-148">INPUTS</span></span>

### <span data-ttu-id="5e0e2-149">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e0e2-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="5e0e2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5e0e2-150">System.String</span></span>

## <span data-ttu-id="5e0e2-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e0e2-151">OUTPUTS</span></span>

### <span data-ttu-id="5e0e2-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e0e2-152">System.Boolean</span></span>

## <span data-ttu-id="5e0e2-153">Note</span><span class="sxs-lookup"><span data-stu-id="5e0e2-153">NOTES</span></span>

## <span data-ttu-id="5e0e2-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e0e2-154">RELATED LINKS</span></span>

[<span data-ttu-id="5e0e2-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e0e2-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="5e0e2-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e0e2-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="5e0e2-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5e0e2-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)