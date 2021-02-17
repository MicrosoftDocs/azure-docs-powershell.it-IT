---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198599"
---
# <span data-ttu-id="cdb86-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="cdb86-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="cdb86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb86-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb86-103">Ottenere una distribuzione e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="cdb86-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="cdb86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdb86-104">SYNTAX</span></span>

### <span data-ttu-id="cdb86-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdb86-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cdb86-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cdb86-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cdb86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cdb86-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb86-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="cdb86-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cdb86-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cdb86-109">DESCRIPTION</span></span>
<span data-ttu-id="cdb86-110">Ottenere una distribuzione e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="cdb86-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="cdb86-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdb86-111">EXAMPLES</span></span>

### <span data-ttu-id="cdb86-112">Esempio 1: Ottenere la distribuzione dell'app Spring Cloud in base al nome.</span><span class="sxs-lookup"><span data-stu-id="cdb86-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="cdb86-113">Ottieni La distribuzione di App Cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="cdb86-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="cdb86-114">Esempio 2: elencare tutte le distribuzioni in un'app cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="cdb86-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="cdb86-115">Elencare tutte le distribuzioni in una determinata app cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="cdb86-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="cdb86-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdb86-116">PARAMETERS</span></span>

### <span data-ttu-id="cdb86-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="cdb86-117">-AppName</span></span>
<span data-ttu-id="cdb86-118">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="cdb86-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="cdb86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb86-119">-DefaultProfile</span></span>
<span data-ttu-id="cdb86-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb86-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdb86-121">-InputObject</span></span>
<span data-ttu-id="cdb86-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cdb86-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cdb86-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cdb86-123">-Name</span></span>
<span data-ttu-id="cdb86-124">Nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="cdb86-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb86-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb86-125">-ResourceGroupName</span></span>
<span data-ttu-id="cdb86-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cdb86-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cdb86-127">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="cdb86-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb86-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cdb86-128">-ServiceName</span></span>
<span data-ttu-id="cdb86-129">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="cdb86-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb86-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdb86-130">-SubscriptionId</span></span>
<span data-ttu-id="cdb86-131">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb86-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cdb86-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cdb86-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cdb86-133">-Version</span><span class="sxs-lookup"><span data-stu-id="cdb86-133">-Version</span></span>
<span data-ttu-id="cdb86-134">Versione delle distribuzioni da visualizzare</span><span class="sxs-lookup"><span data-stu-id="cdb86-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb86-135">CommonParameters</span></span>
<span data-ttu-id="cdb86-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb86-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cdb86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb86-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="cdb86-138">INPUTS</span></span>

### <span data-ttu-id="cdb86-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="cdb86-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="cdb86-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdb86-140">OUTPUTS</span></span>

### <span data-ttu-id="cdb86-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="cdb86-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="cdb86-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="cdb86-142">NOTES</span></span>

<span data-ttu-id="cdb86-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cdb86-143">ALIASES</span></span>

<span data-ttu-id="cdb86-144">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cdb86-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cdb86-145">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cdb86-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cdb86-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cdb86-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cdb86-147">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="cdb86-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cdb86-148">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="cdb86-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="cdb86-149">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="cdb86-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="cdb86-150">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="cdb86-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="cdb86-151">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="cdb86-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="cdb86-152">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cdb86-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="cdb86-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cdb86-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cdb86-154">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="cdb86-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="cdb86-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cdb86-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cdb86-156">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="cdb86-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cdb86-157">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="cdb86-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="cdb86-158">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb86-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cdb86-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cdb86-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cdb86-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdb86-160">RELATED LINKS</span></span>

