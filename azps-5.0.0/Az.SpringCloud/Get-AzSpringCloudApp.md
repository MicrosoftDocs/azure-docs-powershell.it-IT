---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193200"
---
# <span data-ttu-id="5728f-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="5728f-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="5728f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5728f-102">SYNOPSIS</span></span>
<span data-ttu-id="5728f-103">Ottenere un'app e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="5728f-103">Get an App and its properties.</span></span>

## <span data-ttu-id="5728f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5728f-104">SYNTAX</span></span>

### <span data-ttu-id="5728f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5728f-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5728f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5728f-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5728f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5728f-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5728f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5728f-108">DESCRIPTION</span></span>
<span data-ttu-id="5728f-109">Ottenere un'app e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="5728f-109">Get an App and its properties.</span></span>

## <span data-ttu-id="5728f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5728f-110">EXAMPLES</span></span>

### <span data-ttu-id="5728f-111">Esempio 1: ottenere l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="5728f-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="5728f-112">Ottenere l'app Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="5728f-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="5728f-113">Esempio 2: elencare tutta l'app in un servizio cloud primaverile specifico.</span><span class="sxs-lookup"><span data-stu-id="5728f-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="5728f-114">Elenca tutta l'app in un servizio cloud primaverile specifico.</span><span class="sxs-lookup"><span data-stu-id="5728f-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="5728f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5728f-115">PARAMETERS</span></span>

### <span data-ttu-id="5728f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5728f-116">-DefaultProfile</span></span>
<span data-ttu-id="5728f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5728f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5728f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5728f-118">-InputObject</span></span>
<span data-ttu-id="5728f-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5728f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5728f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5728f-120">-Name</span></span>
<span data-ttu-id="5728f-121">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="5728f-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5728f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5728f-122">-ResourceGroupName</span></span>
<span data-ttu-id="5728f-123">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5728f-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5728f-124">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="5728f-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5728f-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5728f-125">-ServiceName</span></span>
<span data-ttu-id="5728f-126">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="5728f-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5728f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5728f-127">-SubscriptionId</span></span>
<span data-ttu-id="5728f-128">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5728f-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5728f-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5728f-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5728f-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="5728f-130">-SyncStatus</span></span>
<span data-ttu-id="5728f-131">Indica se lo stato della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="5728f-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5728f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5728f-132">CommonParameters</span></span>
<span data-ttu-id="5728f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5728f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5728f-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5728f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5728f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5728f-135">INPUTS</span></span>

### <span data-ttu-id="5728f-136">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="5728f-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="5728f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5728f-137">OUTPUTS</span></span>

### <span data-ttu-id="5728f-138">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="5728f-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="5728f-139">Note</span><span class="sxs-lookup"><span data-stu-id="5728f-139">NOTES</span></span>

<span data-ttu-id="5728f-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5728f-140">ALIASES</span></span>

<span data-ttu-id="5728f-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5728f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5728f-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5728f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5728f-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5728f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5728f-144">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5728f-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5728f-145">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="5728f-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="5728f-146">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="5728f-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="5728f-147">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="5728f-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="5728f-148">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5728f-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="5728f-149">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5728f-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="5728f-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5728f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5728f-151">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="5728f-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="5728f-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5728f-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5728f-153">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="5728f-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5728f-154">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="5728f-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="5728f-155">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5728f-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="5728f-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5728f-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5728f-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5728f-157">RELATED LINKS</span></span>
