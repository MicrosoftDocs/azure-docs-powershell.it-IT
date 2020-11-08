---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193191"
---
# <span data-ttu-id="19f71-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="19f71-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="19f71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19f71-102">SYNOPSIS</span></span>
<span data-ttu-id="19f71-103">Creare una nuova distribuzione o aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="19f71-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="19f71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19f71-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="19f71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19f71-105">DESCRIPTION</span></span>
<span data-ttu-id="19f71-106">Creare una nuova distribuzione o aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="19f71-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="19f71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19f71-107">EXAMPLES</span></span>

### <span data-ttu-id="19f71-108">Esempio 1: esempio 1: creare una distribuzione cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="19f71-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="19f71-109">Creare una distribuzione cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="19f71-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="19f71-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19f71-110">PARAMETERS</span></span>

### <span data-ttu-id="19f71-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="19f71-111">-AppName</span></span>
<span data-ttu-id="19f71-112">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="19f71-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="19f71-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19f71-113">-AsJob</span></span>
<span data-ttu-id="19f71-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="19f71-114">Run the command as a job</span></span>

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

### <span data-ttu-id="19f71-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="19f71-115">-Cpu</span></span>
<span data-ttu-id="19f71-116">CPU necessaria</span><span class="sxs-lookup"><span data-stu-id="19f71-116">Required CPU</span></span>

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

### <span data-ttu-id="19f71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f71-117">-DefaultProfile</span></span>
<span data-ttu-id="19f71-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19f71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19f71-119">-Metodo EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="19f71-119">-EnvironmentVariable</span></span>
<span data-ttu-id="19f71-120">Raccolta di variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="19f71-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="19f71-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="19f71-121">-JvmOption</span></span>
<span data-ttu-id="19f71-122">Parametro JVM</span><span class="sxs-lookup"><span data-stu-id="19f71-122">JVM parameter</span></span>

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

### <span data-ttu-id="19f71-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="19f71-123">-MemoryInGb</span></span>
<span data-ttu-id="19f71-124">Dimensioni della memoria necessarie in GB</span><span class="sxs-lookup"><span data-stu-id="19f71-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="19f71-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="19f71-125">-Name</span></span>
<span data-ttu-id="19f71-126">Nome della risorsa di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="19f71-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="19f71-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="19f71-127">-NoWait</span></span>
<span data-ttu-id="19f71-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="19f71-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19f71-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f71-129">-ResourceGroupName</span></span>
<span data-ttu-id="19f71-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="19f71-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="19f71-131">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="19f71-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="19f71-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="19f71-132">-RuntimeVersion</span></span>
<span data-ttu-id="19f71-133">Versione di runtime</span><span class="sxs-lookup"><span data-stu-id="19f71-133">Runtime version</span></span>

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

### <span data-ttu-id="19f71-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="19f71-134">-ServiceName</span></span>
<span data-ttu-id="19f71-135">Nome della risorsa del servizio.</span><span class="sxs-lookup"><span data-stu-id="19f71-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="19f71-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="19f71-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="19f71-137">Selettore per l'elemento da usare per la distribuzione per i progetti a più moduli.</span><span class="sxs-lookup"><span data-stu-id="19f71-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="19f71-138">Questo dovrebbe essere il percorso relativo di Bethe per il modulo/progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="19f71-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="19f71-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="19f71-139">-SourceRelativePath</span></span>
<span data-ttu-id="19f71-140">Percorso relativo dello spazio di archiviazione che archivia l'origine</span><span class="sxs-lookup"><span data-stu-id="19f71-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="19f71-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="19f71-141">-SourceType</span></span>
<span data-ttu-id="19f71-142">Tipo di origine caricata</span><span class="sxs-lookup"><span data-stu-id="19f71-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="19f71-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="19f71-143">-SourceVersion</span></span>
<span data-ttu-id="19f71-144">Versione dell'origine</span><span class="sxs-lookup"><span data-stu-id="19f71-144">Version of the source</span></span>

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

### <span data-ttu-id="19f71-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19f71-145">-SubscriptionId</span></span>
<span data-ttu-id="19f71-146">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19f71-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="19f71-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="19f71-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="19f71-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19f71-148">-Confirm</span></span>
<span data-ttu-id="19f71-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19f71-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f71-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f71-150">-WhatIf</span></span>
<span data-ttu-id="19f71-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19f71-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19f71-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19f71-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f71-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f71-153">CommonParameters</span></span>
<span data-ttu-id="19f71-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f71-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f71-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19f71-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f71-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19f71-156">INPUTS</span></span>

## <span data-ttu-id="19f71-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19f71-157">OUTPUTS</span></span>

### <span data-ttu-id="19f71-158">Microsoft. Azure. PowerShell. Cmdlets. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="19f71-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="19f71-159">Note</span><span class="sxs-lookup"><span data-stu-id="19f71-159">NOTES</span></span>

<span data-ttu-id="19f71-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="19f71-160">ALIASES</span></span>

## <span data-ttu-id="19f71-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19f71-161">RELATED LINKS</span></span>

