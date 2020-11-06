---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce9ca0f1581bc995f9ea18b3b87169ed979dd92c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520645"
---
# <span data-ttu-id="246da-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="246da-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="246da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="246da-102">SYNOPSIS</span></span>
<span data-ttu-id="246da-103">Arresta un runtime di integrazione dedicata gestito.</span><span class="sxs-lookup"><span data-stu-id="246da-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="246da-104">SYNTAX</span></span>

### <span data-ttu-id="246da-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="246da-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="246da-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="246da-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="246da-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="246da-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246da-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="246da-108">DESCRIPTION</span></span>
<span data-ttu-id="246da-109">Il cmdlet **Stop-AzureRmDataFactoryV2IntegrationRuntime** arresta un runtime di Integration dedicato gestito in stato "Started", iniziato dal cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="246da-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="246da-110">Le risorse vengono rilasciate e lo stato viene trasferito in "Stopped".</span><span class="sxs-lookup"><span data-stu-id="246da-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="246da-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="246da-111">EXAMPLES</span></span>

### <span data-ttu-id="246da-112">Esempio 1: arrestare un runtime di integrazione gestita in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="246da-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="246da-113">Il runtime di Integration Managed "test-reserlved-IR" si trova in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="246da-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="246da-114">Dopo aver eseguito Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, le risorse vengono rilasciate e lo stato viene trasferito su "Stopped".</span><span class="sxs-lookup"><span data-stu-id="246da-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="246da-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="246da-115">PARAMETERS</span></span>

### <span data-ttu-id="246da-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="246da-116">-DataFactoryName</span></span>
<span data-ttu-id="246da-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="246da-117">The data factory name.</span></span>

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

### <span data-ttu-id="246da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246da-118">-DefaultProfile</span></span>
<span data-ttu-id="246da-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="246da-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="246da-120">-Force</span><span class="sxs-lookup"><span data-stu-id="246da-120">-Force</span></span>
<span data-ttu-id="246da-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="246da-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="246da-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="246da-122">-InputObject</span></span>
<span data-ttu-id="246da-123">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="246da-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="246da-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="246da-124">-Name</span></span>
<span data-ttu-id="246da-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="246da-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="246da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246da-126">-ResourceGroupName</span></span>
<span data-ttu-id="246da-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="246da-127">The resource group name.</span></span>

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

### <span data-ttu-id="246da-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="246da-128">-ResourceId</span></span>
<span data-ttu-id="246da-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="246da-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="246da-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="246da-130">-Confirm</span></span>
<span data-ttu-id="246da-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="246da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246da-132">-WhatIf</span></span>
<span data-ttu-id="246da-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="246da-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="246da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246da-134">CommonParameters</span></span>
<span data-ttu-id="246da-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246da-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246da-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246da-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="246da-137">INPUTS</span></span>

### <span data-ttu-id="246da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="246da-138">System.String</span></span>

### <span data-ttu-id="246da-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="246da-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="246da-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="246da-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="246da-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="246da-141">OUTPUTS</span></span>

### <span data-ttu-id="246da-142">System. void</span><span class="sxs-lookup"><span data-stu-id="246da-142">System.Void</span></span>

## <span data-ttu-id="246da-143">Note</span><span class="sxs-lookup"><span data-stu-id="246da-143">NOTES</span></span>
<span data-ttu-id="246da-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="246da-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="246da-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="246da-145">RELATED LINKS</span></span>

[<span data-ttu-id="246da-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="246da-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
