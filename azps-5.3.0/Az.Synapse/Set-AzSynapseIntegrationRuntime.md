---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476575"
---
# <span data-ttu-id="b117b-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b117b-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="b117b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b117b-102">SYNOPSIS</span></span>
<span data-ttu-id="b117b-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="b117b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b117b-104">SYNTAX</span></span>

### <span data-ttu-id="b117b-105">SetByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b117b-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="b117b-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b117b-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="b117b-107">SetByParentObject</span></span>
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

### <span data-ttu-id="b117b-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="b117b-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-109">SetByResourceId</span></span>
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

### <span data-ttu-id="b117b-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b117b-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="b117b-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b117b-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b117b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b117b-113">DESCRIPTION</span></span>
<span data-ttu-id="b117b-114">Il cmdlet **set-AzSynapseIntegrationRuntime** aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="b117b-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="b117b-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b117b-115">EXAMPLES</span></span>

### <span data-ttu-id="b117b-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b117b-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="b117b-117">Il cmdlet aggiorna la descrizione di Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="b117b-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="b117b-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b117b-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="b117b-119">Il cmdlet aggiunge l'area di lavoro per usare il runtime di integrazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="b117b-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="b117b-120">Quando `-SharedIntegrationRuntimeResourceId` si usa il parametro `-Type` deve anche essere incluso.</span><span class="sxs-lookup"><span data-stu-id="b117b-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="b117b-121">Tieni presente che nell'area di lavoro deve essere concessa l'autorizzazione per usare Integration runtime prima di eseguire cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b117b-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="b117b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b117b-122">PARAMETERS</span></span>

### <span data-ttu-id="b117b-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="b117b-123">-AuthKey</span></span>
<span data-ttu-id="b117b-124">Chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="b117b-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="b117b-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="b117b-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="b117b-126">Credenziali di amministratore del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="b117b-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="b117b-127">-CatalogPricingTier</span></span>
<span data-ttu-id="b117b-128">Livello di prezzo del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="b117b-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b117b-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="b117b-130">Endpoint del server di database del catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="b117b-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="b117b-131">-DataFlowComputeType</span></span>
<span data-ttu-id="b117b-132">Tipo di calcolo del cluster flusso di dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="b117b-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="b117b-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="b117b-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="b117b-134">Numero di base del cluster flusso di dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="b117b-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="b117b-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b117b-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="b117b-136">Time to Live (in minutes) dell'impostazione del cluster di flusso di dati che eseguirà il processo del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="b117b-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="b117b-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b117b-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="b117b-138">Il nome Self-Hosted Integration Runtime che viene usato come proxy.</span><span class="sxs-lookup"><span data-stu-id="b117b-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="b117b-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b117b-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="b117b-140">Nome del servizio collegato di Azure BLOB Storage che fa riferimento all'archivio dati di staging da usare quando si spostano i dati tra Self-Hosted e il runtime di integrazione di Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="b117b-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="b117b-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="b117b-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="b117b-142">Il percorso nell'archivio dati di staging da usare quando si spostano dati tra Self-Hosted e i runtime di integrazione di Azure-SSIS, se non specificato, verrà usato un contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b117b-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="b117b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b117b-143">-DefaultProfile</span></span>
<span data-ttu-id="b117b-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b117b-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b117b-145">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b117b-145">-Description</span></span>
<span data-ttu-id="b117b-146">Descrizione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="b117b-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="b117b-147">-Edition</span></span>
<span data-ttu-id="b117b-148">L'Edition for SSIS Integration Runtime che potrebbe essere standard o Enterprise, default è standard se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="b117b-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="b117b-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="b117b-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="b117b-150">La configurazione personalizzata Express per runtime Integration SSIS che potrebbe essere usata per configurare le configurazioni e i componenti di terze parti senza script di configurazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="b117b-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="b117b-151">-Force</span><span class="sxs-lookup"><span data-stu-id="b117b-151">-Force</span></span>
<span data-ttu-id="b117b-152">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b117b-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b117b-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b117b-153">-InputObject</span></span>
<span data-ttu-id="b117b-154">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b117b-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="b117b-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b117b-155">-LicenseType</span></span>
<span data-ttu-id="b117b-156">Tipo di licenza che si desidera selezionare per l'IR SSIS.</span><span class="sxs-lookup"><span data-stu-id="b117b-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="b117b-157">Esistono due tipi: LicenseIncluded o BasePrice.</span><span class="sxs-lookup"><span data-stu-id="b117b-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="b117b-158">Se si è qualificati per i prezzi di Azure Hybrid use benefit (AHUB), selezionare BasePrice.</span><span class="sxs-lookup"><span data-stu-id="b117b-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="b117b-159">In caso contrario, seleziona LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="b117b-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="b117b-160">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b117b-160">-Location</span></span>
<span data-ttu-id="b117b-161">Descrizione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="b117b-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="b117b-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="b117b-163">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="b117b-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="b117b-164">-Nome</span><span class="sxs-lookup"><span data-stu-id="b117b-164">-Name</span></span>
<span data-ttu-id="b117b-165">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="b117b-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b117b-166">-NodeCount</span></span>
<span data-ttu-id="b117b-167">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="b117b-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="b117b-168">-NodeSize</span></span>
<span data-ttu-id="b117b-169">Dimensioni del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="b117b-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="b117b-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="b117b-170">-PublicIP</span></span>
<span data-ttu-id="b117b-171">Indirizzi IP pubblici statici che verranno usati da Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="b117b-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="b117b-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b117b-172">-ResourceGroupName</span></span>
<span data-ttu-id="b117b-173">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b117b-173">Resource group name.</span></span>

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

