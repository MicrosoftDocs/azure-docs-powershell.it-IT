---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487631"
---
# <span data-ttu-id="8a556-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="8a556-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="8a556-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a556-102">SYNOPSIS</span></span>
<span data-ttu-id="8a556-103">Ottiene informazioni sui flussi di dati in data factory.</span><span class="sxs-lookup"><span data-stu-id="8a556-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="8a556-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a556-104">SYNTAX</span></span>

### <span data-ttu-id="8a556-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a556-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a556-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8a556-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a556-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a556-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a556-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a556-108">DESCRIPTION</span></span>
<span data-ttu-id="8a556-109">Il cmdlet Get-AzDataFactoryV2DataFlow ottiene informazioni sui flussi di dati in Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8a556-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="8a556-110">Se specifichi il nome di un flusso di dati, questo cmdlet ottiene le informazioni sul flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="8a556-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="8a556-111">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i flussi di dati nella Factory di dati.</span><span class="sxs-lookup"><span data-stu-id="8a556-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="8a556-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a556-112">EXAMPLES</span></span>
### <span data-ttu-id="8a556-113">Esempio 1: ottenere informazioni su tutti i flussi di dati</span><span class="sxs-lookup"><span data-stu-id="8a556-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="8a556-114">Questo comando consente di ottenere informazioni su tutti i flussi di dati nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8a556-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8a556-115">Esempio 2: ottenere informazioni su un flusso di dati specifico</span><span class="sxs-lookup"><span data-stu-id="8a556-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="8a556-116">Questo comando consente di ottenere informazioni sul flusso di dati denominato dataflow1 nella Factory di dati denominata WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8a556-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="8a556-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a556-117">PARAMETERS</span></span>

### <span data-ttu-id="8a556-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8a556-118">-DataFactory</span></span>
<span data-ttu-id="8a556-119">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8a556-119">The data factory object.</span></span>

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

### <span data-ttu-id="8a556-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8a556-120">-DataFactoryName</span></span>
<span data-ttu-id="8a556-121">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="8a556-121">The data factory name.</span></span>

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

### <span data-ttu-id="8a556-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a556-122">-DefaultProfile</span></span>
<span data-ttu-id="8a556-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a556-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a556-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a556-124">-Name</span></span>
<span data-ttu-id="8a556-125">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="8a556-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a556-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a556-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a556-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8a556-127">The resource group name.</span></span>

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

### <span data-ttu-id="8a556-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a556-128">-ResourceId</span></span>
<span data-ttu-id="8a556-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a556-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8a556-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a556-130">CommonParameters</span></span>
<span data-ttu-id="8a556-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a556-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a556-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a556-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a556-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a556-133">INPUTS</span></span>

### <span data-ttu-id="8a556-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8a556-134">System.String</span></span>

### <span data-ttu-id="8a556-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8a556-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8a556-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a556-136">OUTPUTS</span></span>

### <span data-ttu-id="8a556-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="8a556-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="8a556-138">Note</span><span class="sxs-lookup"><span data-stu-id="8a556-138">NOTES</span></span>
<span data-ttu-id="8a556-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="8a556-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8a556-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a556-140">RELATED LINKS</span></span>

[<span data-ttu-id="8a556-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8a556-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="8a556-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8a556-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)