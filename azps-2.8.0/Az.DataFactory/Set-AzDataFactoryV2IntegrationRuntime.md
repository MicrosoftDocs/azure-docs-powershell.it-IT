---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674924"
---
# <span data-ttu-id="6594d-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6594d-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6594d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6594d-102">SYNOPSIS</span></span>
<span data-ttu-id="6594d-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="6594d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6594d-104">SYNTAX</span></span>

### <span data-ttu-id="6594d-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6594d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6594d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6594d-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6594d-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="6594d-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6594d-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6594d-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6594d-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6594d-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6594d-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6594d-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6594d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6594d-111">DESCRIPTION</span></span>
<span data-ttu-id="6594d-112">Il cmdlet Set-AzDataFactoryV2IntegrationRuntime aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="6594d-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="6594d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6594d-113">EXAMPLES</span></span>

### <span data-ttu-id="6594d-114">Esempio 1: aggiornare la descrizione del runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="6594d-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="6594d-115">Il cmdlet aggiorna la descrizione di Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="6594d-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="6594d-116">Esempio 2: condividere il runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="6594d-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="6594d-117">Il cmdlet aggiunge l'ADF per l'uso del runtime di integrazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="6594d-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="6594d-118">Quando `-SharedIntegrationRuntimeResourceId` si usa il parametro `-Type` deve anche essere incluso.</span><span class="sxs-lookup"><span data-stu-id="6594d-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="6594d-119">Tieni presente che per il data factory deve essere concessa l'autorizzazione per usare Integration runtime prima di eseguire cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6594d-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="6594d-120">Esempio 3: configurare Self-Hosted IR come proxy per Azure-SSIS IR in ADF.</span><span class="sxs-lookup"><span data-stu-id="6594d-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="6594d-121">Il cmdlet aggiorna Azure-runtime Integration di SSIS per usare l'autohosted Integration runtime come proxy di dati.</span><span class="sxs-lookup"><span data-stu-id="6594d-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="6594d-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6594d-122">PARAMETERS</span></span>

### <span data-ttu-id="6594d-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="6594d-123">-AuthKey</span></span>
<span data-ttu-id="6594d-124">Chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="6594d-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="6594d-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="6594d-126">Credenziali di amministratore del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="6594d-127">-CatalogPricingTier</span></span>
<span data-ttu-id="6594d-128">Livello di prezzo del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6594d-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="6594d-130">Endpoint del server di database del catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6594d-131">-DataFactoryName</span></span>
<span data-ttu-id="6594d-132">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="6594d-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6594d-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="6594d-134">Il nome di runtime di Self-Hosted Integration usato come proxy</span><span class="sxs-lookup"><span data-stu-id="6594d-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="6594d-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="6594d-136">Nome del servizio collegato di archiviazione BLOB di Azure che fa riferimento all'archivio dati di staging da usare quando si spostano dati tra Self-Hosted ed Azure-runtime Integration di SSIS</span><span class="sxs-lookup"><span data-stu-id="6594d-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="6594d-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="6594d-138">Il percorso nell'archivio dati di staging da usare quando si spostano dati tra Self-Hosted e i runtime di integrazione di Azure-SSIS, se non specificato viene usato un contenitore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6594d-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6594d-139">-DefaultProfile</span></span>
<span data-ttu-id="6594d-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6594d-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6594d-141">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="6594d-141">-Description</span></span>
<span data-ttu-id="6594d-142">Descrizione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="6594d-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="6594d-143">-Edition</span></span>
<span data-ttu-id="6594d-144">L'Edition for SSIS Integration Runtime che potrebbe essere standard o Enterprise, default è standard se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="6594d-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-145">-Force</span><span class="sxs-lookup"><span data-stu-id="6594d-145">-Force</span></span>
<span data-ttu-id="6594d-146">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6594d-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6594d-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6594d-147">-InputObject</span></span>
<span data-ttu-id="6594d-148">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="6594d-148">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6594d-149">-LicenseType</span></span>
<span data-ttu-id="6594d-150">Tipo di licenza che si desidera selezionare per l'IR SSIS.</span><span class="sxs-lookup"><span data-stu-id="6594d-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="6594d-151">Esistono due tipi: LicenseIncluded o BasePrice.</span><span class="sxs-lookup"><span data-stu-id="6594d-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="6594d-152">Se si è qualificati per i prezzi di Azure Hybrid use benefit (AHUB), selezionare BasePrice.</span><span class="sxs-lookup"><span data-stu-id="6594d-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="6594d-153">In caso contrario, seleziona LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="6594d-153">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-154">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6594d-154">-Location</span></span>
<span data-ttu-id="6594d-155">Posizione di runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="6594d-155">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="6594d-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="6594d-157">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="6594d-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="6594d-158">-Name</span></span>
<span data-ttu-id="6594d-159">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-159">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="6594d-160">-NodeCount</span></span>
<span data-ttu-id="6594d-161">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-161">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="6594d-162">-NodeSize</span></span>
<span data-ttu-id="6594d-163">Dimensioni del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="6594d-163">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6594d-164">-ResourceGroupName</span></span>
<span data-ttu-id="6594d-165">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6594d-165">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6594d-166">-ResourceId</span></span>
<span data-ttu-id="6594d-167">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="6594d-167">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="6594d-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="6594d-169">URI SAS del contenitore di Azure BLOB che contiene lo script di configurazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6594d-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="6594d-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="6594d-171">ID risorsa del runtime di integrazione ospitata autonomamente condiviso.</span><span class="sxs-lookup"><span data-stu-id="6594d-171">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-172">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6594d-172">-Subnet</span></span>
<span data-ttu-id="6594d-173">Il nome della subnet in VNet.</span><span class="sxs-lookup"><span data-stu-id="6594d-173">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-174">-Digitare</span><span class="sxs-lookup"><span data-stu-id="6594d-174">-Type</span></span>
<span data-ttu-id="6594d-175">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6594d-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="6594d-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="6594d-176">-VNetId</span></span>
<span data-ttu-id="6594d-177">ID della VNet in cui si unisce Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="6594d-177">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6594d-178">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6594d-178">-Confirm</span></span>
<span data-ttu-id="6594d-179">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6594d-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6594d-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6594d-180">-WhatIf</span></span>
<span data-ttu-id="6594d-181">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6594d-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6594d-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6594d-182">CommonParameters</span></span>
<span data-ttu-id="6594d-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6594d-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6594d-184">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6594d-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6594d-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6594d-185">INPUTS</span></span>

### <span data-ttu-id="6594d-186">System. String</span><span class="sxs-lookup"><span data-stu-id="6594d-186">System.String</span></span>

### <span data-ttu-id="6594d-187">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6594d-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6594d-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6594d-188">OUTPUTS</span></span>

### <span data-ttu-id="6594d-189">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6594d-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6594d-190">Note</span><span class="sxs-lookup"><span data-stu-id="6594d-190">NOTES</span></span>

## <span data-ttu-id="6594d-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6594d-191">RELATED LINKS</span></span>

[<span data-ttu-id="6594d-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6594d-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
