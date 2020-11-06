---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521704"
---
# <span data-ttu-id="3c511-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3c511-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3c511-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c511-102">SYNOPSIS</span></span>
<span data-ttu-id="3c511-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3c511-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c511-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c511-104">SYNTAX</span></span>

### <span data-ttu-id="3c511-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c511-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3c511-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c511-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3c511-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3c511-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="3c511-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c511-108">DESCRIPTION</span></span>
<span data-ttu-id="3c511-109">Il cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3c511-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="3c511-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c511-110">EXAMPLES</span></span>

### <span data-ttu-id="3c511-111">Esempio 1: rimuovere un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="3c511-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="3c511-112">Questo comando rimuove l'Integration runtime denominato ' test-reserved-IR ' dalla data factory denominata ' test-DF '.</span><span class="sxs-lookup"><span data-stu-id="3c511-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="3c511-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="3c511-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="3c511-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c511-114">PARAMETERS</span></span>

### <span data-ttu-id="3c511-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3c511-115">-DataFactoryName</span></span>
<span data-ttu-id="3c511-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="3c511-116">The data factory name.</span></span>

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

### <span data-ttu-id="3c511-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3c511-117">-Force</span></span>
<span data-ttu-id="3c511-118">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3c511-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3c511-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c511-119">-InputObject</span></span>
<span data-ttu-id="3c511-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="3c511-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="3c511-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c511-121">-Name</span></span>
<span data-ttu-id="3c511-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3c511-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="3c511-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c511-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c511-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c511-124">The resource group name.</span></span>

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

### <span data-ttu-id="3c511-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c511-125">-ResourceId</span></span>
<span data-ttu-id="3c511-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c511-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3c511-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c511-127">-Confirm</span></span>
<span data-ttu-id="3c511-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c511-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c511-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c511-129">-WhatIf</span></span>
<span data-ttu-id="3c511-130">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c511-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="3c511-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c511-131">INPUTS</span></span>

### <span data-ttu-id="3c511-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3c511-132">System.String</span></span>
<span data-ttu-id="3c511-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3c511-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3c511-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c511-134">OUTPUTS</span></span>

### <span data-ttu-id="3c511-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="3c511-135">System.Object</span></span>

## <span data-ttu-id="3c511-136">Note</span><span class="sxs-lookup"><span data-stu-id="3c511-136">NOTES</span></span>
<span data-ttu-id="3c511-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="3c511-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="3c511-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c511-138">RELATED LINKS</span></span>
[<span data-ttu-id="3c511-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3c511-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="3c511-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3c511-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

