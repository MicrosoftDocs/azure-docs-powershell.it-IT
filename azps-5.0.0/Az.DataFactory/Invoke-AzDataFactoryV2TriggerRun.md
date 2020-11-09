---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298458"
---
# <span data-ttu-id="f718b-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="f718b-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="f718b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f718b-102">SYNOPSIS</span></span>
 <span data-ttu-id="f718b-103">Richiama un'altra istanza di un'esecuzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="f718b-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="f718b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f718b-104">SYNTAX</span></span>

### <span data-ttu-id="f718b-105">ByFactoryNameByParameterFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f718b-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f718b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f718b-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f718b-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="f718b-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f718b-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f718b-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f718b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f718b-109">DESCRIPTION</span></span>
<span data-ttu-id="f718b-110">Il comando **Invoke-AzDataFactoryV2TriggerRun** avvia un'altra istanza di un trigger in esecuzione con un nuovo ID di esecuzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="f718b-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="f718b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f718b-111">EXAMPLES</span></span>

### <span data-ttu-id="f718b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f718b-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="f718b-113">Avvia un'altra istanza di un trigger eseguito con un nuovo ID di esecuzione del trigger, mantenendo lo stesso windowStartTime e windowEndTime dell'esecuzione del trigger originale.</span><span class="sxs-lookup"><span data-stu-id="f718b-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="f718b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f718b-114">PARAMETERS</span></span>

### <span data-ttu-id="f718b-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f718b-115">-DataFactory</span></span>
<span data-ttu-id="f718b-116">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f718b-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f718b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f718b-117">-DataFactoryName</span></span>
<span data-ttu-id="f718b-118">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="f718b-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f718b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f718b-119">-DefaultProfile</span></span>
<span data-ttu-id="f718b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f718b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f718b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f718b-121">-InputObject</span></span>
<span data-ttu-id="f718b-122">Informazioni sull'esecuzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="f718b-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f718b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f718b-123">-PassThru</span></span>
<span data-ttu-id="f718b-124">Se specificato, il cmdlet scrive vero in caso di esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f718b-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="f718b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f718b-125">-ResourceGroupName</span></span>
<span data-ttu-id="f718b-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f718b-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f718b-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="f718b-127">-TriggerName</span></span>
<span data-ttu-id="f718b-128">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="f718b-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f718b-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="f718b-129">-TriggerRunId</span></span>
<span data-ttu-id="f718b-130">ID esecuzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="f718b-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f718b-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f718b-131">-Confirm</span></span>
<span data-ttu-id="f718b-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f718b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f718b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f718b-133">-WhatIf</span></span>
<span data-ttu-id="f718b-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f718b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f718b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f718b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f718b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f718b-136">CommonParameters</span></span>
<span data-ttu-id="f718b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f718b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f718b-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f718b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f718b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f718b-139">INPUTS</span></span>

### <span data-ttu-id="f718b-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="f718b-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="f718b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f718b-141">System.String</span></span>

### <span data-ttu-id="f718b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f718b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f718b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f718b-143">OUTPUTS</span></span>

### <span data-ttu-id="f718b-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f718b-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="f718b-145">Note</span><span class="sxs-lookup"><span data-stu-id="f718b-145">NOTES</span></span>

## <span data-ttu-id="f718b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f718b-146">RELATED LINKS</span></span>
