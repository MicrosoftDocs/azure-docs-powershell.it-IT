---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 04e93db967a589c9dbcca4a88ed29d75f742ba7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674909"
---
# <span data-ttu-id="26304-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="26304-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="26304-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26304-102">SYNOPSIS</span></span>
<span data-ttu-id="26304-103">Arresta un runtime di integrazione dedicata gestito.</span><span class="sxs-lookup"><span data-stu-id="26304-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="26304-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26304-104">SYNTAX</span></span>

### <span data-ttu-id="26304-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26304-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26304-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="26304-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26304-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="26304-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26304-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26304-108">DESCRIPTION</span></span>
<span data-ttu-id="26304-109">Il cmdlet **Stop-AzDataFactoryV2IntegrationRuntime** arresta un runtime di Integration dedicato gestito in stato "Started", iniziato dal cmdlet Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="26304-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="26304-110">Le risorse vengono rilasciate e lo stato viene trasferito in "Stopped".</span><span class="sxs-lookup"><span data-stu-id="26304-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="26304-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26304-111">EXAMPLES</span></span>

### <span data-ttu-id="26304-112">Esempio 1: arrestare un runtime di integrazione gestita in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="26304-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="26304-113">Il runtime di Integration Managed "test-reserlved-IR" si trova in stato "iniziato".</span><span class="sxs-lookup"><span data-stu-id="26304-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="26304-114">Dopo aver eseguito Stop-AzDataFactoryV2IntegrationRuntime cmdlet, le risorse vengono rilasciate e lo stato viene trasferito su "Stopped".</span><span class="sxs-lookup"><span data-stu-id="26304-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="26304-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26304-115">PARAMETERS</span></span>

### <span data-ttu-id="26304-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="26304-116">-DataFactoryName</span></span>
<span data-ttu-id="26304-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="26304-117">The data factory name.</span></span>

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

### <span data-ttu-id="26304-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26304-118">-DefaultProfile</span></span>
<span data-ttu-id="26304-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26304-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26304-120">-Force</span><span class="sxs-lookup"><span data-stu-id="26304-120">-Force</span></span>
<span data-ttu-id="26304-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="26304-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="26304-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26304-122">-InputObject</span></span>
<span data-ttu-id="26304-123">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="26304-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="26304-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="26304-124">-Name</span></span>
<span data-ttu-id="26304-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="26304-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="26304-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26304-126">-ResourceGroupName</span></span>
<span data-ttu-id="26304-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26304-127">The resource group name.</span></span>

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

### <span data-ttu-id="26304-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26304-128">-ResourceId</span></span>
<span data-ttu-id="26304-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="26304-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="26304-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26304-130">-Confirm</span></span>
<span data-ttu-id="26304-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26304-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26304-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26304-132">-WhatIf</span></span>
<span data-ttu-id="26304-133">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26304-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="26304-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26304-134">CommonParameters</span></span>
<span data-ttu-id="26304-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26304-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26304-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26304-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26304-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26304-137">INPUTS</span></span>

### <span data-ttu-id="26304-138">System. String</span><span class="sxs-lookup"><span data-stu-id="26304-138">System.String</span></span>

### <span data-ttu-id="26304-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="26304-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="26304-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26304-140">OUTPUTS</span></span>

### <span data-ttu-id="26304-141">System. void</span><span class="sxs-lookup"><span data-stu-id="26304-141">System.Void</span></span>

## <span data-ttu-id="26304-142">Note</span><span class="sxs-lookup"><span data-stu-id="26304-142">NOTES</span></span>
<span data-ttu-id="26304-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="26304-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="26304-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26304-144">RELATED LINKS</span></span>

[<span data-ttu-id="26304-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="26304-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()