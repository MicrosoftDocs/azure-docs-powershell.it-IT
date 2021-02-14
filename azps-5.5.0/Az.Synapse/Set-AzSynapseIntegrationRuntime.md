---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188798"
---
# <span data-ttu-id="cd541-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cd541-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="cd541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd541-102">SYNOPSIS</span></span>
<span data-ttu-id="cd541-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="cd541-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd541-104">SYNTAX</span></span>

### <span data-ttu-id="cd541-105">SetByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd541-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="cd541-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="cd541-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd541-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="cd541-107">SetByParentObject</span></span>
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

### <span data-ttu-id="cd541-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="cd541-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd541-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd541-109">SetByResourceId</span></span>
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

### <span data-ttu-id="cd541-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="cd541-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd541-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cd541-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="cd541-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cd541-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd541-113">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd541-113">DESCRIPTION</span></span>
<span data-ttu-id="cd541-114">Il cmdlet **Set-AzSynapseIntegrationRuntime** aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="cd541-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="cd541-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd541-115">EXAMPLES</span></span>

### <span data-ttu-id="cd541-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd541-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="cd541-117">Il cmdlet aggiorna la descrizione del runtime di integrazione denominata "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="cd541-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="cd541-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cd541-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="cd541-119">Il cmdlet aggiunge l'area di lavoro per usare il runtime di integrazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="cd541-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="cd541-120">Quando si `-SharedIntegrationRuntimeResourceId` usa il `-Type` parametro, deve essere incluso anche il parametro.</span><span class="sxs-lookup"><span data-stu-id="cd541-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="cd541-121">Si noti che all'area di lavoro deve essere concessa l'autorizzazione per usare il runtime di integrazione prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd541-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="cd541-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd541-122">PARAMETERS</span></span>

### <span data-ttu-id="cd541-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="cd541-123">-AuthKey</span></span>
<span data-ttu-id="cd541-124">Chiave di autenticazione del runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="cd541-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="cd541-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="cd541-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="cd541-126">Credenziali di amministratore del database del catalogo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cd541-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="cd541-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="cd541-127">-CatalogPricingTier</span></span>
<span data-ttu-id="cd541-128">Livello di prezzi del database di catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="cd541-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd541-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="cd541-130">Endpoint del server di database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="cd541-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="cd541-131">-DataFlowComputeType</span></span>
<span data-ttu-id="cd541-132">Tipo di calcolo del cluster di flusso dei dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="cd541-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="cd541-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="cd541-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="cd541-134">Numero principale del cluster di flusso di dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="cd541-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="cd541-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="cd541-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="cd541-136">Impostazione Tempo di vita (in minuti) del cluster di flusso di dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="cd541-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="cd541-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="cd541-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="cd541-138">Nome Self-Hosted Integration Runtime usato come proxy.</span><span class="sxs-lookup"><span data-stu-id="cd541-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="cd541-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="cd541-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="cd541-140">Nome del servizio collegato Archiviazione BLOB di Azure che fa riferimento all'archivio dati di gestione temporanea da usare per lo spostamento dei dati tra Self-Hosted e Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cd541-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="cd541-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="cd541-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="cd541-142">Il percorso nell'archivio dati di gestione temporanea da usare per lo spostamento dei dati tra i runtime di integrazione Self-Hosted e Azure-SSIS, se non specificato verrà usato un contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cd541-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="cd541-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd541-143">-DefaultProfile</span></span>
<span data-ttu-id="cd541-144">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd541-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd541-145">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd541-145">-Description</span></span>
<span data-ttu-id="cd541-146">Descrizione di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cd541-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="cd541-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="cd541-147">-Edition</span></span>
<span data-ttu-id="cd541-148">L'edizione per il runtime di integrazione SSIS che può essere Standard o Enterprise, se non specificata è Standard.</span><span class="sxs-lookup"><span data-stu-id="cd541-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="cd541-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="cd541-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="cd541-150">Configurazione rapida personalizzata per il runtime di integrazione SSIS che può essere usata per configurare le configurazioni e componenti di terze parti senza script di configurazione personalizzati.</span><span class="sxs-lookup"><span data-stu-id="cd541-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="cd541-151">-Force</span><span class="sxs-lookup"><span data-stu-id="cd541-151">-Force</span></span>
<span data-ttu-id="cd541-152">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cd541-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cd541-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd541-153">-InputObject</span></span>
<span data-ttu-id="cd541-154">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="cd541-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cd541-155">-LicenseType</span></span>
<span data-ttu-id="cd541-156">Il tipo di licenza da selezionare per l'IR SSIS.</span><span class="sxs-lookup"><span data-stu-id="cd541-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="cd541-157">Esistono due tipi: LicenseIncluded o BasePrice.</span><span class="sxs-lookup"><span data-stu-id="cd541-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="cd541-158">Se si è qualificati per il prezzo di Azure Hybrid Use Benefit (AHUB), selezionare BasePrice.</span><span class="sxs-lookup"><span data-stu-id="cd541-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="cd541-159">In caso contrario, seleziona LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="cd541-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="cd541-160">-Location</span><span class="sxs-lookup"><span data-stu-id="cd541-160">-Location</span></span>
<span data-ttu-id="cd541-161">Descrizione di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cd541-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="cd541-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="cd541-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="cd541-163">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="cd541-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="cd541-164">-Name</span><span class="sxs-lookup"><span data-stu-id="cd541-164">-Name</span></span>
<span data-ttu-id="cd541-165">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="cd541-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="cd541-166">-NodeCount</span></span>
<span data-ttu-id="cd541-167">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="cd541-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="cd541-168">-NodeSize</span></span>
<span data-ttu-id="cd541-169">Dimensioni del nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="cd541-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="cd541-170">-PublicIP</span></span>
<span data-ttu-id="cd541-171">Indirizzi IP pubblici statici che verranno utilizzati dal runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="cd541-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd541-172">-ResourceGroupName</span></span>
<span data-ttu-id="cd541-173">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd541-173">Resource group name.</span></span>

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

