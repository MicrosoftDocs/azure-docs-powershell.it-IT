---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193177"
---
# <span data-ttu-id="532c9-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="532c9-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="532c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="532c9-102">SYNOPSIS</span></span>
<span data-ttu-id="532c9-103">Operazione per aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="532c9-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="532c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="532c9-104">SYNTAX</span></span>

### <span data-ttu-id="532c9-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="532c9-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="532c9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="532c9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="532c9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="532c9-107">DESCRIPTION</span></span>
<span data-ttu-id="532c9-108">Operazione per aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="532c9-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="532c9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="532c9-109">EXAMPLES</span></span>

### <span data-ttu-id="532c9-110">Esempio 1: aggiornare la distribuzione del cloud Spring per nome.</span><span class="sxs-lookup"><span data-stu-id="532c9-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="532c9-111">Aggiornare la distribuzione di Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="532c9-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="532c9-112">Esempio 2: aggiornare la distribuzione del cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="532c9-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="532c9-113">Aggiornare la distribuzione del cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="532c9-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="532c9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="532c9-114">PARAMETERS</span></span>

### <span data-ttu-id="532c9-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="532c9-115">-AppName</span></span>
<span data-ttu-id="532c9-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="532c9-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="532c9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="532c9-117">-AsJob</span></span>
<span data-ttu-id="532c9-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="532c9-118">Run the command as a job</span></span>

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

### <span data-ttu-id="532c9-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="532c9-119">-Cpu</span></span>
<span data-ttu-id="532c9-120">CPU necessaria</span><span class="sxs-lookup"><span data-stu-id="532c9-120">Required CPU</span></span>

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

### <span data-ttu-id="532c9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532c9-121">-DefaultProfile</span></span>
<span data-ttu-id="532c9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="532c9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="532c9-123">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="532c9-123">-EnvironmentVariable</span></span>
<span data-ttu-id="532c9-124">Raccolta di variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="532c9-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="532c9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="532c9-125">-InputObject</span></span>
<span data-ttu-id="532c9-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="532c9-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="532c9-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="532c9-127">-JvmOption</span></span>
<span data-ttu-id="532c9-128">Parametro JVM</span><span class="sxs-lookup"><span data-stu-id="532c9-128">JVM parameter</span></span>

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

### <span data-ttu-id="532c9-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="532c9-129">-MemoryInGb</span></span>
<span data-ttu-id="532c9-130">Dimensioni della memoria necessarie in GB</span><span class="sxs-lookup"><span data-stu-id="532c9-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="532c9-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="532c9-131">-Name</span></span>
<span data-ttu-id="532c9-132">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="532c9-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="532c9-133">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="532c9-133">-NoWait</span></span>
<span data-ttu-id="532c9-134">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="532c9-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="532c9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="532c9-135">-ResourceGroupName</span></span>
<span data-ttu-id="532c9-136">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="532c9-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="532c9-137">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="532c9-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="532c9-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="532c9-138">-RuntimeVersion</span></span>
<span data-ttu-id="532c9-139">Versione di runtime</span><span class="sxs-lookup"><span data-stu-id="532c9-139">Runtime version</span></span>

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

### <span data-ttu-id="532c9-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="532c9-140">-ServiceName</span></span>
<span data-ttu-id="532c9-141">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="532c9-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="532c9-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="532c9-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="532c9-143">Selettore per l'elemento da usare per la distribuzione per i progetti a più moduli.</span><span class="sxs-lookup"><span data-stu-id="532c9-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="532c9-144">Questo dovrebbe essere il percorso relativo di Bethe per il modulo/progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="532c9-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="532c9-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="532c9-145">-SourceRelativePath</span></span>
<span data-ttu-id="532c9-146">Percorso relativo dello spazio di archiviazione che archivia l'origine</span><span class="sxs-lookup"><span data-stu-id="532c9-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="532c9-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="532c9-147">-SourceType</span></span>
<span data-ttu-id="532c9-148">Tipo di origine caricata</span><span class="sxs-lookup"><span data-stu-id="532c9-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="532c9-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="532c9-149">-SourceVersion</span></span>
<span data-ttu-id="532c9-150">Versione dell'origine</span><span class="sxs-lookup"><span data-stu-id="532c9-150">Version of the source</span></span>

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

### <span data-ttu-id="532c9-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="532c9-151">-SubscriptionId</span></span>
<span data-ttu-id="532c9-152">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="532c9-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="532c9-153">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="532c9-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="532c9-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="532c9-154">-Confirm</span></span>
<span data-ttu-id="532c9-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="532c9-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="532c9-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="532c9-156">-WhatIf</span></span>
<span data-ttu-id="532c9-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="532c9-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="532c9-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="532c9-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="532c9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532c9-159">CommonParameters</span></span>
<span data-ttu-id="532c9-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="532c9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532c9-161">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="532c9-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532c9-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="532c9-162">INPUTS</span></span>

### <span data-ttu-id="532c9-163">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="532c9-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="532c9-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="532c9-164">OUTPUTS</span></span>

### <span data-ttu-id="532c9-165">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="532c9-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="532c9-166">Note</span><span class="sxs-lookup"><span data-stu-id="532c9-166">NOTES</span></span>

<span data-ttu-id="532c9-167">ALIAS</span><span class="sxs-lookup"><span data-stu-id="532c9-167">ALIASES</span></span>

<span data-ttu-id="532c9-168">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="532c9-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="532c9-169">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="532c9-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="532c9-170">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="532c9-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="532c9-171">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="532c9-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="532c9-172">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="532c9-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="532c9-173">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="532c9-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="532c9-174">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="532c9-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="532c9-175">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="532c9-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="532c9-176">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="532c9-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="532c9-177">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="532c9-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="532c9-178">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="532c9-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="532c9-179">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="532c9-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="532c9-180">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="532c9-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="532c9-181">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="532c9-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="532c9-182">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="532c9-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="532c9-183">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="532c9-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="532c9-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="532c9-184">RELATED LINKS</span></span>

