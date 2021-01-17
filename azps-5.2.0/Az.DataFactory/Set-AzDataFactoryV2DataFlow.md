---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357755"
---
# <span data-ttu-id="54437-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="54437-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="54437-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54437-102">SYNOPSIS</span></span>
<span data-ttu-id="54437-103">Crea un flusso di dati in data factory.</span><span class="sxs-lookup"><span data-stu-id="54437-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="54437-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54437-104">SYNTAX</span></span>

### <span data-ttu-id="54437-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54437-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54437-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="54437-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54437-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54437-107">DESCRIPTION</span></span>
<span data-ttu-id="54437-108">Il cmdlet Set-AzDataFactoryV2DataFlow crea un flusso di dati o aggiorna un flusso di dati esistente in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="54437-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="54437-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54437-109">EXAMPLES</span></span>

### <span data-ttu-id="54437-110">Esempio 1: creare un flusso di dati</span><span class="sxs-lookup"><span data-stu-id="54437-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="54437-111">Questo comando crea un flusso di dati denominato TaxiDemo1 nella data factory denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="54437-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="54437-112">Il comando basa il flusso di dati sulle informazioni nella TaxiDemo1.jssu file.</span><span class="sxs-lookup"><span data-stu-id="54437-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="54437-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54437-113">PARAMETERS</span></span>

### <span data-ttu-id="54437-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="54437-114">-DataFactoryName</span></span>
<span data-ttu-id="54437-115">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="54437-115">The data factory name.</span></span>

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

### <span data-ttu-id="54437-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54437-116">-DefaultProfile</span></span>
<span data-ttu-id="54437-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54437-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54437-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="54437-118">-DefinitionFile</span></span>
<span data-ttu-id="54437-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="54437-119">The JSON file path.</span></span>

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

### <span data-ttu-id="54437-120">-Force</span><span class="sxs-lookup"><span data-stu-id="54437-120">-Force</span></span>
<span data-ttu-id="54437-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="54437-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="54437-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="54437-122">-Name</span></span>
<span data-ttu-id="54437-123">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="54437-123">The data flow name.</span></span>

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

### <span data-ttu-id="54437-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54437-124">-ResourceGroupName</span></span>
<span data-ttu-id="54437-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54437-125">The resource group name.</span></span>

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

### <span data-ttu-id="54437-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54437-126">-ResourceId</span></span>
<span data-ttu-id="54437-127">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="54437-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="54437-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54437-128">-Confirm</span></span>
<span data-ttu-id="54437-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54437-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54437-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54437-130">-WhatIf</span></span>
<span data-ttu-id="54437-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54437-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54437-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54437-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54437-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54437-133">CommonParameters</span></span>
<span data-ttu-id="54437-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54437-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54437-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54437-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54437-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54437-136">INPUTS</span></span>

### <span data-ttu-id="54437-137">System. String</span><span class="sxs-lookup"><span data-stu-id="54437-137">System.String</span></span>

## <span data-ttu-id="54437-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54437-138">OUTPUTS</span></span>

### <span data-ttu-id="54437-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="54437-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="54437-140">Note</span><span class="sxs-lookup"><span data-stu-id="54437-140">NOTES</span></span>
<span data-ttu-id="54437-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="54437-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="54437-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54437-142">RELATED LINKS</span></span>

[<span data-ttu-id="54437-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="54437-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="54437-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="54437-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
