---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: e4d7d502d96245291fce001f4706ae44f21f5fed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191245"
---
# <span data-ttu-id="2fa68-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="2fa68-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="2fa68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fa68-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa68-103">Operazione per aggiornare un'app in uscita.</span><span class="sxs-lookup"><span data-stu-id="2fa68-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="2fa68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fa68-104">SYNTAX</span></span>

### <span data-ttu-id="2fa68-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fa68-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2fa68-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2fa68-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2fa68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fa68-107">DESCRIPTION</span></span>
<span data-ttu-id="2fa68-108">Operazione per aggiornare un'app in uscita.</span><span class="sxs-lookup"><span data-stu-id="2fa68-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="2fa68-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fa68-109">EXAMPLES</span></span>

### <span data-ttu-id="2fa68-110">Esempio 1: aggiornare l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="2fa68-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="2fa68-111">Aggiornare l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="2fa68-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="2fa68-112">Esempio 2: aggiornare l'app Cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="2fa68-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="2fa68-113">Aggiornare l'app Spring cloud da pipe.</span><span class="sxs-lookup"><span data-stu-id="2fa68-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="2fa68-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fa68-114">PARAMETERS</span></span>

### <span data-ttu-id="2fa68-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2fa68-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="2fa68-116">Nome della distribuzione attiva dell'app</span><span class="sxs-lookup"><span data-stu-id="2fa68-116">Name of the active deployment of the App</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fa68-117">-AsJob</span></span>
<span data-ttu-id="2fa68-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2fa68-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2fa68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa68-119">-DefaultProfile</span></span>
<span data-ttu-id="2fa68-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa68-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa68-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2fa68-121">-Fqdn</span></span>
<span data-ttu-id="2fa68-122">Nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="2fa68-122">Fully qualified dns Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2fa68-123">-HttpsOnly</span></span>
<span data-ttu-id="2fa68-124">Indica se è consentito solo HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2fa68-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="2fa68-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fa68-125">-InputObject</span></span>
<span data-ttu-id="2fa68-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2fa68-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2fa68-127">-Location</span></span>
<span data-ttu-id="2fa68-128">La posizione GEO dell'applicazione, sempre la stessa con la relativa risorsa padre</span><span class="sxs-lookup"><span data-stu-id="2fa68-128">The GEO location of the application, always the same with its parent resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fa68-129">-Name</span></span>
<span data-ttu-id="2fa68-130">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="2fa68-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2fa68-131">-NoWait</span></span>
<span data-ttu-id="2fa68-132">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2fa68-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2fa68-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="2fa68-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="2fa68-134">Montare il percorso del disco persistente</span><span class="sxs-lookup"><span data-stu-id="2fa68-134">Mount path of the persistent disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="2fa68-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="2fa68-136">Dimensioni del disco persistente in GB</span><span class="sxs-lookup"><span data-stu-id="2fa68-136">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-137">-Pubblico</span><span class="sxs-lookup"><span data-stu-id="2fa68-137">-Public</span></span>
<span data-ttu-id="2fa68-138">Indica se l'app espone endpoint pubblico</span><span class="sxs-lookup"><span data-stu-id="2fa68-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="2fa68-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa68-139">-ResourceGroupName</span></span>
<span data-ttu-id="2fa68-140">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2fa68-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2fa68-141">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2fa68-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2fa68-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2fa68-142">-ServiceName</span></span>
<span data-ttu-id="2fa68-143">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="2fa68-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2fa68-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2fa68-144">-SubscriptionId</span></span>
<span data-ttu-id="2fa68-145">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa68-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2fa68-146">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2fa68-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2fa68-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="2fa68-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="2fa68-148">Montare il percorso del disco temporaneo</span><span class="sxs-lookup"><span data-stu-id="2fa68-148">Mount path of the temporary disk</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="2fa68-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="2fa68-150">Dimensioni del disco temporaneo in GB</span><span class="sxs-lookup"><span data-stu-id="2fa68-150">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa68-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2fa68-151">-Confirm</span></span>
<span data-ttu-id="2fa68-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa68-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa68-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa68-153">-WhatIf</span></span>
<span data-ttu-id="2fa68-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fa68-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa68-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2fa68-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa68-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa68-156">CommonParameters</span></span>
<span data-ttu-id="2fa68-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa68-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa68-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fa68-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa68-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fa68-159">INPUTS</span></span>

### <span data-ttu-id="2fa68-160">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2fa68-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2fa68-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fa68-161">OUTPUTS</span></span>

### <span data-ttu-id="2fa68-162">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="2fa68-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="2fa68-163">Note</span><span class="sxs-lookup"><span data-stu-id="2fa68-163">NOTES</span></span>

<span data-ttu-id="2fa68-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2fa68-164">ALIASES</span></span>

<span data-ttu-id="2fa68-165">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fa68-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2fa68-166">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2fa68-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2fa68-167">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2fa68-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2fa68-168">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2fa68-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2fa68-169">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="2fa68-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2fa68-170">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="2fa68-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2fa68-171">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="2fa68-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2fa68-172">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2fa68-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2fa68-173">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2fa68-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2fa68-174">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="2fa68-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2fa68-175">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="2fa68-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2fa68-176">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2fa68-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2fa68-177">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="2fa68-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2fa68-178">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="2fa68-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2fa68-179">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa68-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2fa68-180">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2fa68-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2fa68-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fa68-181">RELATED LINKS</span></span>

