---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191900"
---
# <span data-ttu-id="1009d-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="1009d-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="1009d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1009d-102">SYNOPSIS</span></span>
<span data-ttu-id="1009d-103">Ottenere una distribuzione e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="1009d-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="1009d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1009d-104">SYNTAX</span></span>

### <span data-ttu-id="1009d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1009d-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1009d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="1009d-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1009d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1009d-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1009d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1009d-108">DESCRIPTION</span></span>
<span data-ttu-id="1009d-109">Ottenere una distribuzione e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="1009d-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="1009d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1009d-110">EXAMPLES</span></span>

### <span data-ttu-id="1009d-111">Esempio 1: ottenere l'app Spring cloud Deploymeng per nome.</span><span class="sxs-lookup"><span data-stu-id="1009d-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="1009d-112">Ottenere l'app Spring cloud Deploymeng per nome.</span><span class="sxs-lookup"><span data-stu-id="1009d-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="1009d-113">Esempio 2: elencare tutta la distribuzione in una determinata app Spring cloud.</span><span class="sxs-lookup"><span data-stu-id="1009d-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="1009d-114">Elencare tutte le distribuzioni in una determinata app Spring cloud.</span><span class="sxs-lookup"><span data-stu-id="1009d-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="1009d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1009d-115">PARAMETERS</span></span>

### <span data-ttu-id="1009d-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="1009d-116">-AppName</span></span>
<span data-ttu-id="1009d-117">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="1009d-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="1009d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1009d-118">-DefaultProfile</span></span>
<span data-ttu-id="1009d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1009d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1009d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1009d-120">-InputObject</span></span>
<span data-ttu-id="1009d-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1009d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1009d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1009d-122">-Name</span></span>
<span data-ttu-id="1009d-123">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1009d-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="1009d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1009d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1009d-125">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1009d-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1009d-126">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="1009d-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1009d-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1009d-127">-ServiceName</span></span>
<span data-ttu-id="1009d-128">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="1009d-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="1009d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1009d-129">-SubscriptionId</span></span>
<span data-ttu-id="1009d-130">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1009d-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1009d-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1009d-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1009d-132">-Versione</span><span class="sxs-lookup"><span data-stu-id="1009d-132">-Version</span></span>
<span data-ttu-id="1009d-133">Versione delle distribuzioni da elencare</span><span class="sxs-lookup"><span data-stu-id="1009d-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1009d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1009d-134">CommonParameters</span></span>
<span data-ttu-id="1009d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1009d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1009d-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1009d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1009d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1009d-137">INPUTS</span></span>

### <span data-ttu-id="1009d-138">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="1009d-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="1009d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1009d-139">OUTPUTS</span></span>

### <span data-ttu-id="1009d-140">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="1009d-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="1009d-141">Note</span><span class="sxs-lookup"><span data-stu-id="1009d-141">NOTES</span></span>

<span data-ttu-id="1009d-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1009d-142">ALIASES</span></span>

<span data-ttu-id="1009d-143">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1009d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1009d-144">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1009d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1009d-145">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1009d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1009d-146">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1009d-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1009d-147">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="1009d-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="1009d-148">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="1009d-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="1009d-149">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="1009d-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="1009d-150">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1009d-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="1009d-151">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1009d-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="1009d-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1009d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1009d-153">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="1009d-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="1009d-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1009d-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1009d-155">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="1009d-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1009d-156">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="1009d-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="1009d-157">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1009d-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1009d-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1009d-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1009d-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1009d-159">RELATED LINKS</span></span>

