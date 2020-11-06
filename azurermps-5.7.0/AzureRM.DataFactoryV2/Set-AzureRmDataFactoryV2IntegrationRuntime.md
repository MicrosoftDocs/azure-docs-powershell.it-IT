---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514440"
---
# <span data-ttu-id="9db47-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9db47-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="9db47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9db47-102">SYNOPSIS</span></span>
<span data-ttu-id="9db47-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9db47-104">SYNTAX</span></span>

### <span data-ttu-id="9db47-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9db47-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9db47-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9db47-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9db47-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9db47-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db47-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9db47-108">DESCRIPTION</span></span>
<span data-ttu-id="9db47-109">Il cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="9db47-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="9db47-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9db47-110">EXAMPLES</span></span>

### <span data-ttu-id="9db47-111">Esempio 1: aggiornare la descrizione del runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="9db47-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="9db47-112">Il cmdlet aggiorna la descrizione di Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="9db47-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9db47-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9db47-113">PARAMETERS</span></span>

### <span data-ttu-id="9db47-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="9db47-114">-AuthKey</span></span>
<span data-ttu-id="9db47-115">Chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="9db47-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="9db47-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="9db47-117">Credenziali di amministratore del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="9db47-118">-CatalogPricingTier</span></span>
<span data-ttu-id="9db47-119">Livello di prezzo del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9db47-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="9db47-121">Endpoint del server di database del catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9db47-122">-DataFactoryName</span></span>
<span data-ttu-id="9db47-123">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="9db47-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db47-124">-DefaultProfile</span></span>
<span data-ttu-id="9db47-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9db47-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9db47-126">-Description</span></span>
<span data-ttu-id="9db47-127">Descrizione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-128">-Edition</span><span class="sxs-lookup"><span data-stu-id="9db47-128">-Edition</span></span>
<span data-ttu-id="9db47-129">L'Edition for SSIS Integration Runtime che potrebbe essere standard o Enterprise, default è standard se non è specificato.</span><span class="sxs-lookup"><span data-stu-id="9db47-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9db47-130">-Force</span></span>
<span data-ttu-id="9db47-131">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9db47-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9db47-132">-InputObject</span></span>
<span data-ttu-id="9db47-133">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="9db47-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9db47-134">-LicenseType</span></span>
<span data-ttu-id="9db47-135">Tipo di licenza che si desidera selezionare per l'IR SSIS.</span><span class="sxs-lookup"><span data-stu-id="9db47-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="9db47-136">Esistono due tipi: LicenseIncluded o BasePrice.</span><span class="sxs-lookup"><span data-stu-id="9db47-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="9db47-137">Se si è qualificati per i prezzi di Azure Hybrid use benefit (AHUB), selezionare BasePrice.</span><span class="sxs-lookup"><span data-stu-id="9db47-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="9db47-138">In caso contrario, seleziona LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="9db47-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-139">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9db47-139">-Location</span></span>
<span data-ttu-id="9db47-140">Posizione di runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="9db47-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="9db47-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="9db47-142">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="9db47-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="9db47-143">-Name</span></span>
<span data-ttu-id="9db47-144">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9db47-145">-NodeCount</span></span>
<span data-ttu-id="9db47-146">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="9db47-147">-NodeSize</span></span>
<span data-ttu-id="9db47-148">Dimensioni del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="9db47-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db47-149">-ResourceGroupName</span></span>
<span data-ttu-id="9db47-150">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9db47-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9db47-151">-ResourceId</span></span>
<span data-ttu-id="9db47-152">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="9db47-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="9db47-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="9db47-154">URI SAS del contenitore di Azure BLOB che contiene lo script di configurazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9db47-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="9db47-155">-Subnet</span></span>
<span data-ttu-id="9db47-156">Il nome della subnet in VNet.</span><span class="sxs-lookup"><span data-stu-id="9db47-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-157">-Digitare</span><span class="sxs-lookup"><span data-stu-id="9db47-157">-Type</span></span>
<span data-ttu-id="9db47-158">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9db47-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="9db47-159">-VNetId</span></span>
<span data-ttu-id="9db47-160">ID della VNet in cui si unisce Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="9db47-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db47-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9db47-161">-Confirm</span></span>
<span data-ttu-id="9db47-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9db47-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db47-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db47-163">-WhatIf</span></span>
<span data-ttu-id="9db47-164">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9db47-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9db47-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db47-165">CommonParameters</span></span>
<span data-ttu-id="9db47-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db47-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db47-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db47-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db47-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9db47-168">INPUTS</span></span>

### <span data-ttu-id="9db47-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9db47-169">System.String</span></span>
<span data-ttu-id="9db47-170">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9db47-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9db47-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9db47-171">OUTPUTS</span></span>

### <span data-ttu-id="9db47-172">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9db47-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9db47-173">Note</span><span class="sxs-lookup"><span data-stu-id="9db47-173">NOTES</span></span>

## <span data-ttu-id="9db47-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9db47-174">RELATED LINKS</span></span>

[<span data-ttu-id="9db47-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9db47-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
