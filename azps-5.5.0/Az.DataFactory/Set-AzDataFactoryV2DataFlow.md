---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 44439d49fc89f00abaef904e80112d076121890f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407438"
---
# <span data-ttu-id="da7ed-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="da7ed-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="da7ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="da7ed-103">Crea un flusso di dati in Data factory.</span><span class="sxs-lookup"><span data-stu-id="da7ed-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="da7ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da7ed-104">SYNTAX</span></span>

### <span data-ttu-id="da7ed-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="da7ed-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da7ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="da7ed-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7ed-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da7ed-107">DESCRIPTION</span></span>
<span data-ttu-id="da7ed-108">Il cmdlet Set-AzDataFactoryV2DataFlow crea un flusso di dati o aggiorna un flusso di dati esistente in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="da7ed-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="da7ed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da7ed-109">EXAMPLES</span></span>

### <span data-ttu-id="da7ed-110">Esempio 1: Creare un flusso di dati</span><span class="sxs-lookup"><span data-stu-id="da7ed-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="da7ed-111">Questo comando crea un flusso di dati denominatoDemo1 nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="da7ed-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="da7ed-112">Il comando basa il flusso di dati sulle informazioni TaxiDemo1.jssu file.</span><span class="sxs-lookup"><span data-stu-id="da7ed-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="da7ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da7ed-113">PARAMETERS</span></span>

### <span data-ttu-id="da7ed-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="da7ed-114">-DataFactoryName</span></span>
<span data-ttu-id="da7ed-115">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="da7ed-115">The data factory name.</span></span>

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

### <span data-ttu-id="da7ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7ed-116">-DefaultProfile</span></span>
<span data-ttu-id="da7ed-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da7ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da7ed-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="da7ed-118">-DefinitionFile</span></span>
<span data-ttu-id="da7ed-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="da7ed-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da7ed-120">-Force</span><span class="sxs-lookup"><span data-stu-id="da7ed-120">-Force</span></span>
<span data-ttu-id="da7ed-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="da7ed-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="da7ed-122">-Name</span><span class="sxs-lookup"><span data-stu-id="da7ed-122">-Name</span></span>
<span data-ttu-id="da7ed-123">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="da7ed-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da7ed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7ed-124">-ResourceGroupName</span></span>
<span data-ttu-id="da7ed-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da7ed-125">The resource group name.</span></span>

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

### <span data-ttu-id="da7ed-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da7ed-126">-ResourceId</span></span>
<span data-ttu-id="da7ed-127">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="da7ed-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="da7ed-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da7ed-128">-Confirm</span></span>
<span data-ttu-id="da7ed-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7ed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7ed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7ed-130">-WhatIf</span></span>
<span data-ttu-id="da7ed-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da7ed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da7ed-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da7ed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7ed-133">CommonParameters</span></span>
<span data-ttu-id="da7ed-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7ed-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da7ed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7ed-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="da7ed-136">INPUTS</span></span>

### <span data-ttu-id="da7ed-137">System.String</span><span class="sxs-lookup"><span data-stu-id="da7ed-137">System.String</span></span>

## <span data-ttu-id="da7ed-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da7ed-138">OUTPUTS</span></span>

### <span data-ttu-id="da7ed-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="da7ed-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="da7ed-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="da7ed-140">NOTES</span></span>
<span data-ttu-id="da7ed-141">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="da7ed-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="da7ed-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da7ed-142">RELATED LINKS</span></span>


