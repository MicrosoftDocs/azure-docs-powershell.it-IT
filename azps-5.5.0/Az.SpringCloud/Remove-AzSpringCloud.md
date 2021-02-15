---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197790"
---
# <span data-ttu-id="b241d-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="b241d-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="b241d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b241d-102">SYNOPSIS</span></span>
<span data-ttu-id="b241d-103">Operazione per l'eliminazione di un servizio.</span><span class="sxs-lookup"><span data-stu-id="b241d-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="b241d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b241d-104">SYNTAX</span></span>

### <span data-ttu-id="b241d-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b241d-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b241d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b241d-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b241d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b241d-107">DESCRIPTION</span></span>
<span data-ttu-id="b241d-108">Operazione per l'eliminazione di un servizio.</span><span class="sxs-lookup"><span data-stu-id="b241d-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="b241d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b241d-109">EXAMPLES</span></span>

### <span data-ttu-id="b241d-110">Esempio 1: Rimuovere il servizio cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b241d-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="b241d-111">Rimuovere il servizio Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="b241d-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="b241d-112">Esempio 2: Rimuovere il servizio cloud Spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="b241d-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="b241d-113">Rimuovi Il servizio Cloud Spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="b241d-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="b241d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b241d-114">PARAMETERS</span></span>

### <span data-ttu-id="b241d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b241d-115">-AsJob</span></span>
<span data-ttu-id="b241d-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b241d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b241d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b241d-117">-DefaultProfile</span></span>
<span data-ttu-id="b241d-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b241d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b241d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b241d-119">-InputObject</span></span>
<span data-ttu-id="b241d-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b241d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b241d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b241d-121">-Name</span></span>
<span data-ttu-id="b241d-122">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="b241d-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b241d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b241d-123">-NoWait</span></span>
<span data-ttu-id="b241d-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b241d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b241d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b241d-125">-PassThru</span></span>
<span data-ttu-id="b241d-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b241d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b241d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b241d-127">-ResourceGroupName</span></span>
<span data-ttu-id="b241d-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b241d-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b241d-129">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b241d-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b241d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b241d-130">-SubscriptionId</span></span>
<span data-ttu-id="b241d-131">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b241d-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b241d-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b241d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b241d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b241d-133">-Confirm</span></span>
<span data-ttu-id="b241d-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b241d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b241d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b241d-135">-WhatIf</span></span>
<span data-ttu-id="b241d-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b241d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b241d-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b241d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b241d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b241d-138">CommonParameters</span></span>
<span data-ttu-id="b241d-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b241d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b241d-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b241d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b241d-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="b241d-141">INPUTS</span></span>

### <span data-ttu-id="b241d-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b241d-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b241d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b241d-143">OUTPUTS</span></span>

### <span data-ttu-id="b241d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b241d-144">System.Boolean</span></span>

## <span data-ttu-id="b241d-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="b241d-145">NOTES</span></span>

<span data-ttu-id="b241d-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b241d-146">ALIASES</span></span>

<span data-ttu-id="b241d-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b241d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b241d-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b241d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b241d-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b241d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b241d-150">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b241d-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b241d-151">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="b241d-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b241d-152">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="b241d-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b241d-153">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="b241d-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b241d-154">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b241d-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b241d-155">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b241d-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b241d-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b241d-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b241d-157">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="b241d-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b241d-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b241d-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b241d-159">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b241d-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b241d-160">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="b241d-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b241d-161">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b241d-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b241d-162">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b241d-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b241d-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b241d-163">RELATED LINKS</span></span>

