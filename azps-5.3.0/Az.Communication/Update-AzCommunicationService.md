---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488576"
---
# <span data-ttu-id="75b7b-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="75b7b-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="75b7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="75b7b-103">Operazione per aggiornare un CommunicationService esistente.</span><span class="sxs-lookup"><span data-stu-id="75b7b-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="75b7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75b7b-104">SYNTAX</span></span>

### <span data-ttu-id="75b7b-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75b7b-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75b7b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75b7b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75b7b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75b7b-107">DESCRIPTION</span></span>
<span data-ttu-id="75b7b-108">Operazione per aggiornare un CommunicationService esistente.</span><span class="sxs-lookup"><span data-stu-id="75b7b-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="75b7b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75b7b-109">EXAMPLES</span></span>

### <span data-ttu-id="75b7b-110">Esempio 1: aggiornare una risorsa ACS esistente per avere Tag</span><span class="sxs-lookup"><span data-stu-id="75b7b-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="75b7b-111">Allega i tag specificati alla risorsa ACS specificata.</span><span class="sxs-lookup"><span data-stu-id="75b7b-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="75b7b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75b7b-112">PARAMETERS</span></span>

### <span data-ttu-id="75b7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b7b-113">-DefaultProfile</span></span>
<span data-ttu-id="75b7b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75b7b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b7b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75b7b-115">-InputObject</span></span>
<span data-ttu-id="75b7b-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="75b7b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75b7b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="75b7b-117">-Name</span></span>
<span data-ttu-id="75b7b-118">Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="75b7b-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b7b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b7b-119">-ResourceGroupName</span></span>
<span data-ttu-id="75b7b-120">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="75b7b-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="75b7b-121">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="75b7b-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b7b-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75b7b-122">-SubscriptionId</span></span>
<span data-ttu-id="75b7b-123">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75b7b-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="75b7b-124">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="75b7b-124">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b7b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="75b7b-125">-Tag</span></span>
<span data-ttu-id="75b7b-126">Tag del servizio che è un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="75b7b-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="75b7b-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75b7b-127">-Confirm</span></span>
<span data-ttu-id="75b7b-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b7b-129">-WhatIf</span></span>
<span data-ttu-id="75b7b-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75b7b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b7b-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75b7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b7b-132">CommonParameters</span></span>
<span data-ttu-id="75b7b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b7b-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75b7b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b7b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75b7b-135">INPUTS</span></span>

### <span data-ttu-id="75b7b-136">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="75b7b-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="75b7b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75b7b-137">OUTPUTS</span></span>

### <span data-ttu-id="75b7b-138">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="75b7b-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="75b7b-139">Note</span><span class="sxs-lookup"><span data-stu-id="75b7b-139">NOTES</span></span>

<span data-ttu-id="75b7b-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="75b7b-140">ALIASES</span></span>

<span data-ttu-id="75b7b-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75b7b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75b7b-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="75b7b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75b7b-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75b7b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75b7b-144">INPUTOBJECT <ICommunicationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="75b7b-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75b7b-145">`[CommunicationServiceName <String>]`: Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="75b7b-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="75b7b-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="75b7b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75b7b-147">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="75b7b-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="75b7b-148">`[OperationId <String>]`: ID di un'operazione asincrona in corso</span><span class="sxs-lookup"><span data-stu-id="75b7b-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="75b7b-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="75b7b-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="75b7b-150">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="75b7b-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="75b7b-151">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75b7b-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="75b7b-152">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="75b7b-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="75b7b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75b7b-153">RELATED LINKS</span></span>

