---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188967"
---
# <span data-ttu-id="079a3-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="079a3-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="079a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="079a3-102">SYNOPSIS</span></span>
<span data-ttu-id="079a3-103">Operazione di aggiornamento di una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="079a3-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="079a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="079a3-104">SYNTAX</span></span>

### <span data-ttu-id="079a3-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="079a3-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="079a3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="079a3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="079a3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="079a3-107">DESCRIPTION</span></span>
<span data-ttu-id="079a3-108">Operazione di aggiornamento di una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="079a3-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="079a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="079a3-109">EXAMPLES</span></span>

### <span data-ttu-id="079a3-110">Esempio 1: Aggiornare la distribuzione cloud Spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="079a3-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="079a3-111">Aggiornare la distribuzione cloud spring in base al nome.</span><span class="sxs-lookup"><span data-stu-id="079a3-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="079a3-112">Esempio 2: Aggiornare la distribuzione cloud spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="079a3-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="079a3-113">Aggiorna la distribuzione cloud spring dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="079a3-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="079a3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="079a3-114">PARAMETERS</span></span>

### <span data-ttu-id="079a3-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="079a3-115">-AppName</span></span>
<span data-ttu-id="079a3-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="079a3-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="079a3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="079a3-117">-AsJob</span></span>
<span data-ttu-id="079a3-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="079a3-118">Run the command as a job</span></span>

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

### <span data-ttu-id="079a3-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="079a3-119">-Cpu</span></span>
<span data-ttu-id="079a3-120">CPU richiesta</span><span class="sxs-lookup"><span data-stu-id="079a3-120">Required CPU</span></span>

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

### <span data-ttu-id="079a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="079a3-121">-DefaultProfile</span></span>
<span data-ttu-id="079a3-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="079a3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="079a3-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="079a3-123">-EnvironmentVariable</span></span>
<span data-ttu-id="079a3-124">Raccolta di variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="079a3-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="079a3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="079a3-125">-InputObject</span></span>
<span data-ttu-id="079a3-126">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="079a3-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="079a3-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="079a3-127">-JvmOption</span></span>
<span data-ttu-id="079a3-128">Parametro JVM</span><span class="sxs-lookup"><span data-stu-id="079a3-128">JVM parameter</span></span>

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

### <span data-ttu-id="079a3-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="079a3-129">-MemoryInGb</span></span>
<span data-ttu-id="079a3-130">Dimensioni della memoria richieste in GB</span><span class="sxs-lookup"><span data-stu-id="079a3-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="079a3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="079a3-131">-Name</span></span>
<span data-ttu-id="079a3-132">Nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="079a3-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="079a3-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="079a3-133">-NoWait</span></span>
<span data-ttu-id="079a3-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="079a3-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="079a3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="079a3-135">-ResourceGroupName</span></span>
<span data-ttu-id="079a3-136">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="079a3-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="079a3-137">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="079a3-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="079a3-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="079a3-138">-RuntimeVersion</span></span>
<span data-ttu-id="079a3-139">Versione di runtime</span><span class="sxs-lookup"><span data-stu-id="079a3-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="079a3-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="079a3-140">-ServiceName</span></span>
<span data-ttu-id="079a3-141">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="079a3-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="079a3-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="079a3-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="079a3-143">Selettore per l'elemento da usare per la distribuzione per i progetti multi module.</span><span class="sxs-lookup"><span data-stu-id="079a3-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="079a3-144">Questo dovrebbe essere il percorso relativo del modulo o progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="079a3-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="079a3-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="079a3-145">-SourceRelativePath</span></span>
<span data-ttu-id="079a3-146">Percorso relativo dello spazio di archiviazione in cui è archiviata l'origine</span><span class="sxs-lookup"><span data-stu-id="079a3-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="079a3-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="079a3-147">-SourceType</span></span>
<span data-ttu-id="079a3-148">Tipo di origine caricata</span><span class="sxs-lookup"><span data-stu-id="079a3-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="079a3-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="079a3-149">-SourceVersion</span></span>
<span data-ttu-id="079a3-150">Versione dell'origine</span><span class="sxs-lookup"><span data-stu-id="079a3-150">Version of the source</span></span>

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

### <span data-ttu-id="079a3-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="079a3-151">-SubscriptionId</span></span>
<span data-ttu-id="079a3-152">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="079a3-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="079a3-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="079a3-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="079a3-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="079a3-154">-Confirm</span></span>
<span data-ttu-id="079a3-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="079a3-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="079a3-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="079a3-156">-WhatIf</span></span>
<span data-ttu-id="079a3-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="079a3-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="079a3-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="079a3-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="079a3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="079a3-159">CommonParameters</span></span>
<span data-ttu-id="079a3-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="079a3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="079a3-161">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="079a3-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="079a3-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="079a3-162">INPUTS</span></span>

### <span data-ttu-id="079a3-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="079a3-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="079a3-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="079a3-164">OUTPUTS</span></span>

### <span data-ttu-id="079a3-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="079a3-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="079a3-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="079a3-166">NOTES</span></span>

<span data-ttu-id="079a3-167">ALIAS</span><span class="sxs-lookup"><span data-stu-id="079a3-167">ALIASES</span></span>

<span data-ttu-id="079a3-168">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="079a3-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="079a3-169">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="079a3-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="079a3-170">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="079a3-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="079a3-171">INPUTOBJECT <ISpringCloudIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="079a3-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="079a3-172">`[AppName <String>]`: nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="079a3-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="079a3-173">`[BindingName <String>]`: nome della risorsa di associazione.</span><span class="sxs-lookup"><span data-stu-id="079a3-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="079a3-174">`[CertificateName <String>]`: nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="079a3-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="079a3-175">`[DeploymentName <String>]`: nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="079a3-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="079a3-176">`[DomainName <String>]`: nome della risorsa di dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="079a3-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="079a3-177">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="079a3-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="079a3-178">`[Location <String>]`: l'area geografica</span><span class="sxs-lookup"><span data-stu-id="079a3-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="079a3-179">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="079a3-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="079a3-180">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="079a3-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="079a3-181">`[ServiceName <String>]`: nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="079a3-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="079a3-182">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="079a3-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="079a3-183">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="079a3-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="079a3-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="079a3-184">RELATED LINKS</span></span>

