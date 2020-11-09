---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297199"
---
# <span data-ttu-id="15a5f-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="15a5f-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="15a5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="15a5f-103">Crea un'unità di servizio nella topologia di servizio e servizio specificata.</span><span class="sxs-lookup"><span data-stu-id="15a5f-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="15a5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15a5f-104">SYNTAX</span></span>

### <span data-ttu-id="15a5f-105">ByTopologyAndServiceNames (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15a5f-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15a5f-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="15a5f-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a5f-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="15a5f-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a5f-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="15a5f-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a5f-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="15a5f-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a5f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15a5f-110">DESCRIPTION</span></span>
<span data-ttu-id="15a5f-111">Il cmdlet **New-AzDeploymentManagerServiceUnit** crea un servizio in un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="15a5f-112">Specificare l'unità di servizio in base al nome, al nome del servizio, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15a5f-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="15a5f-113">Il cmdlet restituisce un oggetto ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="15a5f-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="15a5f-114">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al servizio usando il cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="15a5f-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="15a5f-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15a5f-115">EXAMPLES</span></span>

### <span data-ttu-id="15a5f-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15a5f-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="15a5f-117">Questo cmdlet crea una nuova unità di servizio con il nome ContosoService2Storage in ContosoResourceGroup sotto il servizio ContosoService2 nella topologia ContosoServiceTopology, nella posizione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="15a5f-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="15a5f-118">I file di modello e parametri sono definiti come percorsi relativi nella posizione di origine dell'elemento a cui fa riferimento la topologia del servizio ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="15a5f-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="15a5f-119">Le risorse definite in questo modello devono essere distribuite nel gruppo di risorse di destinazione service2ResourceGroup con la modalità di distribuzione impostata su incrementale.</span><span class="sxs-lookup"><span data-stu-id="15a5f-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="15a5f-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="15a5f-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="15a5f-121">Questo cmdlet crea una nuova unità di servizio con il nome ContosoService2Storage in ContosoResourceGroup sotto il servizio ContosoService2 nella topologia ContosoServiceTopology, nella posizione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="15a5f-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="15a5f-122">I riferimenti a modello e parametri vengono forniti come ResourceId di origine degli elementi di SAS come elemento non specificato nella topologia del servizio ContosoServiceTopology1.</span><span class="sxs-lookup"><span data-stu-id="15a5f-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="15a5f-123">Le risorse definite in questo modello devono essere distribuite nel gruppo di risorse di destinazione service2ResourceGroup con la modalità di distribuzione impostata per il completamento.</span><span class="sxs-lookup"><span data-stu-id="15a5f-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="15a5f-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15a5f-124">PARAMETERS</span></span>

### <span data-ttu-id="15a5f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15a5f-125">-AsJob</span></span>
<span data-ttu-id="15a5f-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="15a5f-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15a5f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a5f-127">-DefaultProfile</span></span>
<span data-ttu-id="15a5f-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15a5f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a5f-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="15a5f-129">-DeploymentMode</span></span>
<span data-ttu-id="15a5f-130">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="15a5f-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="15a5f-131">-Location</span></span>
<span data-ttu-id="15a5f-132">Posizione della risorsa dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="15a5f-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a5f-133">-Name</span></span>
<span data-ttu-id="15a5f-134">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="15a5f-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="15a5f-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="15a5f-136">Il percorso del file Parameters relativo all'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="15a5f-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="15a5f-137">Richiede il riferimento a ArtifactSource in ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="15a5f-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="15a5f-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="15a5f-138">-ParametersUri</span></span>
<span data-ttu-id="15a5f-139">URI SAS per il file Parameters.</span><span class="sxs-lookup"><span data-stu-id="15a5f-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="15a5f-140">Se nel ServiceTopology è stato fatto riferimento a ArtifactSourceId, specificare il percorso relativo usando ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="15a5f-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="15a5f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a5f-141">-ResourceGroupName</span></span>
<span data-ttu-id="15a5f-142">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="15a5f-142">The resource group.</span></span>

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

### <span data-ttu-id="15a5f-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="15a5f-143">-ServiceName</span></span>
<span data-ttu-id="15a5f-144">Nome del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="15a5f-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="15a5f-145">-ServiceObject</span></span>
<span data-ttu-id="15a5f-146">Oggetto Service in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="15a5f-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="15a5f-147">-ServiceResourceId</span></span>
<span data-ttu-id="15a5f-148">Identificatore della risorsa del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="15a5f-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="15a5f-149">-ServiceTopologyName</span></span>
<span data-ttu-id="15a5f-150">Nome della topologia del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="15a5f-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="15a5f-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="15a5f-152">Oggetto topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="15a5f-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="15a5f-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="15a5f-154">Identificatore della risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="15a5f-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="15a5f-155">-Tag</span></span>
<span data-ttu-id="15a5f-156">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="15a5f-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="15a5f-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="15a5f-157">-TargetResourceGroup</span></span>
<span data-ttu-id="15a5f-158">Determina la posizione in cui verranno distribuite le risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="15a5f-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="15a5f-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="15a5f-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="15a5f-160">Il percorso del file modello relativo all'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="15a5f-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="15a5f-161">Richiede il riferimento a ArtifactSource in ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="15a5f-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="15a5f-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="15a5f-162">-TemplateUri</span></span>
<span data-ttu-id="15a5f-163">URI SAS per il file di modello.</span><span class="sxs-lookup"><span data-stu-id="15a5f-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="15a5f-164">Se nel ServiceTopology è stato fatto riferimento a ArtifactSourceId, specificare il percorso relativo usando TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="15a5f-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="15a5f-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15a5f-165">-Confirm</span></span>
<span data-ttu-id="15a5f-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15a5f-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a5f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a5f-167">-WhatIf</span></span>
<span data-ttu-id="15a5f-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a5f-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a5f-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15a5f-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a5f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a5f-170">CommonParameters</span></span>
<span data-ttu-id="15a5f-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a5f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a5f-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15a5f-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a5f-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15a5f-173">INPUTS</span></span>

### <span data-ttu-id="15a5f-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="15a5f-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15a5f-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15a5f-175">OUTPUTS</span></span>

### <span data-ttu-id="15a5f-176">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="15a5f-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="15a5f-177">Note</span><span class="sxs-lookup"><span data-stu-id="15a5f-177">NOTES</span></span>

## <span data-ttu-id="15a5f-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15a5f-178">RELATED LINKS</span></span>
