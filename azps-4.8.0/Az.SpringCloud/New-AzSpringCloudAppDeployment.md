---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191888"
---
# <span data-ttu-id="da002-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="da002-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="da002-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da002-102">SYNOPSIS</span></span>
<span data-ttu-id="da002-103">Creare una nuova distribuzione o aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="da002-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="da002-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da002-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="da002-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da002-105">DESCRIPTION</span></span>
<span data-ttu-id="da002-106">Creare una nuova distribuzione o aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="da002-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="da002-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da002-107">EXAMPLES</span></span>

### <span data-ttu-id="da002-108">Esempio 1: esempio 1: creare una distribuzione cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="da002-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

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

<span data-ttu-id="da002-109">Creare una distribuzione cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="da002-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="da002-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da002-110">PARAMETERS</span></span>

### <span data-ttu-id="da002-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="da002-111">-AppName</span></span>
<span data-ttu-id="da002-112">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="da002-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da002-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da002-113">-AsJob</span></span>
<span data-ttu-id="da002-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="da002-114">Run the command as a job</span></span>

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

### <span data-ttu-id="da002-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="da002-115">-Cpu</span></span>
<span data-ttu-id="da002-116">CPU necessaria</span><span class="sxs-lookup"><span data-stu-id="da002-116">Required CPU</span></span>

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

### <span data-ttu-id="da002-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da002-117">-DefaultProfile</span></span>
<span data-ttu-id="da002-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da002-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da002-119">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="da002-119">-EnvironmentVariable</span></span>
<span data-ttu-id="da002-120">Raccolta di variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="da002-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="da002-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="da002-121">-InstanceCount</span></span>
<span data-ttu-id="da002-122">Conteggio istanze</span><span class="sxs-lookup"><span data-stu-id="da002-122">Instance count</span></span>

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

### <span data-ttu-id="da002-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="da002-123">-JvmOption</span></span>
<span data-ttu-id="da002-124">Parametro JVM</span><span class="sxs-lookup"><span data-stu-id="da002-124">JVM parameter</span></span>

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

### <span data-ttu-id="da002-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="da002-125">-MemoryInGb</span></span>
<span data-ttu-id="da002-126">Dimensioni della memoria necessarie in GB</span><span class="sxs-lookup"><span data-stu-id="da002-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="da002-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="da002-127">-Name</span></span>
<span data-ttu-id="da002-128">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="da002-128">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da002-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="da002-129">-NoWait</span></span>
<span data-ttu-id="da002-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="da002-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da002-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da002-131">-ResourceGroupName</span></span>
<span data-ttu-id="da002-132">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="da002-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="da002-133">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="da002-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da002-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="da002-134">-RuntimeVersion</span></span>
<span data-ttu-id="da002-135">Versione di runtime</span><span class="sxs-lookup"><span data-stu-id="da002-135">Runtime version</span></span>

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

### <span data-ttu-id="da002-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da002-136">-ServiceName</span></span>
<span data-ttu-id="da002-137">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="da002-137">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da002-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="da002-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="da002-139">Selettore per l'elemento da usare per la distribuzione per i progetti a più moduli.</span><span class="sxs-lookup"><span data-stu-id="da002-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="da002-140">Questo dovrebbe essere il percorso relativo di Bethe per il modulo/progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="da002-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="da002-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="da002-141">-SourceRelativePath</span></span>
<span data-ttu-id="da002-142">Percorso relativo dello spazio di archiviazione che archivia l'origine</span><span class="sxs-lookup"><span data-stu-id="da002-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="da002-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="da002-143">-SourceType</span></span>
<span data-ttu-id="da002-144">Tipo di origine caricata</span><span class="sxs-lookup"><span data-stu-id="da002-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="da002-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="da002-145">-SourceVersion</span></span>
<span data-ttu-id="da002-146">Versione dell'origine</span><span class="sxs-lookup"><span data-stu-id="da002-146">Version of the source</span></span>

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

### <span data-ttu-id="da002-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da002-147">-SubscriptionId</span></span>
<span data-ttu-id="da002-148">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="da002-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="da002-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="da002-149">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da002-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da002-150">-Confirm</span></span>
<span data-ttu-id="da002-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da002-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da002-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da002-152">-WhatIf</span></span>
<span data-ttu-id="da002-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da002-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da002-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da002-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da002-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da002-155">CommonParameters</span></span>
<span data-ttu-id="da002-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da002-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da002-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da002-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da002-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da002-158">INPUTS</span></span>

## <span data-ttu-id="da002-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da002-159">OUTPUTS</span></span>

### <span data-ttu-id="da002-160">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="da002-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="da002-161">Note</span><span class="sxs-lookup"><span data-stu-id="da002-161">NOTES</span></span>

<span data-ttu-id="da002-162">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da002-162">ALIASES</span></span>

## <span data-ttu-id="da002-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da002-163">RELATED LINKS</span></span>

