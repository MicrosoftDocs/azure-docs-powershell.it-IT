---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298338"
---
# <span data-ttu-id="cf038-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf038-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="cf038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf038-102">SYNOPSIS</span></span>
<span data-ttu-id="cf038-103">Rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cf038-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="cf038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf038-104">SYNTAX</span></span>

### <span data-ttu-id="cf038-105">ByIntegrationRuntimeName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf038-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf038-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf038-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf038-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cf038-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf038-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf038-108">DESCRIPTION</span></span>
<span data-ttu-id="cf038-109">Il cmdlet Remove-AzDataFactoryV2IntegrationRuntime rimuove un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cf038-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="cf038-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf038-110">EXAMPLES</span></span>

### <span data-ttu-id="cf038-111">Esempio 1: rimuovere un runtime di integrazione</span><span class="sxs-lookup"><span data-stu-id="cf038-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="cf038-112">Questo comando rimuove l'Integration runtime denominato ' test-reserved-IR ' dalla data factory denominata ' test-DF '.</span><span class="sxs-lookup"><span data-stu-id="cf038-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="cf038-113">Questo comando restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="cf038-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="cf038-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf038-114">PARAMETERS</span></span>

### <span data-ttu-id="cf038-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cf038-115">-DataFactoryName</span></span>
<span data-ttu-id="cf038-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="cf038-116">The data factory name.</span></span>

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

### <span data-ttu-id="cf038-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf038-117">-DefaultProfile</span></span>
<span data-ttu-id="cf038-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf038-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf038-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cf038-119">-Force</span></span>
<span data-ttu-id="cf038-120">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cf038-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cf038-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf038-121">-InputObject</span></span>
<span data-ttu-id="cf038-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="cf038-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="cf038-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cf038-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="cf038-124">Nome della factory di dati collegati.</span><span class="sxs-lookup"><span data-stu-id="cf038-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="cf038-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf038-125">-Name</span></span>
<span data-ttu-id="cf038-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="cf038-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="cf038-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf038-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf038-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf038-128">The resource group name.</span></span>

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

### <span data-ttu-id="cf038-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf038-129">-ResourceId</span></span>
<span data-ttu-id="cf038-130">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="cf038-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cf038-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf038-131">-Confirm</span></span>
<span data-ttu-id="cf038-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf038-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf038-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf038-133">-WhatIf</span></span>
<span data-ttu-id="cf038-134">Mostra cosa succede se il cmdlet viene eseguito, ma il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf038-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cf038-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf038-135">CommonParameters</span></span>
<span data-ttu-id="cf038-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf038-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf038-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf038-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf038-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf038-138">INPUTS</span></span>

### <span data-ttu-id="cf038-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cf038-139">System.String</span></span>

### <span data-ttu-id="cf038-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf038-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="cf038-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf038-141">OUTPUTS</span></span>

### <span data-ttu-id="cf038-142">System. void</span><span class="sxs-lookup"><span data-stu-id="cf038-142">System.Void</span></span>

## <span data-ttu-id="cf038-143">Note</span><span class="sxs-lookup"><span data-stu-id="cf038-143">NOTES</span></span>
<span data-ttu-id="cf038-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory, copy, Activities, Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="cf038-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="cf038-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf038-145">RELATED LINKS</span></span>

[<span data-ttu-id="cf038-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf038-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="cf038-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf038-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

