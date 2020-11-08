---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191244"
---
# <span data-ttu-id="e484f-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="e484f-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="e484f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e484f-102">SYNOPSIS</span></span>
<span data-ttu-id="e484f-103">Operazione per aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="e484f-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="e484f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e484f-104">SYNTAX</span></span>

### <span data-ttu-id="e484f-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e484f-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e484f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e484f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e484f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e484f-107">DESCRIPTION</span></span>
<span data-ttu-id="e484f-108">Operazione per aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="e484f-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="e484f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e484f-109">EXAMPLES</span></span>

### <span data-ttu-id="e484f-110">Esempio 1: aggiornare la distribuzione del cloud Spring per nome.</span><span class="sxs-lookup"><span data-stu-id="e484f-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="e484f-111">Aggiornare la distribuzione di Spring cloud per nome.</span><span class="sxs-lookup"><span data-stu-id="e484f-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="e484f-112">Esempio 2: aggiornare la distribuzione del cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="e484f-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="e484f-113">Aggiornare la distribuzione del cloud Spring da pipe.</span><span class="sxs-lookup"><span data-stu-id="e484f-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="e484f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e484f-114">PARAMETERS</span></span>

### <span data-ttu-id="e484f-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="e484f-115">-AppName</span></span>
<span data-ttu-id="e484f-116">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="e484f-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="e484f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e484f-117">-AsJob</span></span>
<span data-ttu-id="e484f-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e484f-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e484f-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="e484f-119">-Cpu</span></span>
<span data-ttu-id="e484f-120">CPU necessaria</span><span class="sxs-lookup"><span data-stu-id="e484f-120">Required CPU</span></span>

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

### <span data-ttu-id="e484f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e484f-121">-DefaultProfile</span></span>
<span data-ttu-id="e484f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e484f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e484f-123">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="e484f-123">-EnvironmentVariable</span></span>
<span data-ttu-id="e484f-124">Raccolta di variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="e484f-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="e484f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e484f-125">-InputObject</span></span>
<span data-ttu-id="e484f-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e484f-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e484f-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e484f-127">-InstanceCount</span></span>
<span data-ttu-id="e484f-128">Conteggio istanze</span><span class="sxs-lookup"><span data-stu-id="e484f-128">Instance count</span></span>

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

### <span data-ttu-id="e484f-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="e484f-129">-JvmOption</span></span>
<span data-ttu-id="e484f-130">Parametro JVM</span><span class="sxs-lookup"><span data-stu-id="e484f-130">JVM parameter</span></span>

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

### <span data-ttu-id="e484f-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="e484f-131">-MemoryInGb</span></span>
<span data-ttu-id="e484f-132">Dimensioni della memoria necessarie in GB</span><span class="sxs-lookup"><span data-stu-id="e484f-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="e484f-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e484f-133">-Name</span></span>
<span data-ttu-id="e484f-134">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e484f-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="e484f-135">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e484f-135">-NoWait</span></span>
<span data-ttu-id="e484f-136">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e484f-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e484f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e484f-137">-ResourceGroupName</span></span>
<span data-ttu-id="e484f-138">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e484f-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e484f-139">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="e484f-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e484f-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="e484f-140">-RuntimeVersion</span></span>
<span data-ttu-id="e484f-141">Versione di runtime</span><span class="sxs-lookup"><span data-stu-id="e484f-141">Runtime version</span></span>

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

### <span data-ttu-id="e484f-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e484f-142">-ServiceName</span></span>
<span data-ttu-id="e484f-143">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="e484f-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e484f-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="e484f-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="e484f-145">Selettore per l'elemento da usare per la distribuzione per i progetti a più moduli.</span><span class="sxs-lookup"><span data-stu-id="e484f-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="e484f-146">Questo dovrebbe essere il percorso relativo di Bethe per il modulo/progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e484f-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="e484f-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="e484f-147">-SourceRelativePath</span></span>
<span data-ttu-id="e484f-148">Percorso relativo dello spazio di archiviazione che archivia l'origine</span><span class="sxs-lookup"><span data-stu-id="e484f-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="e484f-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="e484f-149">-SourceType</span></span>
<span data-ttu-id="e484f-150">Tipo di origine caricata</span><span class="sxs-lookup"><span data-stu-id="e484f-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="e484f-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="e484f-151">-SourceVersion</span></span>
<span data-ttu-id="e484f-152">Versione dell'origine</span><span class="sxs-lookup"><span data-stu-id="e484f-152">Version of the source</span></span>

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

### <span data-ttu-id="e484f-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e484f-153">-SubscriptionId</span></span>
<span data-ttu-id="e484f-154">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e484f-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e484f-155">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e484f-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e484f-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e484f-156">-Confirm</span></span>
<span data-ttu-id="e484f-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e484f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e484f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e484f-158">-WhatIf</span></span>
<span data-ttu-id="e484f-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e484f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e484f-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e484f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e484f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e484f-161">CommonParameters</span></span>
<span data-ttu-id="e484f-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e484f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e484f-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e484f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e484f-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e484f-164">INPUTS</span></span>

### <span data-ttu-id="e484f-165">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e484f-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e484f-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e484f-166">OUTPUTS</span></span>

### <span data-ttu-id="e484f-167">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="e484f-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="e484f-168">Note</span><span class="sxs-lookup"><span data-stu-id="e484f-168">NOTES</span></span>

<span data-ttu-id="e484f-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e484f-169">ALIASES</span></span>

<span data-ttu-id="e484f-170">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e484f-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e484f-171">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e484f-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e484f-172">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e484f-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e484f-173">INPUTOBJECT <ISpringCloudIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e484f-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e484f-174">`[AppName <String>]`: Il nome della risorsa app.</span><span class="sxs-lookup"><span data-stu-id="e484f-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e484f-175">`[BindingName <String>]`: Nome della risorsa di binding.</span><span class="sxs-lookup"><span data-stu-id="e484f-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e484f-176">`[CertificateName <String>]`: Il nome della risorsa certificato.</span><span class="sxs-lookup"><span data-stu-id="e484f-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e484f-177">`[DeploymentName <String>]`: Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e484f-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e484f-178">`[DomainName <String>]`: Nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e484f-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e484f-179">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e484f-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e484f-180">`[Location <String>]`: area geografica</span><span class="sxs-lookup"><span data-stu-id="e484f-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e484f-181">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e484f-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e484f-182">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="e484f-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e484f-183">`[ServiceName <String>]`: Nome della risorsa servizio.</span><span class="sxs-lookup"><span data-stu-id="e484f-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e484f-184">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e484f-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e484f-185">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e484f-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e484f-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e484f-186">RELATED LINKS</span></span>

