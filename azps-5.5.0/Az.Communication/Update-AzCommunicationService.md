---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205003"
---
# <span data-ttu-id="faa1e-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="faa1e-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="faa1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faa1e-102">SYNOPSIS</span></span>
<span data-ttu-id="faa1e-103">Operazione per aggiornare un servizio di comunicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="faa1e-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="faa1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faa1e-104">SYNTAX</span></span>

### <span data-ttu-id="faa1e-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="faa1e-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="faa1e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="faa1e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="faa1e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="faa1e-107">DESCRIPTION</span></span>
<span data-ttu-id="faa1e-108">Operazione per aggiornare un servizio di comunicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="faa1e-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="faa1e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faa1e-109">EXAMPLES</span></span>

### <span data-ttu-id="faa1e-110">Esempio 1: Aggiornare una risorsa ACS esistente in modo che abbia tag</span><span class="sxs-lookup"><span data-stu-id="faa1e-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="faa1e-111">Collega i tag specificati alla risorsa ACS specificata.</span><span class="sxs-lookup"><span data-stu-id="faa1e-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="faa1e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faa1e-112">PARAMETERS</span></span>

### <span data-ttu-id="faa1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa1e-113">-DefaultProfile</span></span>
<span data-ttu-id="faa1e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faa1e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa1e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faa1e-115">-InputObject</span></span>
<span data-ttu-id="faa1e-116">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="faa1e-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="faa1e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="faa1e-117">-Name</span></span>
<span data-ttu-id="faa1e-118">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="faa1e-118">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="faa1e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa1e-119">-ResourceGroupName</span></span>
<span data-ttu-id="faa1e-120">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="faa1e-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="faa1e-121">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="faa1e-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="faa1e-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="faa1e-122">-SubscriptionId</span></span>
<span data-ttu-id="faa1e-123">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="faa1e-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="faa1e-124">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="faa1e-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="faa1e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="faa1e-125">-Tag</span></span>
<span data-ttu-id="faa1e-126">Tag del servizio, ovvero un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="faa1e-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="faa1e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="faa1e-127">-Confirm</span></span>
<span data-ttu-id="faa1e-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faa1e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faa1e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faa1e-129">-WhatIf</span></span>
<span data-ttu-id="faa1e-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faa1e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faa1e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faa1e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faa1e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa1e-132">CommonParameters</span></span>
<span data-ttu-id="faa1e-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa1e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa1e-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="faa1e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa1e-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="faa1e-135">INPUTS</span></span>

### <span data-ttu-id="faa1e-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="faa1e-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="faa1e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faa1e-137">OUTPUTS</span></span>

### <span data-ttu-id="faa1e-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="faa1e-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="faa1e-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="faa1e-139">NOTES</span></span>

<span data-ttu-id="faa1e-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="faa1e-140">ALIASES</span></span>

<span data-ttu-id="faa1e-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="faa1e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="faa1e-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="faa1e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="faa1e-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="faa1e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="faa1e-144">INPUTOBJECT <ICommunicationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="faa1e-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="faa1e-145">`[CommunicationServiceName <String>]`: nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="faa1e-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="faa1e-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="faa1e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="faa1e-147">`[Location <String>]`: l'area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="faa1e-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="faa1e-148">`[OperationId <String>]`: ID di un'operazione di sincronizzazione in corso</span><span class="sxs-lookup"><span data-stu-id="faa1e-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="faa1e-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="faa1e-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="faa1e-150">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="faa1e-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="faa1e-151">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="faa1e-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="faa1e-152">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="faa1e-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="faa1e-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faa1e-153">RELATED LINKS</span></span>

