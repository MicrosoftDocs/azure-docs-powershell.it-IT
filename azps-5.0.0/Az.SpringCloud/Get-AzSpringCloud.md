---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193199"
---
# <span data-ttu-id="ce132-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="ce132-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="ce132-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce132-102">SYNOPSIS</span></span>
<span data-ttu-id="ce132-103">Ottenere un servizio e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="ce132-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="ce132-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce132-104">SYNTAX</span></span>

### <span data-ttu-id="ce132-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce132-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ce132-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ce132-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ce132-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce132-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ce132-108">List1</span><span class="sxs-lookup"><span data-stu-id="ce132-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce132-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce132-109">DESCRIPTION</span></span>
<span data-ttu-id="ce132-110">Ottenere un servizio e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="ce132-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="ce132-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce132-111">EXAMPLES</span></span>

### <span data-ttu-id="ce132-112">Esempio 1: ottenere il servizio cloud primaverile in base al nome</span><span class="sxs-lookup"><span data-stu-id="ce132-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="ce132-113">Ottenere il servizio cloud primaverile in base al nome</span><span class="sxs-lookup"><span data-stu-id="ce132-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="ce132-114">Esempio 2: elencare tutto il servizio cloud primaverile sotto il gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="ce132-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="ce132-115">Elencare tutto il servizio cloud primaverile sotto il gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="ce132-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="ce132-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce132-116">PARAMETERS</span></span>

### <span data-ttu-id="ce132-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce132-117">-DefaultProfile</span></span>
<span data-ttu-id="ce132-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce132-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce132-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce132-119">-InputObject</span></span>
<span data-ttu-id="ce132-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ce132-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce132-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce132-121">-Name</span></span>
<span data-ttu-id="ce132-122">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="ce132-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce132-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce132-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce132-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ce132-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ce132-125">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ce132-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce132-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce132-126">-SubscriptionId</span></span>
<span data-ttu-id="ce132-127">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce132-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce132-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ce132-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce132-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce132-129">CommonParameters</span></span>
<span data-ttu-id="ce132-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce132-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce132-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce132-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce132-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce132-132">INPUTS</span></span>

### <span data-ttu-id="ce132-133">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ce132-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ce132-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce132-134">OUTPUTS</span></span>

### <span data-ttu-id="ce132-135">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="ce132-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="ce132-136">Note</span><span class="sxs-lookup"><span data-stu-id="ce132-136">NOTES</span></span>

<span data-ttu-id="ce132-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ce132-137">ALIASES</span></span>

<span data-ttu-id="ce132-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce132-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce132-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ce132-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce132-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce132-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce132-141">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ce132-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce132-142">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="ce132-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ce132-143">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="ce132-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ce132-144">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="ce132-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ce132-145">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ce132-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ce132-146">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce132-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ce132-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ce132-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce132-148">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="ce132-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ce132-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ce132-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ce132-150">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ce132-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ce132-151">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="ce132-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ce132-152">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ce132-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ce132-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ce132-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ce132-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce132-154">RELATED LINKS</span></span>

