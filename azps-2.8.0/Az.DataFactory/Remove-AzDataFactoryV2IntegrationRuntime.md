---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 9478c190d33608706006ff7fe792b4ee8f14b9d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674956"
---
# <span data-ttu-id="c9aaf-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9aaf-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c9aaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="c9aaf-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="c9aaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9aaf-104">SYNTAX</span></span>

### <span data-ttu-id="c9aaf-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9aaf-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9aaf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9aaf-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9aaf-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c9aaf-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9aaf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9aaf-108">DESCRIPTION</span></span>
<span data-ttu-id="c9aaf-109">Il cmdlet Remove-AzDataFactoryV2IntegrationRuntime rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="c9aaf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9aaf-110">EXAMPLES</span></span>

### <span data-ttu-id="c9aaf-111">Esempio 1: rimuovere un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="c9aaf-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="c9aaf-112">Questo comando rimuove l'Integration runtime denominato ' test-reserved-IR ' dalla data factory denominata ' test-DF '.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="c9aaf-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="c9aaf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9aaf-114">PARAMETERS</span></span>

### <span data-ttu-id="c9aaf-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c9aaf-115">-DataFactoryName</span></span>
<span data-ttu-id="c9aaf-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-116">The data factory name.</span></span>

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

### <span data-ttu-id="c9aaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9aaf-117">-DefaultProfile</span></span>
<span data-ttu-id="c9aaf-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9aaf-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c9aaf-119">-Force</span></span>
<span data-ttu-id="c9aaf-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c9aaf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9aaf-121">-InputObject</span></span>
<span data-ttu-id="c9aaf-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="c9aaf-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c9aaf-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="c9aaf-124">Nome della factory di dati collegati.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="c9aaf-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9aaf-125">-Name</span></span>
<span data-ttu-id="c9aaf-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="c9aaf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9aaf-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9aaf-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-128">The resource group name.</span></span>

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

### <span data-ttu-id="c9aaf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9aaf-129">-ResourceId</span></span>
<span data-ttu-id="c9aaf-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c9aaf-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9aaf-131">-Confirm</span></span>
<span data-ttu-id="c9aaf-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9aaf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9aaf-133">-WhatIf</span></span>
<span data-ttu-id="c9aaf-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c9aaf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9aaf-135">CommonParameters</span></span>
<span data-ttu-id="c9aaf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9aaf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9aaf-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9aaf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9aaf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9aaf-138">INPUTS</span></span>

### <span data-ttu-id="c9aaf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c9aaf-139">System.String</span></span>

### <span data-ttu-id="c9aaf-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9aaf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c9aaf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9aaf-141">OUTPUTS</span></span>

### <span data-ttu-id="c9aaf-142">System. void</span><span class="sxs-lookup"><span data-stu-id="c9aaf-142">System.Void</span></span>

## <span data-ttu-id="c9aaf-143">Note</span><span class="sxs-lookup"><span data-stu-id="c9aaf-143">NOTES</span></span>
<span data-ttu-id="c9aaf-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="c9aaf-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c9aaf-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9aaf-145">RELATED LINKS</span></span>

[<span data-ttu-id="c9aaf-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9aaf-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="c9aaf-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9aaf-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