### <span data-ttu-id="cd541-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd541-174">-ResourceId</span></span>
<span data-ttu-id="cd541-175">Identificatore di risorsa del runtime di integrazione synapse.</span><span class="sxs-lookup"><span data-stu-id="cd541-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="cd541-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="cd541-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="cd541-177">URI di firma di accesso condiviso del contenitore BLOB Azure che contiene lo script di configurazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cd541-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="cd541-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="cd541-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="cd541-179">ID risorsa del runtime di integrazione self-hosted condivisa.</span><span class="sxs-lookup"><span data-stu-id="cd541-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="cd541-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="cd541-180">-Subnet</span></span>
<span data-ttu-id="cd541-181">Nome della subnet nella rete VNet.</span><span class="sxs-lookup"><span data-stu-id="cd541-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="cd541-182">-Type</span><span class="sxs-lookup"><span data-stu-id="cd541-182">-Type</span></span>
<span data-ttu-id="cd541-183">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="cd541-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="cd541-184">-VNetId</span></span>
<span data-ttu-id="cd541-185">ID della rete virtuale a cui verrà join il runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cd541-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="cd541-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd541-186">-WorkspaceName</span></span>
<span data-ttu-id="cd541-187">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="cd541-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cd541-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cd541-188">-WorkspaceObject</span></span>
<span data-ttu-id="cd541-189">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd541-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cd541-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd541-190">-Confirm</span></span>
<span data-ttu-id="cd541-191">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd541-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd541-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd541-192">-WhatIf</span></span>
<span data-ttu-id="cd541-193">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd541-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd541-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd541-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd541-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd541-195">CommonParameters</span></span>
<span data-ttu-id="cd541-196">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd541-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd541-197">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd541-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd541-198">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd541-198">INPUTS</span></span>

### <span data-ttu-id="cd541-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd541-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cd541-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cd541-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cd541-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd541-201">OUTPUTS</span></span>

### <span data-ttu-id="cd541-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cd541-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cd541-203">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd541-203">NOTES</span></span>

## <span data-ttu-id="cd541-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd541-204">RELATED LINKS</span></span>
