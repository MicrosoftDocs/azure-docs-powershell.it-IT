---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: a76731c52de32f8b92ed244f82c6afd69bab32d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007486"
---
# <span data-ttu-id="c4999-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c4999-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="c4999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4999-102">SYNOPSIS</span></span>
<span data-ttu-id="c4999-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="c4999-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4999-104">SYNTAX</span></span>

### <span data-ttu-id="c4999-105">SetByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4999-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c4999-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="c4999-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="c4999-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4999-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c4999-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c4999-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4999-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c4999-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4999-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4999-113">DESCRIPTION</span></span>
<span data-ttu-id="c4999-114">Il cmdlet **Set-AzSynapseIntegrationRuntime** aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="c4999-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="c4999-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4999-115">EXAMPLES</span></span>

### <span data-ttu-id="c4999-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c4999-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="c4999-117">Il cmdlet aggiorna la descrizione del runtime di integrazione denominata "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="c4999-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="c4999-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c4999-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="c4999-119">Il cmdlet aggiunge l'area di lavoro per usare il runtime di integrazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="c4999-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="c4999-120">Quando si `-SharedIntegrationRuntimeResourceId` usa il `-Type` parametro, deve essere incluso anche il parametro.</span><span class="sxs-lookup"><span data-stu-id="c4999-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="c4999-121">Si noti che all'area di lavoro deve essere concessa l'autorizzazione per usare il runtime di integrazione prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4999-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="c4999-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4999-122">PARAMETERS</span></span>

### <span data-ttu-id="c4999-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="c4999-123">-AuthKey</span></span>
<span data-ttu-id="c4999-124">Chiave di autenticazione del runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="c4999-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="c4999-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="c4999-126">Credenziali di amministratore del database del catalogo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="c4999-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="c4999-127">-CatalogPricingTier</span></span>
<span data-ttu-id="c4999-128">Livello di prezzi del database dei cataloghi del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c4999-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="c4999-130">Endpoint del server di database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="c4999-131">-DataFlowComputeType</span></span>
<span data-ttu-id="c4999-132">Tipo di calcolo del cluster di flusso dei dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="c4999-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="c4999-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="c4999-134">Numero principale del cluster di flusso dei dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="c4999-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c4999-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="c4999-136">Impostazione Tempo di vita (in minuti) del cluster di flusso di dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="c4999-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c4999-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="c4999-138">Nome Self-Hosted Integration Runtime usato come proxy.</span><span class="sxs-lookup"><span data-stu-id="c4999-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c4999-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="c4999-140">Nome del servizio collegato Archiviazione BLOB di Azure che fa riferimento all'archivio dati di gestione temporanea da usare per lo spostamento dei dati tra Self-Hosted e Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="c4999-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="c4999-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="c4999-142">Percorso nell'archivio dati di gestione temporanea da usare per lo spostamento dei dati tra i runtime di integrazione Self-Hosted e Azure-SSIS, se non specificato verrà usato un contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c4999-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4999-143">-DefaultProfile</span></span>
<span data-ttu-id="c4999-144">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4999-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4999-145">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4999-145">-Description</span></span>
<span data-ttu-id="c4999-146">Descrizione di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="c4999-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="c4999-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="c4999-147">-Edition</span></span>
<span data-ttu-id="c4999-148">L'edizione per il runtime di integrazione SSIS che può essere Standard o Enterprise, se non è specificata, è Standard.</span><span class="sxs-lookup"><span data-stu-id="c4999-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="c4999-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="c4999-150">Configurazione rapida personalizzata per il runtime di integrazione SSIS che può essere usata per configurare le configurazioni e componenti di terze parti senza script di configurazione personalizzati.</span><span class="sxs-lookup"><span data-stu-id="c4999-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-151">-Force</span><span class="sxs-lookup"><span data-stu-id="c4999-151">-Force</span></span>
<span data-ttu-id="c4999-152">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c4999-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c4999-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4999-153">-InputObject</span></span>
<span data-ttu-id="c4999-154">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c4999-155">-LicenseType</span></span>
<span data-ttu-id="c4999-156">Il tipo di licenza da selezionare per l'IR SSIS.</span><span class="sxs-lookup"><span data-stu-id="c4999-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="c4999-157">Esistono due tipi: LicenseIncluded o BasePrice.</span><span class="sxs-lookup"><span data-stu-id="c4999-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="c4999-158">Se si è qualificati per il prezzo di Azure Hybrid Use Benefit (AHUB), selezionare BasePrice.</span><span class="sxs-lookup"><span data-stu-id="c4999-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="c4999-159">In caso contrario, seleziona LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="c4999-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-160">-Location</span><span class="sxs-lookup"><span data-stu-id="c4999-160">-Location</span></span>
<span data-ttu-id="c4999-161">Descrizione di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="c4999-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="c4999-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="c4999-163">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="c4999-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-164">-Name</span><span class="sxs-lookup"><span data-stu-id="c4999-164">-Name</span></span>
<span data-ttu-id="c4999-165">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c4999-166">-NodeCount</span></span>
<span data-ttu-id="c4999-167">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c4999-168">-NodeSize</span></span>
<span data-ttu-id="c4999-169">Dimensioni del nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="c4999-170">-PublicIP</span></span>
<span data-ttu-id="c4999-171">Indirizzi IP pubblici statici che verranno utilizzati da Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="c4999-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4999-172">-ResourceGroupName</span></span>
<span data-ttu-id="c4999-173">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4999-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4999-174">-ResourceId</span></span>
<span data-ttu-id="c4999-175">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="c4999-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c4999-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="c4999-177">URI di firma di accesso condiviso del contenitore BLOB azure che contiene lo script di configurazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c4999-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c4999-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="c4999-179">ID risorsa del runtime di integrazione self-hosted condivisa.</span><span class="sxs-lookup"><span data-stu-id="c4999-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c4999-180">-Subnet</span></span>
<span data-ttu-id="c4999-181">Nome della subnet nella rete VNet.</span><span class="sxs-lookup"><span data-stu-id="c4999-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-182">-Type</span><span class="sxs-lookup"><span data-stu-id="c4999-182">-Type</span></span>
<span data-ttu-id="c4999-183">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="c4999-184">-VNetId</span></span>
<span data-ttu-id="c4999-185">ID della rete virtuale a cui verrà join il runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c4999-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c4999-186">-WorkspaceName</span></span>
<span data-ttu-id="c4999-187">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c4999-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c4999-188">-WorkspaceObject</span></span>
<span data-ttu-id="c4999-189">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c4999-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4999-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4999-190">-Confirm</span></span>
<span data-ttu-id="c4999-191">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4999-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4999-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4999-192">-WhatIf</span></span>
<span data-ttu-id="c4999-193">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4999-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4999-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4999-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4999-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4999-195">CommonParameters</span></span>
<span data-ttu-id="c4999-196">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4999-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4999-197">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4999-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4999-198">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4999-198">INPUTS</span></span>

### <span data-ttu-id="c4999-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c4999-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c4999-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c4999-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c4999-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4999-201">OUTPUTS</span></span>

### <span data-ttu-id="c4999-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c4999-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c4999-203">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4999-203">NOTES</span></span>

## <span data-ttu-id="c4999-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4999-204">RELATED LINKS</span></span>
