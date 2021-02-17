---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198630"
---
# <span data-ttu-id="8a337-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="8a337-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="8a337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a337-102">SYNOPSIS</span></span>
<span data-ttu-id="8a337-103">Ottenere un'app e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a337-103">Get an App and its properties.</span></span>

## <span data-ttu-id="8a337-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a337-104">SYNTAX</span></span>

### <span data-ttu-id="8a337-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a337-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a337-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8a337-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a337-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a337-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a337-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8a337-108">DESCRIPTION</span></span>
<span data-ttu-id="8a337-109">Ottenere un'app e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a337-109">Get an App and its properties.</span></span>

## <span data-ttu-id="8a337-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a337-110">EXAMPLES</span></span>

### <span data-ttu-id="8a337-111">Esempio 1: Ottenere l'app Spring Cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="8a337-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="8a337-112">Ottieni l'app Cloud Spring per nome.</span><span class="sxs-lookup"><span data-stu-id="8a337-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="8a337-113">Esempio 2: elencare tutte le app in un determinato servizio cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="8a337-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="8a337-114">Elencare tutte le app in un determinato servizio cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="8a337-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="8a337-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a337-115">PARAMETERS</span></span>

### <span data-ttu-id="8a337-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a337-116">-DefaultProfile</span></span>
<span data-ttu-id="8a337-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a337-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a337-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a337-118">-InputObject</span></span>
<span data-ttu-id="8a337-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8a337-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8a337-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8a337-120">-Name</span></span>
<span data-ttu-id="8a337-121">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="8a337-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="8a337-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a337-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a337-123">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8a337-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8a337-124">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="8a337-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8a337-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8a337-125">-ServiceName</span></span>
<span data-ttu-id="8a337-126">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="8a337-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="8a337-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a337-127">-SubscriptionId</span></span>
<span data-ttu-id="8a337-128">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a337-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a337-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8a337-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8a337-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="8a337-130">-SyncStatus</span></span>
<span data-ttu-id="8a337-131">Indica se lo stato di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="8a337-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="8a337-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a337-132">CommonParameters</span></span>
<span data-ttu-id="8a337-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a337-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a337-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a337-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a337-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="8a337-135">INPUTS</span></span>

### <span data-ttu-id="8a337-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8a337-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8a337-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a337-137">OUTPUTS</span></span>

### <span data-ttu-id="8a337-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="8a337-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="8a337-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="8a337-139">NOTES</span></span>

<span data-ttu-id="8a337-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8a337-140">ALIASES</span></span>

<span data-ttu-id="8a337-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8a337-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a337-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8a337-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a337-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a337-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a337-144">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="8a337-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a337-145">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="8a337-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8a337-146">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="8a337-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8a337-147">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="8a337-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8a337-148">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8a337-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8a337-149">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8a337-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8a337-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8a337-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a337-151">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="8a337-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8a337-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8a337-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8a337-153">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="8a337-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8a337-154">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="8a337-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8a337-155">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a337-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8a337-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8a337-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8a337-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a337-157">RELATED LINKS</span></span>

