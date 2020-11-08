---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: bb80289688688509ee4dfced17c94449cf4fd972
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192545"
---
# <span data-ttu-id="c0435-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="c0435-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="c0435-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0435-102">SYNOPSIS</span></span>
<span data-ttu-id="c0435-103">Rimuovere un nodo con il nome indicato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c0435-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="c0435-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0435-104">SYNTAX</span></span>

### <span data-ttu-id="c0435-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0435-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0435-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0435-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0435-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c0435-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0435-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0435-108">DESCRIPTION</span></span>
<span data-ttu-id="c0435-109">Il cmdlet Remove-AzDataFactoryV2IntegrationRuntimeNode rimuove un nodo in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c0435-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="c0435-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0435-110">EXAMPLES</span></span>

### <span data-ttu-id="c0435-111">Esempio 1: rimuovere un nodo da un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="c0435-111">Example 1: Remove a node from an integration runtime</span></span>

<span data-ttu-id="c0435-112">Rimuovere un nodo con il nome indicato in un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c0435-112">Remove a node with the given name on an integration runtime.</span></span> <span data-ttu-id="c0435-113">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c0435-113">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzDataFactoryV2IntegrationRuntimeNode -DataFactoryName 'test-df-eu2' -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1' -ResourceGroupName 'rg-test-dfv2'
```

## <span data-ttu-id="c0435-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0435-114">PARAMETERS</span></span>

### <span data-ttu-id="c0435-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c0435-115">-DataFactoryName</span></span>
<span data-ttu-id="c0435-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="c0435-116">The data factory name.</span></span>

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

### <span data-ttu-id="c0435-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0435-117">-DefaultProfile</span></span>
<span data-ttu-id="c0435-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0435-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0435-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c0435-119">-Force</span></span>
<span data-ttu-id="c0435-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c0435-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c0435-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0435-121">-InputObject</span></span>
<span data-ttu-id="c0435-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="c0435-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="c0435-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c0435-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c0435-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c0435-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0435-125">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c0435-125">-NodeName</span></span>
<span data-ttu-id="c0435-126">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="c0435-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0435-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0435-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0435-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c0435-128">The resource group name.</span></span>

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

### <span data-ttu-id="c0435-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0435-129">-ResourceId</span></span>
<span data-ttu-id="c0435-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="c0435-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c0435-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0435-131">-Confirm</span></span>
<span data-ttu-id="c0435-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0435-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0435-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0435-133">-WhatIf</span></span>
<span data-ttu-id="c0435-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0435-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c0435-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0435-135">CommonParameters</span></span>
<span data-ttu-id="c0435-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0435-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0435-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0435-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0435-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0435-138">INPUTS</span></span>

### <span data-ttu-id="c0435-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0435-139">System.String</span></span>

### <span data-ttu-id="c0435-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c0435-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c0435-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0435-141">OUTPUTS</span></span>

### <span data-ttu-id="c0435-142">System. void</span><span class="sxs-lookup"><span data-stu-id="c0435-142">System.Void</span></span>

## <span data-ttu-id="c0435-143">Note</span><span class="sxs-lookup"><span data-stu-id="c0435-143">NOTES</span></span>

## <span data-ttu-id="c0435-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0435-144">RELATED LINKS</span></span>