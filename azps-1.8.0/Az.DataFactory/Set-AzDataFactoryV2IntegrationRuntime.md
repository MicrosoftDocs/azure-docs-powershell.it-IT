---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836451"
---
# <span data-ttu-id="5b59f-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b59f-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5b59f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b59f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b59f-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="5b59f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b59f-104">SYNTAX</span></span>

### <span data-ttu-id="5b59f-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b59f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b59f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b59f-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b59f-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="5b59f-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b59f-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5b59f-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b59f-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5b59f-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b59f-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5b59f-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b59f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b59f-111">DESCRIPTION</span></span>
<span data-ttu-id="5b59f-112">Il cmdlet Set-AzDataFactoryV2IntegrationRuntime aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="5b59f-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="5b59f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b59f-113">EXAMPLES</span></span>

### <span data-ttu-id="5b59f-114">Esempio 1: aggiornare la descrizione del runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="5b59f-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="5b59f-115">Il cmdlet aggiorna la descrizione di Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="5b59f-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="5b59f-116">Esempio 2: condividere il runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="5b59f-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="5b59f-117">Il cmdlet aggiunge l'ADF per l'uso del runtime di integrazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="5b59f-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="5b59f-118">Quando `-SharedIntegrationRuntimeResourceId` si usa il parametro `-Type` deve anche essere incluso.</span><span class="sxs-lookup"><span data-stu-id="5b59f-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="5b59f-119">Tieni presente che per il data factory deve essere concessa l'autorizzazione per usare Integration runtime prima di eseguire cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b59f-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="5b59f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b59f-120">PARAMETERS</span></span>

### <span data-ttu-id="5b59f-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="5b59f-121">-AuthKey</span></span>
<span data-ttu-id="5b59f-122">Chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="5b59f-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="5b59f-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="5b59f-124">Credenziali di amministratore del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="5b59f-125">-CatalogPricingTier</span></span>
<span data-ttu-id="5b59f-126">Livello di prezzo del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b59f-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="5b59f-128">Endpoint del server di database del catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-129">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5b59f-129">-DataFactoryName</span></span>
<span data-ttu-id="5b59f-130">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="5b59f-130">The data factory name.</span></span>

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

### <span data-ttu-id="5b59f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b59f-131">-DefaultProfile</span></span>
<span data-ttu-id="5b59f-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b59f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b59f-133">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b59f-133">-Description</span></span>
<span data-ttu-id="5b59f-134">Descrizione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="5b59f-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="5b59f-135">-Edition</span></span>
<span data-ttu-id="5b59f-136">L'Edition for SSIS Integration Runtime che potrebbe essere standard o Enterprise, default è standard se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="5b59f-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="5b59f-137">-Force</span><span class="sxs-lookup"><span data-stu-id="5b59f-137">-Force</span></span>
<span data-ttu-id="5b59f-138">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5b59f-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5b59f-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b59f-139">-InputObject</span></span>
<span data-ttu-id="5b59f-140">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="5b59f-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="5b59f-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5b59f-141">-LicenseType</span></span>
<span data-ttu-id="5b59f-142">Tipo di licenza che si desidera selezionare per l'IR SSIS.</span><span class="sxs-lookup"><span data-stu-id="5b59f-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="5b59f-143">Esistono due tipi: LicenseIncluded o BasePrice.</span><span class="sxs-lookup"><span data-stu-id="5b59f-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="5b59f-144">Se si è qualificati per i prezzi di Azure Hybrid use benefit (AHUB), selezionare BasePrice.</span><span class="sxs-lookup"><span data-stu-id="5b59f-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="5b59f-145">In caso contrario, seleziona LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="5b59f-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="5b59f-146">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5b59f-146">-Location</span></span>
<span data-ttu-id="5b59f-147">Posizione di runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="5b59f-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="5b59f-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="5b59f-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="5b59f-149">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="5b59f-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b59f-150">-Name</span></span>
<span data-ttu-id="5b59f-151">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="5b59f-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5b59f-152">-NodeCount</span></span>
<span data-ttu-id="5b59f-153">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="5b59f-154">-NodeSize</span></span>
<span data-ttu-id="5b59f-155">Dimensioni del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="5b59f-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="5b59f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b59f-156">-ResourceGroupName</span></span>
<span data-ttu-id="5b59f-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b59f-157">The resource group name.</span></span>

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

### <span data-ttu-id="5b59f-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b59f-158">-ResourceId</span></span>
<span data-ttu-id="5b59f-159">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="5b59f-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5b59f-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="5b59f-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="5b59f-161">URI SAS del contenitore di Azure BLOB che contiene lo script di configurazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5b59f-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="5b59f-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="5b59f-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="5b59f-163">ID risorsa del runtime di integrazione ospitata autonomamente condiviso.</span><span class="sxs-lookup"><span data-stu-id="5b59f-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="5b59f-164">-Subnet</span><span class="sxs-lookup"><span data-stu-id="5b59f-164">-Subnet</span></span>
<span data-ttu-id="5b59f-165">Il nome della subnet in VNet.</span><span class="sxs-lookup"><span data-stu-id="5b59f-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="5b59f-166">-Digitare</span><span class="sxs-lookup"><span data-stu-id="5b59f-166">-Type</span></span>
<span data-ttu-id="5b59f-167">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="5b59f-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="5b59f-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="5b59f-168">-VNetId</span></span>
<span data-ttu-id="5b59f-169">ID della VNet in cui si unisce Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="5b59f-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="5b59f-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5b59f-170">-Confirm</span></span>
<span data-ttu-id="5b59f-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b59f-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b59f-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b59f-172">-WhatIf</span></span>
<span data-ttu-id="5b59f-173">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b59f-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5b59f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b59f-174">CommonParameters</span></span>
<span data-ttu-id="5b59f-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b59f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b59f-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b59f-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b59f-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b59f-177">INPUTS</span></span>

### <span data-ttu-id="5b59f-178">System. String</span><span class="sxs-lookup"><span data-stu-id="5b59f-178">System.String</span></span>

### <span data-ttu-id="5b59f-179">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b59f-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5b59f-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b59f-180">OUTPUTS</span></span>

### <span data-ttu-id="5b59f-181">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b59f-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5b59f-182">Note</span><span class="sxs-lookup"><span data-stu-id="5b59f-182">NOTES</span></span>

## <span data-ttu-id="5b59f-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b59f-183">RELATED LINKS</span></span>

[<span data-ttu-id="5b59f-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5b59f-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
