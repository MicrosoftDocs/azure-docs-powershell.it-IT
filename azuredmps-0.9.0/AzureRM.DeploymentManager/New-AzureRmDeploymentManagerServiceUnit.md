---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490854"
---
# <span data-ttu-id="a5ca7-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a5ca7-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a5ca7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ca7-103">Crea una nuova unità di servizio in un servizio in una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="a5ca7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5ca7-104">SYNTAX</span></span>

### <span data-ttu-id="a5ca7-105">ByTopologyAndServiceNames (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5ca7-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5ca7-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a5ca7-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ca7-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a5ca7-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ca7-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="a5ca7-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ca7-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ca7-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ca7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5ca7-110">DESCRIPTION</span></span>
<span data-ttu-id="a5ca7-111">Il cmdlet **New-AzureRmDeploymentManagerServiceUnit** crea un servizio in un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="a5ca7-112">Specificare l'unità di servizio in base al nome, al nome del servizio, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="a5ca7-113">Il cmdlet restituisce un oggetto ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="a5ca7-114">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al servizio usando il cmdlet Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="a5ca7-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5ca7-115">EXAMPLES</span></span>

### <span data-ttu-id="a5ca7-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5ca7-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="a5ca7-117">Questo cmdlet crea una nuova unità di servizio con il nome ContosoService2Storage in ContosoResourceGroup sotto il servizio ContosoService2 nella topologia ContosoServiceTopology, nella posizione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="a5ca7-118">I file di modello e parametri sono definiti come percorsi relativi nella posizione di origine dell'elemento a cui fa riferimento la topologia del servizio ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="a5ca7-119">Le risorse definite in questo modello devono essere distribuite nel gruppo di risorse di destinazione service2ResourceGroup con la modalità di distribuzione impostata su incrementale.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="a5ca7-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a5ca7-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="a5ca7-121">Questo cmdlet crea una nuova unità di servizio con il nome ContosoService2Storage in ContosoResourceGroup sotto il servizio ContosoService2 nella topologia ContosoServiceTopology, nella posizione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="a5ca7-122">I riferimenti a modello e parametri vengono forniti come ResourceId di origine degli elementi di SAS come elemento non specificato nella topologia del servizio ContosoServiceTopology1.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="a5ca7-123">Le risorse definite in questo modello devono essere distribuite nel gruppo di risorse di destinazione service2ResourceGroup con la modalità di distribuzione impostata per il completamento.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="a5ca7-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5ca7-124">PARAMETERS</span></span>

### <span data-ttu-id="a5ca7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5ca7-125">-AsJob</span></span>
<span data-ttu-id="a5ca7-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a5ca7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5ca7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ca7-127">-DefaultProfile</span></span>
<span data-ttu-id="a5ca7-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ca7-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a5ca7-129">-DeploymentMode</span></span>
<span data-ttu-id="a5ca7-130">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="a5ca7-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a5ca7-131">-Location</span></span>
<span data-ttu-id="a5ca7-132">Posizione della risorsa dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="a5ca7-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5ca7-133">-Name</span></span>
<span data-ttu-id="a5ca7-134">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="a5ca7-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="a5ca7-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="a5ca7-136">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="a5ca7-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="a5ca7-137">-ParametersUri</span></span>
<span data-ttu-id="a5ca7-138">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="a5ca7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ca7-139">-ResourceGroupName</span></span>
<span data-ttu-id="a5ca7-140">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-140">The resource group.</span></span>

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

### <span data-ttu-id="a5ca7-141">-Servizio</span><span class="sxs-lookup"><span data-stu-id="a5ca7-141">-Service</span></span>
<span data-ttu-id="a5ca7-142">Oggetto Service in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a5ca7-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5ca7-143">-ServiceName</span></span>
<span data-ttu-id="a5ca7-144">Nome del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="a5ca7-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ca7-145">-ServiceResourceId</span></span>
<span data-ttu-id="a5ca7-146">Identificatore della risorsa del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a5ca7-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a5ca7-147">-ServiceTopology</span></span>
<span data-ttu-id="a5ca7-148">Oggetto topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a5ca7-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="a5ca7-149">-ServiceTopologyName</span></span>
<span data-ttu-id="a5ca7-150">Nome della topologia serivce di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="a5ca7-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ca7-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a5ca7-152">Identificatore della risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a5ca7-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5ca7-153">-Tag</span></span>
<span data-ttu-id="a5ca7-154">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="a5ca7-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5ca7-155">-TargetResourceGroup</span></span>
<span data-ttu-id="a5ca7-156">Determina la posizione in cui verranno distribuite le risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="a5ca7-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="a5ca7-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="a5ca7-158">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="a5ca7-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a5ca7-159">-TemplateUri</span></span>
<span data-ttu-id="a5ca7-160">Modalità di distribuzione da usare per la distribuzione delle risorse nell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="a5ca7-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5ca7-161">-Confirm</span></span>
<span data-ttu-id="a5ca7-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ca7-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ca7-163">-WhatIf</span></span>
<span data-ttu-id="a5ca7-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5ca7-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ca7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ca7-166">CommonParameters</span></span>
<span data-ttu-id="a5ca7-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ca7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ca7-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ca7-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ca7-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5ca7-169">INPUTS</span></span>

### <span data-ttu-id="a5ca7-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a5ca7-170">None</span></span>

## <span data-ttu-id="a5ca7-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5ca7-171">OUTPUTS</span></span>

### <span data-ttu-id="a5ca7-172">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a5ca7-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a5ca7-173">Note</span><span class="sxs-lookup"><span data-stu-id="a5ca7-173">NOTES</span></span>

## <span data-ttu-id="a5ca7-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5ca7-174">RELATED LINKS</span></span>

[<span data-ttu-id="a5ca7-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a5ca7-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="a5ca7-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a5ca7-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="a5ca7-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a5ca7-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)