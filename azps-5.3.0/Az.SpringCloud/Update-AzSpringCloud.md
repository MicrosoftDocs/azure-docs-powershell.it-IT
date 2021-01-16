---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375661"
---
# <span data-ttu-id="35a8c-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="35a8c-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="35a8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="35a8c-103">Operazione per aggiornare un servizio che esce.</span><span class="sxs-lookup"><span data-stu-id="35a8c-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="35a8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35a8c-104">SYNTAX</span></span>

### <span data-ttu-id="35a8c-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35a8c-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35a8c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35a8c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35a8c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35a8c-107">DESCRIPTION</span></span>
<span data-ttu-id="35a8c-108">Operazione per aggiornare un servizio che esce.</span><span class="sxs-lookup"><span data-stu-id="35a8c-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="35a8c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35a8c-109">EXAMPLES</span></span>

### <span data-ttu-id="35a8c-110">Esempio 1: aggiornare il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="35a8c-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="35a8c-111">Aggiornare il servizio cloud primaverile in base al nome.</span><span class="sxs-lookup"><span data-stu-id="35a8c-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="35a8c-112">Esempio 2: aggiornare il servizio cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="35a8c-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="35a8c-113">Aggiornare il servizio cloud primaverile da pipe.</span><span class="sxs-lookup"><span data-stu-id="35a8c-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="35a8c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35a8c-114">PARAMETERS</span></span>

### <span data-ttu-id="35a8c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35a8c-115">-AsJob</span></span>
<span data-ttu-id="35a8c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="35a8c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="35a8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a8c-117">-DefaultProfile</span></span>
<span data-ttu-id="35a8c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35a8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a8c-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="35a8c-119">-GitPropertyUri</span></span>
<span data-ttu-id="35a8c-120">URI del repository</span><span class="sxs-lookup"><span data-stu-id="35a8c-120">URI of the repository</span></span>

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

### <span data-ttu-id="35a8c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35a8c-121">-InputObject</span></span>
<span data-ttu-id="35a8c-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="35a8c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35a8c-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="35a8c-123">-Location</span></span>
<span data-ttu-id="35a8c-124">Posizione GEO della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35a8c-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="35a8c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="35a8c-125">-Name</span></span>
<span data-ttu-id="35a8c-126">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="35a8c-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a8c-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="35a8c-127">-NoWait</span></span>
<span data-ttu-id="35a8c-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="35a8c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35a8c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a8c-129">-ResourceGroupName</span></span>
<span data-ttu-id="35a8c-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="35a8c-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="35a8c-131">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="35a8c-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="35a8c-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="35a8c-132">-SkuName</span></span>
<span data-ttu-id="35a8c-133">Nome dell'USK</span><span class="sxs-lookup"><span data-stu-id="35a8c-133">Name of the Sku</span></span>

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

### <span data-ttu-id="35a8c-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="35a8c-134">-SkuTier</span></span>
<span data-ttu-id="35a8c-135">Livello dell'USK</span><span class="sxs-lookup"><span data-stu-id="35a8c-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="35a8c-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35a8c-136">-SubscriptionId</span></span>
<span data-ttu-id="35a8c-137">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35a8c-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="35a8c-138">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="35a8c-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35a8c-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="35a8c-139">-Tag</span></span>
<span data-ttu-id="35a8c-140">Tag del servizio che è un elenco di coppie di valori chiave che descrivono la risorsa.</span><span class="sxs-lookup"><span data-stu-id="35a8c-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="35a8c-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="35a8c-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="35a8c-142">Chiave di strumentazione Insight Application di destinazione</span><span class="sxs-lookup"><span data-stu-id="35a8c-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="35a8c-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="35a8c-143">-TraceEnabled</span></span>
<span data-ttu-id="35a8c-144">Indica se abilitare la funzionalità di traccia</span><span class="sxs-lookup"><span data-stu-id="35a8c-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="35a8c-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35a8c-145">-Confirm</span></span>
<span data-ttu-id="35a8c-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35a8c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a8c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a8c-147">-WhatIf</span></span>
<span data-ttu-id="35a8c-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35a8c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a8c-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35a8c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a8c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a8c-150">CommonParameters</span></span>
<span data-ttu-id="35a8c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a8c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a8c-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35a8c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a8c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35a8c-153">INPUTS</span></span>

### <span data-ttu-id="35a8c-154">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="35a8c-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="35a8c-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35a8c-155">OUTPUTS</span></span>

### <span data-ttu-id="35a8c-156">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="35a8c-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="35a8c-157">Note</span><span class="sxs-lookup"><span data-stu-id="35a8c-157">NOTES</span></span>

<span data-ttu-id="35a8c-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="35a8c-158">ALIASES</span></span>

<span data-ttu-id="35a8c-159">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35a8c-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35a8c-160">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="35a8c-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35a8c-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35a8c-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35a8c-162">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="35a8c-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35a8c-163">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="35a8c-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="35a8c-164">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="35a8c-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="35a8c-165">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="35a8c-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="35a8c-166">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="35a8c-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="35a8c-167">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="35a8c-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="35a8c-168">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="35a8c-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35a8c-169">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="35a8c-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="35a8c-170">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="35a8c-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="35a8c-171">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="35a8c-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="35a8c-172">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="35a8c-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="35a8c-173">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35a8c-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="35a8c-174">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="35a8c-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="35a8c-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35a8c-175">RELATED LINKS</span></span>

