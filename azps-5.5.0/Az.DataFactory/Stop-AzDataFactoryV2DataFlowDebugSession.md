---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209826"
---
# <span data-ttu-id="a295d-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="a295d-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="a295d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a295d-102">SYNOPSIS</span></span>
<span data-ttu-id="a295d-103">Interrompe una sessione di debug del flusso di dati in Data factory di Azure</span><span class="sxs-lookup"><span data-stu-id="a295d-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="a295d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a295d-104">SYNTAX</span></span>

### <span data-ttu-id="a295d-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="a295d-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a295d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a295d-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a295d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a295d-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a295d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a295d-108">DESCRIPTION</span></span>
<span data-ttu-id="a295d-109">Questo comando interrompe la sessione di debug, in caso contrario viene automaticamente disattivata in base all'impostazione Time To Live della sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="a295d-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="a295d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a295d-110">EXAMPLES</span></span>

### <span data-ttu-id="a295d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a295d-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="a295d-112">Interrompe una sessione di debug del flusso di dati "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" nel data factory "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="a295d-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="a295d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a295d-113">PARAMETERS</span></span>

### <span data-ttu-id="a295d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a295d-114">-DataFactory</span></span>
<span data-ttu-id="a295d-115">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="a295d-115">The data factory object.</span></span>

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

### <span data-ttu-id="a295d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a295d-116">-DataFactoryName</span></span>
<span data-ttu-id="a295d-117">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="a295d-117">The data factory name.</span></span>

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

### <span data-ttu-id="a295d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a295d-118">-DefaultProfile</span></span>
<span data-ttu-id="a295d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a295d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a295d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a295d-120">-PassThru</span></span>
<span data-ttu-id="a295d-121">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="a295d-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="a295d-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a295d-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a295d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a295d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a295d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a295d-124">The resource group name.</span></span>

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

### <span data-ttu-id="a295d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a295d-125">-ResourceId</span></span>
<span data-ttu-id="a295d-126">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="a295d-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a295d-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="a295d-127">-SessionId</span></span>
<span data-ttu-id="a295d-128">ID sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="a295d-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="a295d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a295d-129">-Confirm</span></span>
<span data-ttu-id="a295d-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a295d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a295d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a295d-131">-WhatIf</span></span>
<span data-ttu-id="a295d-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a295d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a295d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a295d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a295d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a295d-134">CommonParameters</span></span>
<span data-ttu-id="a295d-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a295d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a295d-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a295d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a295d-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="a295d-137">INPUTS</span></span>

### <span data-ttu-id="a295d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a295d-138">System.String</span></span>

### <span data-ttu-id="a295d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a295d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a295d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a295d-140">OUTPUTS</span></span>

### <span data-ttu-id="a295d-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="a295d-141">System.Void</span></span>

### <span data-ttu-id="a295d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a295d-142">System.Boolean</span></span>

## <span data-ttu-id="a295d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="a295d-143">NOTES</span></span>
<span data-ttu-id="a295d-144">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="a295d-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a295d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a295d-145">RELATED LINKS</span></span>

[<span data-ttu-id="a295d-146">Start-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="a295d-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a295d-147">Get-AzDataSessionV2DataFlowSession</span><span class="sxs-lookup"><span data-stu-id="a295d-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="a295d-148">Add-AzDataSessionV2DataFlowSessionPackage</span><span class="sxs-lookup"><span data-stu-id="a295d-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="a295d-149">Invoke-AzDataSessionV2DataFlowSessionCommand</span><span class="sxs-lookup"><span data-stu-id="a295d-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)