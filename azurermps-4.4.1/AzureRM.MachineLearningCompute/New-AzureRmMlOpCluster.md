---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519576"
---
# <span data-ttu-id="1fe26-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="1fe26-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="1fe26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fe26-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe26-103">Crea un nuovo cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fe26-104">SYNTAX</span></span>

### <span data-ttu-id="1fe26-105">Creare un nuovo cluster di operatività da una definizione di istanza di OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="1fe26-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1fe26-106">Creare un nuovo cluster di operatività da parametri di input cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe26-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1fe26-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe26-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe26-108">Crea un nuovo cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="1fe26-109">Verrà creato un oggetto cluster, un servizio contenitore, se necessario, informazioni sulle applicazioni e un registro di sistema di Azure container.</span><span class="sxs-lookup"><span data-stu-id="1fe26-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="1fe26-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fe26-110">EXAMPLES</span></span>

### <span data-ttu-id="1fe26-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1fe26-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="1fe26-112">Crea un nuovo cluster di operatività con Azure Container Service e Kubernetes come orchestratore.</span><span class="sxs-lookup"><span data-stu-id="1fe26-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="1fe26-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1fe26-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="1fe26-114">Crea un nuovo cluster di operatività localmente.</span><span class="sxs-lookup"><span data-stu-id="1fe26-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="1fe26-115">In questo modo viene creato un registro di sistema, informazioni dettagliate sull'applicazione e un account di archiviazione di Azure, ma non viene creato un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="1fe26-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="1fe26-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fe26-116">PARAMETERS</span></span>

### <span data-ttu-id="1fe26-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="1fe26-117">-AgentCount</span></span>
<span data-ttu-id="1fe26-118">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="1fe26-119">-AgentVmSize</span></span>
<span data-ttu-id="1fe26-120">Numero di nodi agente nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1fe26-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="1fe26-122">L'URI al registro di sistema di Azure container da usare invece di crearne uno.</span><span class="sxs-lookup"><span data-stu-id="1fe26-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe26-123">-InputObject</span></span>
<span data-ttu-id="1fe26-124">Proprietà del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="1fe26-125">-ClusterType</span></span>
<span data-ttu-id="1fe26-126">Tipo di cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fe26-127">-Confirm</span></span>
<span data-ttu-id="1fe26-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe26-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-129">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe26-129">-Description</span></span>
<span data-ttu-id="1fe26-130">Numero di nodi master nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="1fe26-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="1fe26-132">Proprietà aggiuntive per la configurazione del servizio globale.</span><span class="sxs-lookup"><span data-stu-id="1fe26-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="1fe26-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="1fe26-134">L'ETag della configurazione per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="1fe26-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1fe26-135">-Location</span></span>
<span data-ttu-id="1fe26-136">Posizione del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="1fe26-137">-MasterCount</span></span>
<span data-ttu-id="1fe26-138">Numero di nodi master nel cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fe26-139">-Name</span></span>
<span data-ttu-id="1fe26-140">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="1fe26-141">-OrchestratorType</span></span>
<span data-ttu-id="1fe26-142">Tipo di agente di orchestrazione del cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe26-143">-ResourceGroupName</span></span>
<span data-ttu-id="1fe26-144">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="1fe26-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-145">-ClientID</span><span class="sxs-lookup"><span data-stu-id="1fe26-145">-ClientId</span></span>
<span data-ttu-id="1fe26-146">ID entità del servizio di orchestrazione del cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-147">-Segreto</span><span class="sxs-lookup"><span data-stu-id="1fe26-147">-Secret</span></span>
<span data-ttu-id="1fe26-148">Segreto principale del servizio di orchestrazione del cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="1fe26-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="1fe26-149">-SslCName</span></span>
<span data-ttu-id="1fe26-150">Il CName per il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="1fe26-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe26-151">-SslCertificate</span></span>
<span data-ttu-id="1fe26-152">Dati del certificato SSL in formato PEM codificati come stringa Base64.</span><span class="sxs-lookup"><span data-stu-id="1fe26-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="1fe26-153">-SslKey</span></span>
<span data-ttu-id="1fe26-154">Dati della chiave SSL in formato PEM codificati come stringa Base64.</span><span class="sxs-lookup"><span data-stu-id="1fe26-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="1fe26-155">-SslStatus</span></span>
<span data-ttu-id="1fe26-156">Stato SSL.</span><span class="sxs-lookup"><span data-stu-id="1fe26-156">SSL status.</span></span>
<span data-ttu-id="1fe26-157">I valori possibili sono "Enabled" e "disabled".</span><span class="sxs-lookup"><span data-stu-id="1fe26-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1fe26-158">-StorageAccount</span></span>
<span data-ttu-id="1fe26-159">L'URI per l'account di archiviazione da usare invece di crearne uno.</span><span class="sxs-lookup"><span data-stu-id="1fe26-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe26-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe26-160">-WhatIf</span></span>
<span data-ttu-id="1fe26-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fe26-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe26-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fe26-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1fe26-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fe26-163">INPUTS</span></span>

### <span data-ttu-id="1fe26-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1fe26-164">None</span></span>


## <span data-ttu-id="1fe26-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fe26-165">OUTPUTS</span></span>

### <span data-ttu-id="1fe26-166">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="1fe26-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="1fe26-167">Note</span><span class="sxs-lookup"><span data-stu-id="1fe26-167">NOTES</span></span>

## <span data-ttu-id="1fe26-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fe26-168">RELATED LINKS</span></span>

