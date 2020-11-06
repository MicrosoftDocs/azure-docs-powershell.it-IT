---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520535"
---
# <span data-ttu-id="b3530-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b3530-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="b3530-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3530-102">SYNOPSIS</span></span>
<span data-ttu-id="b3530-103">Rimuovere un nodo con il nome indicato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b3530-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3530-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3530-104">SYNTAX</span></span>

### <span data-ttu-id="b3530-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3530-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="b3530-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3530-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="b3530-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b3530-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b3530-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3530-108">DESCRIPTION</span></span>
<span data-ttu-id="b3530-109">Il cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntimeNode rimuove un nodo in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b3530-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="b3530-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3530-110">EXAMPLES</span></span>

### <span data-ttu-id="b3530-111">Esempio 1: rimuovere un nodo da un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="b3530-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="b3530-112">Questo comando rimuove un nodo denominato "Node_1" nel runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominata "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="b3530-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="b3530-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3530-113">PARAMETERS</span></span>

### <span data-ttu-id="b3530-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3530-114">-Confirm</span></span>
<span data-ttu-id="b3530-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3530-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3530-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b3530-116">-DataFactoryName</span></span>
<span data-ttu-id="b3530-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="b3530-117">The data factory name.</span></span>

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

### <span data-ttu-id="b3530-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b3530-118">-Force</span></span>
<span data-ttu-id="b3530-119">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b3530-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b3530-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3530-120">-InputObject</span></span>
<span data-ttu-id="b3530-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b3530-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="b3530-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b3530-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b3530-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b3530-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3530-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="b3530-124">-NodeName</span></span>
<span data-ttu-id="b3530-125">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b3530-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b3530-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3530-126">-ResourceGroupName</span></span>
<span data-ttu-id="b3530-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3530-127">The resource group name.</span></span>

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

### <span data-ttu-id="b3530-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3530-128">-ResourceId</span></span>
<span data-ttu-id="b3530-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3530-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b3530-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3530-130">-WhatIf</span></span>
<span data-ttu-id="b3530-131">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3530-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="b3530-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3530-132">INPUTS</span></span>

### <span data-ttu-id="b3530-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b3530-133">System.String</span></span>
<span data-ttu-id="b3530-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b3530-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="b3530-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3530-135">OUTPUTS</span></span>

### <span data-ttu-id="b3530-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="b3530-136">System.Object</span></span>

## <span data-ttu-id="b3530-137">Note</span><span class="sxs-lookup"><span data-stu-id="b3530-137">NOTES</span></span>

## <span data-ttu-id="b3530-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3530-138">RELATED LINKS</span></span>

