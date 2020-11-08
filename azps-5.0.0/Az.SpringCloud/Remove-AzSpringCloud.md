---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193187"
---
# <span data-ttu-id="dc8cf-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="dc8cf-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="dc8cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8cf-103">Operazione per eliminare un servizio.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="dc8cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc8cf-104">SYNTAX</span></span>

### <span data-ttu-id="dc8cf-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc8cf-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dc8cf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc8cf-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc8cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc8cf-107">DESCRIPTION</span></span>
<span data-ttu-id="dc8cf-108">Operazione per eliminare un servizio.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="dc8cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc8cf-109">EXAMPLES</span></span>

### <span data-ttu-id="dc8cf-110">Esempio 1: rimuovere il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="dc8cf-111">Rimuovere il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="dc8cf-112">Esempio 2: rimuovere il servizio cloud primaverile dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="dc8cf-113">Rimuovere il servizio cloud primaverile dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="dc8cf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc8cf-114">PARAMETERS</span></span>

### <span data-ttu-id="dc8cf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc8cf-115">-AsJob</span></span>
<span data-ttu-id="dc8cf-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="dc8cf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dc8cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8cf-117">-DefaultProfile</span></span>
<span data-ttu-id="dc8cf-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc8cf-119">-InputObject</span></span>
<span data-ttu-id="dc8cf-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc8cf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc8cf-121">-Name</span></span>
<span data-ttu-id="dc8cf-122">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="dc8cf-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="dc8cf-123">-NoWait</span></span>
<span data-ttu-id="dc8cf-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="dc8cf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc8cf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc8cf-125">-PassThru</span></span>
<span data-ttu-id="dc8cf-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="dc8cf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc8cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc8cf-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dc8cf-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dc8cf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc8cf-130">-SubscriptionId</span></span>
<span data-ttu-id="dc8cf-131">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc8cf-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dc8cf-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc8cf-133">-Confirm</span></span>
<span data-ttu-id="dc8cf-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc8cf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc8cf-135">-WhatIf</span></span>
<span data-ttu-id="dc8cf-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc8cf-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc8cf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8cf-138">CommonParameters</span></span>
<span data-ttu-id="dc8cf-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8cf-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc8cf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8cf-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc8cf-141">INPUTS</span></span>

### <span data-ttu-id="dc8cf-142">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="dc8cf-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="dc8cf-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc8cf-143">OUTPUTS</span></span>

### <span data-ttu-id="dc8cf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc8cf-144">System.Boolean</span></span>

## <span data-ttu-id="dc8cf-145">Note</span><span class="sxs-lookup"><span data-stu-id="dc8cf-145">NOTES</span></span>

<span data-ttu-id="dc8cf-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dc8cf-146">ALIASES</span></span>

<span data-ttu-id="dc8cf-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc8cf-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc8cf-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc8cf-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc8cf-150">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="dc8cf-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc8cf-151">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="dc8cf-152">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="dc8cf-153">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="dc8cf-154">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="dc8cf-155">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="dc8cf-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="dc8cf-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc8cf-157">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="dc8cf-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="dc8cf-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="dc8cf-159">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="dc8cf-160">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="dc8cf-161">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="dc8cf-162">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="dc8cf-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dc8cf-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc8cf-163">RELATED LINKS</span></span>

