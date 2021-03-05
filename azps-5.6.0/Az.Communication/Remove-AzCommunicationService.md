---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: 3feb6e2246e2265c36e67d64621a5726eaabb6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991603"
---
# <span data-ttu-id="69391-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="69391-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="69391-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69391-102">SYNOPSIS</span></span>
<span data-ttu-id="69391-103">Operazione per eliminare un servizio di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="69391-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="69391-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69391-104">SYNTAX</span></span>

### <span data-ttu-id="69391-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69391-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69391-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="69391-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69391-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="69391-107">DESCRIPTION</span></span>
<span data-ttu-id="69391-108">Operazione per eliminare un servizio di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="69391-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="69391-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69391-109">EXAMPLES</span></span>

### <span data-ttu-id="69391-110">Esempio 1: Rimuovere la risorsa di comunicazione di Azure specificata</span><span class="sxs-lookup"><span data-stu-id="69391-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="69391-111">Rimuovere/eliminare la risorsa di comunicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="69391-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="69391-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69391-112">PARAMETERS</span></span>

### <span data-ttu-id="69391-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69391-113">-AsJob</span></span>
<span data-ttu-id="69391-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="69391-114">Run the command as a job</span></span>

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

### <span data-ttu-id="69391-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69391-115">-DefaultProfile</span></span>
<span data-ttu-id="69391-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69391-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69391-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69391-117">-InputObject</span></span>
<span data-ttu-id="69391-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="69391-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69391-119">-Name</span><span class="sxs-lookup"><span data-stu-id="69391-119">-Name</span></span>
<span data-ttu-id="69391-120">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="69391-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69391-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69391-121">-NoWait</span></span>
<span data-ttu-id="69391-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="69391-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69391-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69391-123">-PassThru</span></span>
<span data-ttu-id="69391-124">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="69391-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69391-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69391-125">-ResourceGroupName</span></span>
<span data-ttu-id="69391-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="69391-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="69391-127">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="69391-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69391-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69391-128">-SubscriptionId</span></span>
<span data-ttu-id="69391-129">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69391-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="69391-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="69391-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69391-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69391-131">-Confirm</span></span>
<span data-ttu-id="69391-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69391-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69391-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69391-133">-WhatIf</span></span>
<span data-ttu-id="69391-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69391-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69391-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69391-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69391-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69391-136">CommonParameters</span></span>
<span data-ttu-id="69391-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69391-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69391-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="69391-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69391-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="69391-139">INPUTS</span></span>

### <span data-ttu-id="69391-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="69391-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="69391-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69391-141">OUTPUTS</span></span>

### <span data-ttu-id="69391-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69391-142">System.Boolean</span></span>

## <span data-ttu-id="69391-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="69391-143">NOTES</span></span>

<span data-ttu-id="69391-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="69391-144">ALIASES</span></span>

<span data-ttu-id="69391-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="69391-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69391-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="69391-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69391-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69391-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69391-148">INPUTOBJECT <ICommunicationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="69391-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69391-149">`[CommunicationServiceName <String>]`: nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="69391-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="69391-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="69391-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69391-151">`[Location <String>]`: l'area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="69391-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="69391-152">`[OperationId <String>]`: ID di un'operazione di sincronizzazione in corso</span><span class="sxs-lookup"><span data-stu-id="69391-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="69391-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="69391-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="69391-154">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="69391-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="69391-155">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69391-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="69391-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="69391-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="69391-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69391-157">RELATED LINKS</span></span>

