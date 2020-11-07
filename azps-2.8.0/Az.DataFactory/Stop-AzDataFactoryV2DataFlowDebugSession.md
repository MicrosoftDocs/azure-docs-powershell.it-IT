---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: def0ff5b525f4ced0ac1510fdc65b1dfd746cc6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674912"
---
# <span data-ttu-id="d3a87-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3a87-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="d3a87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3a87-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a87-103">Interrompe una sessione di debug del flusso di dati in Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="d3a87-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="d3a87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3a87-104">SYNTAX</span></span>

### <span data-ttu-id="d3a87-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3a87-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3a87-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3a87-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a87-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3a87-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a87-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3a87-108">DESCRIPTION</span></span>
<span data-ttu-id="d3a87-109">Questo comando interrompe la sessione di debug, se non quindi la sessione verrà disattivata automaticamente in base all'impostazione del tempo di esecuzione della sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="d3a87-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="d3a87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3a87-110">EXAMPLES</span></span>

### <span data-ttu-id="d3a87-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3a87-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="d3a87-112">Interrompe una sessione di debug del flusso di dati "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" in Factory di dati "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="d3a87-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="d3a87-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3a87-113">PARAMETERS</span></span>

### <span data-ttu-id="d3a87-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d3a87-114">-DataFactory</span></span>
<span data-ttu-id="d3a87-115">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d3a87-115">The data factory object.</span></span>

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

### <span data-ttu-id="d3a87-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d3a87-116">-DataFactoryName</span></span>
<span data-ttu-id="d3a87-117">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="d3a87-117">The data factory name.</span></span>

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

### <span data-ttu-id="d3a87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a87-118">-DefaultProfile</span></span>
<span data-ttu-id="d3a87-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a87-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a87-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3a87-120">-PassThru</span></span>
<span data-ttu-id="d3a87-121">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="d3a87-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="d3a87-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d3a87-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d3a87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a87-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3a87-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3a87-124">The resource group name.</span></span>

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

### <span data-ttu-id="d3a87-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3a87-125">-ResourceId</span></span>
<span data-ttu-id="d3a87-126">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a87-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a87-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="d3a87-127">-SessionId</span></span>
<span data-ttu-id="d3a87-128">ID sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="d3a87-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a87-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3a87-129">-Confirm</span></span>
<span data-ttu-id="d3a87-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a87-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a87-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a87-131">-WhatIf</span></span>
<span data-ttu-id="d3a87-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3a87-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a87-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3a87-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a87-134">CommonParameters</span></span>
<span data-ttu-id="d3a87-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a87-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3a87-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a87-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3a87-137">INPUTS</span></span>

### <span data-ttu-id="d3a87-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d3a87-138">System.String</span></span>

### <span data-ttu-id="d3a87-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d3a87-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d3a87-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3a87-140">OUTPUTS</span></span>

### <span data-ttu-id="d3a87-141">System. void</span><span class="sxs-lookup"><span data-stu-id="d3a87-141">System.Void</span></span>

### <span data-ttu-id="d3a87-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3a87-142">System.Boolean</span></span>

## <span data-ttu-id="d3a87-143">Note</span><span class="sxs-lookup"><span data-stu-id="d3a87-143">NOTES</span></span>
<span data-ttu-id="d3a87-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="d3a87-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3a87-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3a87-145">RELATED LINKS</span></span>

[<span data-ttu-id="d3a87-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3a87-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d3a87-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3a87-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d3a87-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="d3a87-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="d3a87-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="d3a87-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)