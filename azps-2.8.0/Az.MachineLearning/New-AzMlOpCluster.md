---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673927"
---
# <span data-ttu-id="952a5-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="952a5-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="952a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="952a5-102">SYNOPSIS</span></span>
<span data-ttu-id="952a5-103">Crea un nuovo cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="952a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="952a5-104">SYNTAX</span></span>

### <span data-ttu-id="952a5-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="952a5-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="952a5-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="952a5-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="952a5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="952a5-107">DESCRIPTION</span></span>
<span data-ttu-id="952a5-108">Crea un nuovo cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="952a5-109">Verrà creato un oggetto cluster, un servizio contenitore, se necessario, informazioni sulle applicazioni e un registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="952a5-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="952a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="952a5-110">EXAMPLES</span></span>

### <span data-ttu-id="952a5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="952a5-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="952a5-112">Crea un nuovo cluster di operatività con Azure Container Service e Kubernetes come orchestratore.</span><span class="sxs-lookup"><span data-stu-id="952a5-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="952a5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="952a5-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="952a5-114">Crea un nuovo cluster di operatività localmente.</span><span class="sxs-lookup"><span data-stu-id="952a5-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="952a5-115">In questo modo viene creato un registro di sistema, informazioni dettagliate sull'applicazione e un account di archiviazione di Azure, ma non viene creato un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="952a5-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="952a5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="952a5-116">PARAMETERS</span></span>

### <span data-ttu-id="952a5-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="952a5-117">-AgentCount</span></span>
<span data-ttu-id="952a5-118">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="952a5-119">-AgentVmSize</span></span>
<span data-ttu-id="952a5-120">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="952a5-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="952a5-122">L'URI al registro di sistema di Azure container da usare invece di crearne uno.</span><span class="sxs-lookup"><span data-stu-id="952a5-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-123">-ClientID</span><span class="sxs-lookup"><span data-stu-id="952a5-123">-ClientId</span></span>
<span data-ttu-id="952a5-124">ID entità del servizio di orchestrazione del cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="952a5-125">-ClusterType</span></span>
<span data-ttu-id="952a5-126">Tipo di cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952a5-127">-DefaultProfile</span></span>
<span data-ttu-id="952a5-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="952a5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="952a5-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="952a5-129">-Description</span></span>
<span data-ttu-id="952a5-130">Numero di nodi master nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="952a5-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="952a5-132">Proprietà aggiuntive per la configurazione del servizio globale.</span><span class="sxs-lookup"><span data-stu-id="952a5-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="952a5-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="952a5-134">L'ETag della configurazione per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="952a5-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="952a5-135">-InputObject</span></span>
<span data-ttu-id="952a5-136">Proprietà del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="952a5-137">-Location</span></span>
<span data-ttu-id="952a5-138">Posizione del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="952a5-139">-MasterCount</span></span>
<span data-ttu-id="952a5-140">Numero di nodi master nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="952a5-141">-Name</span></span>
<span data-ttu-id="952a5-142">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="952a5-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="952a5-143">-OrchestratorType</span></span>
<span data-ttu-id="952a5-144">Tipo di agente di orchestrazione del cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952a5-145">-ResourceGroupName</span></span>
<span data-ttu-id="952a5-146">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="952a5-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="952a5-147">-Segreto</span><span class="sxs-lookup"><span data-stu-id="952a5-147">-Secret</span></span>
<span data-ttu-id="952a5-148">Segreto principale del servizio di orchestrazione del cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="952a5-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="952a5-149">-SslCertificate</span></span>
<span data-ttu-id="952a5-150">Dati del certificato SSL in formato PEM codificati come stringa Base64.</span><span class="sxs-lookup"><span data-stu-id="952a5-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="952a5-151">-SslCName</span></span>
<span data-ttu-id="952a5-152">Il CName per il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="952a5-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="952a5-153">-SslKey</span></span>
<span data-ttu-id="952a5-154">Dati della chiave SSL in formato PEM codificati come stringa Base64.</span><span class="sxs-lookup"><span data-stu-id="952a5-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="952a5-155">-SslStatus</span></span>
<span data-ttu-id="952a5-156">Stato SSL.</span><span class="sxs-lookup"><span data-stu-id="952a5-156">SSL status.</span></span>
<span data-ttu-id="952a5-157">I valori possibili sono "Enabled" e "disabled".</span><span class="sxs-lookup"><span data-stu-id="952a5-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="952a5-158">-StorageAccount</span></span>
<span data-ttu-id="952a5-159">L'URI per l'account di archiviazione da usare invece di crearne uno.</span><span class="sxs-lookup"><span data-stu-id="952a5-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952a5-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="952a5-160">-Confirm</span></span>
<span data-ttu-id="952a5-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="952a5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="952a5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952a5-162">-WhatIf</span></span>
<span data-ttu-id="952a5-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="952a5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952a5-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="952a5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="952a5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952a5-165">CommonParameters</span></span>
<span data-ttu-id="952a5-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952a5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952a5-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="952a5-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952a5-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="952a5-168">INPUTS</span></span>

### <span data-ttu-id="952a5-169">Nessuno</span><span class="sxs-lookup"><span data-stu-id="952a5-169">None</span></span>

## <span data-ttu-id="952a5-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="952a5-170">OUTPUTS</span></span>

### <span data-ttu-id="952a5-171">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="952a5-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="952a5-172">Note</span><span class="sxs-lookup"><span data-stu-id="952a5-172">NOTES</span></span>

## <span data-ttu-id="952a5-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="952a5-173">RELATED LINKS</span></span>