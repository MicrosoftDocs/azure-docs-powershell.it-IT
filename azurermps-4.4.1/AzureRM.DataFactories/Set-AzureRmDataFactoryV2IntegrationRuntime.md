---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688337"
---
# <span data-ttu-id="025d8-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="025d8-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="025d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="025d8-102">SYNOPSIS</span></span>
<span data-ttu-id="025d8-103">Aggiorna un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="025d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="025d8-104">SYNTAX</span></span>

### <span data-ttu-id="025d8-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="025d8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="025d8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="025d8-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="025d8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="025d8-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025d8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="025d8-108">DESCRIPTION</span></span>
<span data-ttu-id="025d8-109">Il cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime aggiorna un runtime di integrazione con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="025d8-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="025d8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="025d8-110">EXAMPLES</span></span>

### <span data-ttu-id="025d8-111">Esempio 1: aggiornare la descrizione del runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="025d8-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="025d8-112">Il cmdlet aggiorna la descrizione di Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="025d8-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="025d8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="025d8-113">PARAMETERS</span></span>

### <span data-ttu-id="025d8-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="025d8-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="025d8-115">Credenziali di amministratore del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="025d8-116">-CatalogPricingTier</span></span>
<span data-ttu-id="025d8-117">Livello di prezzo del database catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="025d8-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="025d8-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="025d8-119">Endpoint del server di database del catalogo del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="025d8-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="025d8-120">-Confirm</span></span>
<span data-ttu-id="025d8-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025d8-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="025d8-122">-DataFactoryName</span></span>
<span data-ttu-id="025d8-123">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="025d8-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="025d8-124">-Description</span></span>
<span data-ttu-id="025d8-125">Descrizione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="025d8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="025d8-126">-Force</span></span>
<span data-ttu-id="025d8-127">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="025d8-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="025d8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="025d8-128">-InputObject</span></span>
<span data-ttu-id="025d8-129">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="025d8-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="025d8-130">-Location</span></span>
<span data-ttu-id="025d8-131">Posizione di runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="025d8-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="025d8-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="025d8-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="025d8-133">Numero massimo di esecuzioni parallele per nodo per un runtime di integrazione dedicato gestito.</span><span class="sxs-lookup"><span data-stu-id="025d8-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="025d8-134">-Name</span></span>
<span data-ttu-id="025d8-135">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="025d8-136">-NodeCount</span></span>
<span data-ttu-id="025d8-137">Numero di nodi di destinazione del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="025d8-138">-NodeSize</span></span>
<span data-ttu-id="025d8-139">Dimensioni del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="025d8-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="025d8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025d8-140">-ResourceGroupName</span></span>
<span data-ttu-id="025d8-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="025d8-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="025d8-142">-ResourceId</span></span>
<span data-ttu-id="025d8-143">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="025d8-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-144">-Subnet</span><span class="sxs-lookup"><span data-stu-id="025d8-144">-Subnet</span></span>
<span data-ttu-id="025d8-145">Il nome della subnet in VNet.</span><span class="sxs-lookup"><span data-stu-id="025d8-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025d8-146">-Digitare</span><span class="sxs-lookup"><span data-stu-id="025d8-146">-Type</span></span>
<span data-ttu-id="025d8-147">Tipo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="025d8-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="025d8-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="025d8-148">-VNetId</span></span>
<span data-ttu-id="025d8-149">ID della VNet in cui si unisce Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="025d8-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="025d8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025d8-150">-WhatIf</span></span>
<span data-ttu-id="025d8-151">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="025d8-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="025d8-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025d8-152">-DefaultProfile</span></span>
<span data-ttu-id="025d8-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="025d8-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="025d8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025d8-154">CommonParameters</span></span>
<span data-ttu-id="025d8-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025d8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025d8-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025d8-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025d8-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="025d8-157">INPUTS</span></span>

### <span data-ttu-id="025d8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="025d8-158">System.String</span></span>
<span data-ttu-id="025d8-159">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="025d8-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="025d8-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="025d8-160">OUTPUTS</span></span>

### <span data-ttu-id="025d8-161">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="025d8-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="025d8-162">Note</span><span class="sxs-lookup"><span data-stu-id="025d8-162">NOTES</span></span>

## <span data-ttu-id="025d8-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="025d8-163">RELATED LINKS</span></span>

[<span data-ttu-id="025d8-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="025d8-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
