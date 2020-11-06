---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 181d63a41853105b21826353fabfca83cddf1bd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522144"
---
# <span data-ttu-id="97ed8-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="97ed8-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="97ed8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="97ed8-103">Arresta un runtime di integrazione dedicata gestito.</span><span class="sxs-lookup"><span data-stu-id="97ed8-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97ed8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97ed8-104">SYNTAX</span></span>

### <span data-ttu-id="97ed8-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97ed8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="97ed8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="97ed8-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="97ed8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="97ed8-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="97ed8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97ed8-108">DESCRIPTION</span></span>
<span data-ttu-id="97ed8-109">Il cmdlet **Stop-AzureRmDataFactoryV2IntegrationRuntime** arresta un runtime di Integration dedicato gestito in stato "Started", iniziato dal cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="97ed8-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="97ed8-110">Le risorse vengono rilasciate e lo stato viene trasferito in "Stopped".</span><span class="sxs-lookup"><span data-stu-id="97ed8-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="97ed8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97ed8-111">EXAMPLES</span></span>

### <span data-ttu-id="97ed8-112">Esempio 1: arrestare un runtime di integrazione gestita in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="97ed8-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="97ed8-113">Il runtime di Integration Managed "test-reserlved-IR" si trova in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="97ed8-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="97ed8-114">Dopo aver eseguito Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, le risorse vengono rilasciate e lo stato viene trasferito su "Stopped".</span><span class="sxs-lookup"><span data-stu-id="97ed8-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="97ed8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97ed8-115">PARAMETERS</span></span>

### <span data-ttu-id="97ed8-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97ed8-116">-Confirm</span></span>
<span data-ttu-id="97ed8-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ed8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ed8-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="97ed8-118">-DataFactoryName</span></span>
<span data-ttu-id="97ed8-119">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="97ed8-119">The data factory name.</span></span>

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

### <span data-ttu-id="97ed8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="97ed8-120">-Force</span></span>
<span data-ttu-id="97ed8-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="97ed8-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="97ed8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97ed8-122">-InputObject</span></span>
<span data-ttu-id="97ed8-123">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="97ed8-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="97ed8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="97ed8-124">-Name</span></span>
<span data-ttu-id="97ed8-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="97ed8-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="97ed8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ed8-126">-ResourceGroupName</span></span>
<span data-ttu-id="97ed8-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97ed8-127">The resource group name.</span></span>

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

### <span data-ttu-id="97ed8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97ed8-128">-ResourceId</span></span>
<span data-ttu-id="97ed8-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="97ed8-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="97ed8-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97ed8-130">-Confirm</span></span>
<span data-ttu-id="97ed8-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ed8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97ed8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97ed8-132">-WhatIf</span></span>
<span data-ttu-id="97ed8-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97ed8-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="97ed8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ed8-134">CommonParameters</span></span>
<span data-ttu-id="97ed8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ed8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ed8-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ed8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ed8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97ed8-137">INPUTS</span></span>

### <span data-ttu-id="97ed8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="97ed8-138">System.String</span></span>
<span data-ttu-id="97ed8-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="97ed8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="97ed8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97ed8-140">OUTPUTS</span></span>

### <span data-ttu-id="97ed8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97ed8-141">System.Boolean</span></span>

## <span data-ttu-id="97ed8-142">Note</span><span class="sxs-lookup"><span data-stu-id="97ed8-142">NOTES</span></span>
<span data-ttu-id="97ed8-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="97ed8-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="97ed8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97ed8-144">RELATED LINKS</span></span>
[<span data-ttu-id="97ed8-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="97ed8-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
