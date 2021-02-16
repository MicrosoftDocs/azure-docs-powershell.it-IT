---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 7bd25d444a4277e2aa423026be551fab1c5f360e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415156"
---
# <span data-ttu-id="25d1a-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="25d1a-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="25d1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="25d1a-103">Ottiene informazioni sui flussi di dati in Data factory.</span><span class="sxs-lookup"><span data-stu-id="25d1a-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="25d1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25d1a-104">SYNTAX</span></span>

### <span data-ttu-id="25d1a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="25d1a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d1a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="25d1a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25d1a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25d1a-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25d1a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25d1a-108">DESCRIPTION</span></span>
<span data-ttu-id="25d1a-109">Il Get-AzDataFactoryV2DataFlow cmdlet recupera informazioni sui flussi di dati in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="25d1a-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="25d1a-110">Se si specifica il nome di un flusso di dati, questo cmdlet riceve informazioni sul flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="25d1a-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="25d1a-111">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i flussi di dati nel data factory.</span><span class="sxs-lookup"><span data-stu-id="25d1a-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="25d1a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25d1a-112">EXAMPLES</span></span>
### <span data-ttu-id="25d1a-113">Esempio 1: Ottenere informazioni su tutti i flussi di dati</span><span class="sxs-lookup"><span data-stu-id="25d1a-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="25d1a-114">Questo comando recupera informazioni su tutti i flussi di dati nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="25d1a-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="25d1a-115">Esempio 2: Ottenere informazioni su un flusso di dati specifico</span><span class="sxs-lookup"><span data-stu-id="25d1a-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="25d1a-116">Questo comando recupera informazioni sul flusso di dati denominato flusso di dati1 nel data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="25d1a-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="25d1a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25d1a-117">PARAMETERS</span></span>

### <span data-ttu-id="25d1a-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="25d1a-118">-DataFactory</span></span>
<span data-ttu-id="25d1a-119">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="25d1a-119">The data factory object.</span></span>

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

### <span data-ttu-id="25d1a-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="25d1a-120">-DataFactoryName</span></span>
<span data-ttu-id="25d1a-121">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="25d1a-121">The data factory name.</span></span>

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

### <span data-ttu-id="25d1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d1a-122">-DefaultProfile</span></span>
<span data-ttu-id="25d1a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25d1a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d1a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="25d1a-124">-Name</span></span>
<span data-ttu-id="25d1a-125">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="25d1a-125">The data flow name.</span></span>

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

### <span data-ttu-id="25d1a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d1a-126">-ResourceGroupName</span></span>
<span data-ttu-id="25d1a-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25d1a-127">The resource group name.</span></span>

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

### <span data-ttu-id="25d1a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25d1a-128">-ResourceId</span></span>
<span data-ttu-id="25d1a-129">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="25d1a-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="25d1a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d1a-130">CommonParameters</span></span>
<span data-ttu-id="25d1a-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d1a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d1a-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25d1a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d1a-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="25d1a-133">INPUTS</span></span>

### <span data-ttu-id="25d1a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="25d1a-134">System.String</span></span>

### <span data-ttu-id="25d1a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="25d1a-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="25d1a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25d1a-136">OUTPUTS</span></span>

### <span data-ttu-id="25d1a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="25d1a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="25d1a-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="25d1a-138">NOTES</span></span>
<span data-ttu-id="25d1a-139">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="25d1a-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="25d1a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25d1a-140">RELATED LINKS</span></span>


