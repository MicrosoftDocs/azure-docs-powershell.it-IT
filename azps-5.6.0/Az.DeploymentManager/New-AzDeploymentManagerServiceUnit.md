---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 5c4b418812c6cbe3ee1b5e1f8ee82baa05723f86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962158"
---
# <span data-ttu-id="c1b23-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="c1b23-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="c1b23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b23-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b23-103">Crea un'unità di servizio nella topologia di servizio e di servizio specificata.</span><span class="sxs-lookup"><span data-stu-id="c1b23-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="c1b23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1b23-104">SYNTAX</span></span>

### <span data-ttu-id="c1b23-105">ByTopologyAndServiceNames (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1b23-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1b23-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c1b23-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1b23-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="c1b23-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1b23-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="c1b23-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1b23-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c1b23-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1b23-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c1b23-110">DESCRIPTION</span></span>
<span data-ttu-id="c1b23-111">Il cmdlet **New-AzDeploymentManagerServiceUnit** crea un servizio in un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="c1b23-112">Specificare l'unità di servizio in base al nome, al nome del servizio, alla topologia di servizio in cui si trova e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1b23-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="c1b23-113">Il cmdlet restituisce un oggetto ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="c1b23-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="c1b23-114">È possibile modificare l'oggetto in locale e quindi applicarvi le modifiche usando il cmdlet Set-AzDeploymentManagerService servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="c1b23-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1b23-115">EXAMPLES</span></span>

### <span data-ttu-id="c1b23-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1b23-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="c1b23-117">Questo cmdlet crea una nuova unità di servizio con il nome ContosoService2Storage in ContosoResourceGroup nel servizio ContosoService2 in topologia ContosoServiceTopology, nella posizione Stati Uniti centrale.</span><span class="sxs-lookup"><span data-stu-id="c1b23-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="c1b23-118">I file di modelli e parametri sono definiti come percorsi relativi nel percorso di origine dell'elemento a cui si fa riferimento nella topologia di servizio ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c1b23-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="c1b23-119">Le risorse definite in questo modello devono essere distribuite nel gruppo di risorse di destinazione service2ResourceGroup con la modalità di distribuzione impostata su Incrementale.</span><span class="sxs-lookup"><span data-stu-id="c1b23-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="c1b23-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c1b23-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="c1b23-121">Questo cmdlet crea una nuova unità di servizio con il nome ContosoService2Storage in ContosoResourceGroup nel servizio ContosoService2 in topologia ContosoServiceTopology, nella posizione Stati Uniti centrale.</span><span class="sxs-lookup"><span data-stu-id="c1b23-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="c1b23-122">I riferimenti a modelli e parametri vengono forniti come URI della firma di accesso condiviso perché ResourceId dell'origine dell'elemento non è stato fornito nella topologia di servizio ContosoServiceTopology1.</span><span class="sxs-lookup"><span data-stu-id="c1b23-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="c1b23-123">Le risorse definite in questo modello devono essere distribuite nel gruppo di risorse di destinazione service2ResourceGroup con la modalità di distribuzione impostata su Complete.</span><span class="sxs-lookup"><span data-stu-id="c1b23-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="c1b23-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1b23-124">PARAMETERS</span></span>

### <span data-ttu-id="c1b23-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1b23-125">-AsJob</span></span>
<span data-ttu-id="c1b23-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c1b23-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1b23-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b23-127">-DefaultProfile</span></span>
<span data-ttu-id="c1b23-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b23-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="c1b23-129">-DeploymentMode</span></span>
<span data-ttu-id="c1b23-130">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-131">-Location</span><span class="sxs-lookup"><span data-stu-id="c1b23-131">-Location</span></span>
<span data-ttu-id="c1b23-132">Posizione della risorsa dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="c1b23-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c1b23-133">-Name</span></span>
<span data-ttu-id="c1b23-134">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c1b23-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="c1b23-136">Percorso del file di parametri relativo all'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c1b23-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="c1b23-137">Richiede che ArtifactSource sia indicato in ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c1b23-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="c1b23-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="c1b23-138">-ParametersUri</span></span>
<span data-ttu-id="c1b23-139">Uri della firma di accesso condiviso nel file di parametri.</span><span class="sxs-lookup"><span data-stu-id="c1b23-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="c1b23-140">Se ArtifactSourceId è stato fatto riferimento in ServiceTopology, specificare il percorso relativo usando ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="c1b23-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="c1b23-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b23-141">-ResourceGroupName</span></span>
<span data-ttu-id="c1b23-142">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c1b23-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c1b23-143">-ServiceName</span></span>
<span data-ttu-id="c1b23-144">Il nome del servizio di cui fa parte questa unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="c1b23-145">-ServiceObject</span></span>
<span data-ttu-id="c1b23-146">Oggetto servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="c1b23-147">-ServiceResourceId</span></span>
<span data-ttu-id="c1b23-148">Identificatore della risorsa servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="c1b23-149">-ServiceTopologyName</span></span>
<span data-ttu-id="c1b23-150">Il nome della topologia di servizio di questa unità di servizio fa parte di.</span><span class="sxs-lookup"><span data-stu-id="c1b23-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c1b23-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="c1b23-152">Oggetto topologia di servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c1b23-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="c1b23-154">Identificatore di risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1b23-155">-Tag</span></span>
<span data-ttu-id="c1b23-156">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1b23-156">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b23-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1b23-157">-TargetResourceGroup</span></span>
<span data-ttu-id="c1b23-158">Determina la posizione in cui verranno distribuite le risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="c1b23-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="c1b23-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c1b23-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="c1b23-160">Percorso del file modello relativo all'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c1b23-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="c1b23-161">Richiede che ArtifactSource sia indicato in ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c1b23-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="c1b23-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c1b23-162">-TemplateUri</span></span>
<span data-ttu-id="c1b23-163">URI della firma di accesso condiviso nel file modello.</span><span class="sxs-lookup"><span data-stu-id="c1b23-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="c1b23-164">Se ArtifactSourceId è stato fatto riferimento in ServiceTopology, specificare il percorso relativo usando TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="c1b23-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="c1b23-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1b23-165">-Confirm</span></span>
<span data-ttu-id="c1b23-166">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1b23-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1b23-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1b23-167">-WhatIf</span></span>
<span data-ttu-id="c1b23-168">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1b23-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1b23-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1b23-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1b23-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b23-170">CommonParameters</span></span>
<span data-ttu-id="c1b23-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b23-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b23-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1b23-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b23-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="c1b23-173">INPUTS</span></span>

### <span data-ttu-id="c1b23-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c1b23-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c1b23-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1b23-175">OUTPUTS</span></span>

### <span data-ttu-id="c1b23-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="c1b23-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="c1b23-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="c1b23-177">NOTES</span></span>

## <span data-ttu-id="c1b23-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1b23-178">RELATED LINKS</span></span>
