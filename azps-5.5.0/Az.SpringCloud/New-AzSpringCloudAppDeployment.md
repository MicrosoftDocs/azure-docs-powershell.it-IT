---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201551"
---
# <span data-ttu-id="c4de1-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c4de1-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c4de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4de1-102">SYNOPSIS</span></span>
<span data-ttu-id="c4de1-103">Creare una nuova distribuzione o aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="c4de1-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="c4de1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4de1-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c4de1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4de1-105">DESCRIPTION</span></span>
<span data-ttu-id="c4de1-106">Creare una nuova distribuzione o aggiornare una distribuzione in uscita.</span><span class="sxs-lookup"><span data-stu-id="c4de1-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="c4de1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4de1-107">EXAMPLES</span></span>

### <span data-ttu-id="c4de1-108">Esempio 1: Esempio 1: Creare una distribuzione cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="c4de1-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="c4de1-109">Creare una distribuzione cloud primaverile.</span><span class="sxs-lookup"><span data-stu-id="c4de1-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="c4de1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4de1-110">PARAMETERS</span></span>

### <span data-ttu-id="c4de1-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="c4de1-111">-AppName</span></span>
<span data-ttu-id="c4de1-112">Nome della risorsa dell'app.</span><span class="sxs-lookup"><span data-stu-id="c4de1-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="c4de1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4de1-113">-AsJob</span></span>
<span data-ttu-id="c4de1-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c4de1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c4de1-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="c4de1-115">-Cpu</span></span>
<span data-ttu-id="c4de1-116">CPU richiesta</span><span class="sxs-lookup"><span data-stu-id="c4de1-116">Required CPU</span></span>

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

### <span data-ttu-id="c4de1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4de1-117">-DefaultProfile</span></span>
<span data-ttu-id="c4de1-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4de1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4de1-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c4de1-119">-EnvironmentVariable</span></span>
<span data-ttu-id="c4de1-120">Raccolta di variabili di ambiente</span><span class="sxs-lookup"><span data-stu-id="c4de1-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="c4de1-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="c4de1-121">-JvmOption</span></span>
<span data-ttu-id="c4de1-122">Parametro JVM</span><span class="sxs-lookup"><span data-stu-id="c4de1-122">JVM parameter</span></span>

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

### <span data-ttu-id="c4de1-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="c4de1-123">-MemoryInGb</span></span>
<span data-ttu-id="c4de1-124">Dimensioni della memoria richieste in GB</span><span class="sxs-lookup"><span data-stu-id="c4de1-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="c4de1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c4de1-125">-Name</span></span>
<span data-ttu-id="c4de1-126">Nome della risorsa distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c4de1-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="c4de1-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4de1-127">-NoWait</span></span>
<span data-ttu-id="c4de1-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c4de1-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4de1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4de1-129">-ResourceGroupName</span></span>
<span data-ttu-id="c4de1-130">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4de1-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c4de1-131">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c4de1-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c4de1-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c4de1-132">-RuntimeVersion</span></span>
<span data-ttu-id="c4de1-133">Versione di runtime</span><span class="sxs-lookup"><span data-stu-id="c4de1-133">Runtime version</span></span>

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

### <span data-ttu-id="c4de1-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c4de1-134">-ServiceName</span></span>
<span data-ttu-id="c4de1-135">Nome della risorsa Servizio.</span><span class="sxs-lookup"><span data-stu-id="c4de1-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c4de1-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="c4de1-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="c4de1-137">Selettore per l'elemento da usare per la distribuzione per i progetti multi module.</span><span class="sxs-lookup"><span data-stu-id="c4de1-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="c4de1-138">Questo dovrebbe essere il percorso relativo del modulo o progetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c4de1-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="c4de1-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c4de1-139">-SourceRelativePath</span></span>
<span data-ttu-id="c4de1-140">Percorso relativo dello spazio di archiviazione in cui è archiviata l'origine</span><span class="sxs-lookup"><span data-stu-id="c4de1-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="c4de1-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c4de1-141">-SourceType</span></span>
<span data-ttu-id="c4de1-142">Tipo di origine caricata</span><span class="sxs-lookup"><span data-stu-id="c4de1-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="c4de1-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="c4de1-143">-SourceVersion</span></span>
<span data-ttu-id="c4de1-144">Versione dell'origine</span><span class="sxs-lookup"><span data-stu-id="c4de1-144">Version of the source</span></span>

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

### <span data-ttu-id="c4de1-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4de1-145">-SubscriptionId</span></span>
<span data-ttu-id="c4de1-146">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c4de1-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4de1-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c4de1-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c4de1-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4de1-148">-Confirm</span></span>
<span data-ttu-id="c4de1-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4de1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4de1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4de1-150">-WhatIf</span></span>
<span data-ttu-id="c4de1-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4de1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4de1-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4de1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4de1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4de1-153">CommonParameters</span></span>
<span data-ttu-id="c4de1-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4de1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4de1-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4de1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4de1-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4de1-156">INPUTS</span></span>

## <span data-ttu-id="c4de1-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4de1-157">OUTPUTS</span></span>

### <span data-ttu-id="c4de1-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="c4de1-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="c4de1-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4de1-159">NOTES</span></span>

<span data-ttu-id="c4de1-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c4de1-160">ALIASES</span></span>

## <span data-ttu-id="c4de1-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4de1-161">RELATED LINKS</span></span>