### <span data-ttu-id="b117b-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-174">-ResourceId</span></span>
<span data-ttu-id="b117b-175">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b117b-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b117b-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="b117b-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="b117b-177">URI SAS del contenitore di Azure BLOB che contiene lo script di configurazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b117b-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="b117b-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="b117b-179">ID risorsa del runtime di integrazione ospitata autonomamente condiviso.</span><span class="sxs-lookup"><span data-stu-id="b117b-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="b117b-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b117b-180">-Subnet</span></span>
<span data-ttu-id="b117b-181">Il nome della subnet in VNet.</span><span class="sxs-lookup"><span data-stu-id="b117b-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="b117b-182">-Digitare</span><span class="sxs-lookup"><span data-stu-id="b117b-182">-Type</span></span>
<span data-ttu-id="b117b-183">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="b117b-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="b117b-184">-VNetId</span></span>
<span data-ttu-id="b117b-185">ID della VNet a cui verrà aggiunto il runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b117b-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="b117b-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b117b-186">-WorkspaceName</span></span>
<span data-ttu-id="b117b-187">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b117b-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b117b-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b117b-188">-WorkspaceObject</span></span>
<span data-ttu-id="b117b-189">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b117b-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b117b-190">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b117b-190">-Confirm</span></span>
<span data-ttu-id="b117b-191">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b117b-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b117b-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b117b-192">-WhatIf</span></span>
<span data-ttu-id="b117b-193">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b117b-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b117b-194">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b117b-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b117b-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b117b-195">CommonParameters</span></span>
<span data-ttu-id="b117b-196">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b117b-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b117b-197">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b117b-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b117b-198">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b117b-198">INPUTS</span></span>

### <span data-ttu-id="b117b-199">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b117b-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b117b-200">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b117b-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b117b-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b117b-201">OUTPUTS</span></span>

### <span data-ttu-id="b117b-202">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b117b-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b117b-203">Note</span><span class="sxs-lookup"><span data-stu-id="b117b-203">NOTES</span></span>

## <span data-ttu-id="b117b-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b117b-204">RELATED LINKS</span></span>
