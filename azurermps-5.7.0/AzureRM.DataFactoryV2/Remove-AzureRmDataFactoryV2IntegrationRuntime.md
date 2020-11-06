---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508215"
---
# <span data-ttu-id="e282b-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e282b-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e282b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e282b-102">SYNOPSIS</span></span>
<span data-ttu-id="e282b-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e282b-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e282b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e282b-104">SYNTAX</span></span>

### <span data-ttu-id="e282b-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e282b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e282b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e282b-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e282b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e282b-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e282b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e282b-108">DESCRIPTION</span></span>
<span data-ttu-id="e282b-109">Il cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e282b-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="e282b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e282b-110">EXAMPLES</span></span>

### <span data-ttu-id="e282b-111">Esempio 1: rimuovere un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="e282b-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="e282b-112">Questo comando rimuove l'Integration runtime denominato ' test-reserved-IR ' dalla data factory denominata ' test-DF '.</span><span class="sxs-lookup"><span data-stu-id="e282b-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="e282b-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="e282b-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="e282b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e282b-114">PARAMETERS</span></span>

### <span data-ttu-id="e282b-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e282b-115">-DataFactoryName</span></span>
<span data-ttu-id="e282b-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="e282b-116">The data factory name.</span></span>

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

### <span data-ttu-id="e282b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e282b-117">-DefaultProfile</span></span>
<span data-ttu-id="e282b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e282b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e282b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e282b-119">-Force</span></span>
<span data-ttu-id="e282b-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e282b-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e282b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e282b-121">-InputObject</span></span>
<span data-ttu-id="e282b-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="e282b-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="e282b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e282b-123">-Name</span></span>
<span data-ttu-id="e282b-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e282b-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="e282b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e282b-125">-ResourceGroupName</span></span>
<span data-ttu-id="e282b-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e282b-126">The resource group name.</span></span>

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

### <span data-ttu-id="e282b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e282b-127">-ResourceId</span></span>
<span data-ttu-id="e282b-128">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="e282b-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e282b-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e282b-129">-Confirm</span></span>
<span data-ttu-id="e282b-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e282b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e282b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e282b-131">-WhatIf</span></span>
<span data-ttu-id="e282b-132">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e282b-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e282b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e282b-133">CommonParameters</span></span>
<span data-ttu-id="e282b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e282b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e282b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e282b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e282b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e282b-136">INPUTS</span></span>

### <span data-ttu-id="e282b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e282b-137">System.String</span></span>
<span data-ttu-id="e282b-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e282b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e282b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e282b-139">OUTPUTS</span></span>

### <span data-ttu-id="e282b-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="e282b-140">System.Object</span></span>

## <span data-ttu-id="e282b-141">Note</span><span class="sxs-lookup"><span data-stu-id="e282b-141">NOTES</span></span>
<span data-ttu-id="e282b-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="e282b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e282b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e282b-143">RELATED LINKS</span></span>

[<span data-ttu-id="e282b-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e282b-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="e282b-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e282b-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

