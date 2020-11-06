---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: bc16145569fd46b80e6d7a5afc1755f36346fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508212"
---
# <span data-ttu-id="24383-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="24383-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="24383-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24383-102">SYNOPSIS</span></span>
<span data-ttu-id="24383-103">Rimuovere un nodo con il nome indicato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="24383-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24383-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24383-104">SYNTAX</span></span>

### <span data-ttu-id="24383-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24383-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24383-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24383-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24383-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="24383-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24383-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24383-108">DESCRIPTION</span></span>
<span data-ttu-id="24383-109">Il cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntimeNode rimuove un nodo in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="24383-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="24383-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24383-110">EXAMPLES</span></span>

### <span data-ttu-id="24383-111">Esempio 1: rimuovere un nodo da un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="24383-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="24383-112">Questo comando rimuove un nodo denominato "Node_1" nel runtime di integrazione denominato "test-SelfHost-IR" nell'abbonamento per il gruppo di risorse denominato "RG-test-dfv2" e data factory denominata "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="24383-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="24383-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24383-113">PARAMETERS</span></span>

### <span data-ttu-id="24383-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="24383-114">-DataFactoryName</span></span>
<span data-ttu-id="24383-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="24383-115">The data factory name.</span></span>

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

### <span data-ttu-id="24383-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24383-116">-DefaultProfile</span></span>
<span data-ttu-id="24383-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24383-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24383-118">-Force</span><span class="sxs-lookup"><span data-stu-id="24383-118">-Force</span></span>
<span data-ttu-id="24383-119">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="24383-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="24383-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24383-120">-InputObject</span></span>
<span data-ttu-id="24383-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="24383-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="24383-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="24383-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="24383-123">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="24383-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="24383-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="24383-124">-NodeName</span></span>
<span data-ttu-id="24383-125">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="24383-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="24383-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24383-126">-ResourceGroupName</span></span>
<span data-ttu-id="24383-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24383-127">The resource group name.</span></span>

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

### <span data-ttu-id="24383-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24383-128">-ResourceId</span></span>
<span data-ttu-id="24383-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="24383-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24383-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24383-130">-Confirm</span></span>
<span data-ttu-id="24383-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24383-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24383-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24383-132">-WhatIf</span></span>
<span data-ttu-id="24383-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24383-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="24383-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24383-134">CommonParameters</span></span>
<span data-ttu-id="24383-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24383-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24383-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24383-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24383-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24383-137">INPUTS</span></span>

### <span data-ttu-id="24383-138">System. String</span><span class="sxs-lookup"><span data-stu-id="24383-138">System.String</span></span>
<span data-ttu-id="24383-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="24383-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="24383-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24383-140">OUTPUTS</span></span>

### <span data-ttu-id="24383-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="24383-141">System.Object</span></span>

## <span data-ttu-id="24383-142">Note</span><span class="sxs-lookup"><span data-stu-id="24383-142">NOTES</span></span>

## <span data-ttu-id="24383-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24383-143">RELATED LINKS</span></span>

