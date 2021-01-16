---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355039"
---
# <span data-ttu-id="546ce-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="546ce-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="546ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="546ce-102">SYNOPSIS</span></span>
<span data-ttu-id="546ce-103">Arresta un runtime di integrazione dedicata gestito.</span><span class="sxs-lookup"><span data-stu-id="546ce-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="546ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="546ce-104">SYNTAX</span></span>

### <span data-ttu-id="546ce-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="546ce-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="546ce-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="546ce-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="546ce-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="546ce-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="546ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="546ce-108">DESCRIPTION</span></span>
<span data-ttu-id="546ce-109">Il cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** arresta un runtime di Integration dedicato gestito in stato "Started", iniziato dal cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="546ce-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="546ce-110">Le risorse vengono rilasciate e lo stato viene trasferito in "Stopped".</span><span class="sxs-lookup"><span data-stu-id="546ce-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="546ce-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="546ce-111">EXAMPLES</span></span>

### <span data-ttu-id="546ce-112">Esempio 1: arrestare un runtime di integrazione gestita in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="546ce-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="546ce-113">Il runtime di Integration Managed "test-reserlved-IR" si trova in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="546ce-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="546ce-114">Dopo aver eseguito Stop-AzDataFactoryV2IntegrationRuntime cmdlet, le risorse vengono rilasciate e lo stato viene trasferito su "Stopped".</span><span class="sxs-lookup"><span data-stu-id="546ce-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="546ce-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="546ce-115">PARAMETERS</span></span>

### <span data-ttu-id="546ce-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="546ce-116">-DataFactoryName</span></span>
<span data-ttu-id="546ce-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="546ce-117">The data factory name.</span></span>

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

### <span data-ttu-id="546ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546ce-118">-DefaultProfile</span></span>
<span data-ttu-id="546ce-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="546ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="546ce-120">-Force</span><span class="sxs-lookup"><span data-stu-id="546ce-120">-Force</span></span>
<span data-ttu-id="546ce-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="546ce-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="546ce-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="546ce-122">-InputObject</span></span>
<span data-ttu-id="546ce-123">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="546ce-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="546ce-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="546ce-124">-Name</span></span>
<span data-ttu-id="546ce-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="546ce-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="546ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="546ce-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="546ce-127">The resource group name.</span></span>

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

### <span data-ttu-id="546ce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="546ce-128">-ResourceId</span></span>
<span data-ttu-id="546ce-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="546ce-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="546ce-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="546ce-130">-Confirm</span></span>
<span data-ttu-id="546ce-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="546ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="546ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546ce-132">-WhatIf</span></span>
<span data-ttu-id="546ce-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="546ce-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="546ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546ce-134">CommonParameters</span></span>
<span data-ttu-id="546ce-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546ce-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546ce-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546ce-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="546ce-137">INPUTS</span></span>

### <span data-ttu-id="546ce-138">System. String</span><span class="sxs-lookup"><span data-stu-id="546ce-138">System.String</span></span>

### <span data-ttu-id="546ce-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="546ce-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="546ce-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="546ce-140">OUTPUTS</span></span>

### <span data-ttu-id="546ce-141">System. void</span><span class="sxs-lookup"><span data-stu-id="546ce-141">System.Void</span></span>

## <span data-ttu-id="546ce-142">Note</span><span class="sxs-lookup"><span data-stu-id="546ce-142">NOTES</span></span>
<span data-ttu-id="546ce-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="546ce-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="546ce-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="546ce-144">RELATED LINKS</span></span>

[<span data-ttu-id="546ce-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="546ce-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
