---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488587"
---
# <span data-ttu-id="e4700-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="e4700-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="e4700-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4700-102">SYNOPSIS</span></span>
<span data-ttu-id="e4700-103">Operazione per eliminare un CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e4700-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="e4700-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4700-104">SYNTAX</span></span>

### <span data-ttu-id="e4700-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4700-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4700-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e4700-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4700-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4700-107">DESCRIPTION</span></span>
<span data-ttu-id="e4700-108">Operazione per eliminare un CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e4700-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="e4700-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4700-109">EXAMPLES</span></span>

### <span data-ttu-id="e4700-110">Esempio 1: rimuovere la risorsa di comunicazione di Azure specificata</span><span class="sxs-lookup"><span data-stu-id="e4700-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="e4700-111">Rimuovere/eliminare la risorsa di comunicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4700-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="e4700-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4700-112">PARAMETERS</span></span>

### <span data-ttu-id="e4700-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4700-113">-AsJob</span></span>
<span data-ttu-id="e4700-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e4700-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e4700-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4700-115">-DefaultProfile</span></span>
<span data-ttu-id="e4700-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4700-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4700-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4700-117">-InputObject</span></span>
<span data-ttu-id="e4700-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e4700-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4700-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4700-119">-Name</span></span>
<span data-ttu-id="e4700-120">Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e4700-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="e4700-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e4700-121">-NoWait</span></span>
<span data-ttu-id="e4700-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e4700-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4700-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4700-123">-PassThru</span></span>
<span data-ttu-id="e4700-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e4700-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e4700-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4700-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4700-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4700-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e4700-127">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="e4700-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e4700-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4700-128">-SubscriptionId</span></span>
<span data-ttu-id="e4700-129">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e4700-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4700-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e4700-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4700-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4700-131">-Confirm</span></span>
<span data-ttu-id="e4700-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4700-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4700-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4700-133">-WhatIf</span></span>
<span data-ttu-id="e4700-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4700-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4700-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4700-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4700-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4700-136">CommonParameters</span></span>
<span data-ttu-id="e4700-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4700-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4700-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4700-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4700-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4700-139">INPUTS</span></span>

### <span data-ttu-id="e4700-140">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="e4700-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="e4700-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4700-141">OUTPUTS</span></span>

### <span data-ttu-id="e4700-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4700-142">System.Boolean</span></span>

## <span data-ttu-id="e4700-143">Note</span><span class="sxs-lookup"><span data-stu-id="e4700-143">NOTES</span></span>

<span data-ttu-id="e4700-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e4700-144">ALIASES</span></span>

<span data-ttu-id="e4700-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4700-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4700-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e4700-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4700-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4700-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4700-148">INPUTOBJECT <ICommunicationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e4700-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4700-149">`[CommunicationServiceName <String>]`: Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="e4700-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="e4700-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e4700-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4700-151">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="e4700-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="e4700-152">`[OperationId <String>]`: ID di un'operazione asincrona in corso</span><span class="sxs-lookup"><span data-stu-id="e4700-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="e4700-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4700-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e4700-154">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="e4700-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e4700-155">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e4700-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="e4700-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e4700-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4700-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4700-157">RELATED LINKS</span></span>

