---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: e5afbdd389d1ee9e1b74895743ed47ceed0b4ae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675004"
---
# <span data-ttu-id="57fba-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57fba-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="57fba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57fba-102">SYNOPSIS</span></span>
<span data-ttu-id="57fba-103">Ottiene informazioni sui trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="57fba-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="57fba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57fba-104">SYNTAX</span></span>

### <span data-ttu-id="57fba-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57fba-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57fba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="57fba-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57fba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="57fba-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57fba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57fba-108">DESCRIPTION</span></span>
<span data-ttu-id="57fba-109">Il cmdlet **Get-AzDataFactoryV2Trigger** ottiene le informazioni sui trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="57fba-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="57fba-110">Se specifichi il nome di un trigger, il cmdlet otterrà le informazioni sul trigger.</span><span class="sxs-lookup"><span data-stu-id="57fba-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="57fba-111">Se non specifichi un nome, il cmdlet riceverà informazioni su tutti i trigger nella data factory.</span><span class="sxs-lookup"><span data-stu-id="57fba-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="57fba-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57fba-112">EXAMPLES</span></span>

### <span data-ttu-id="57fba-113">Esempio 1: ottenere informazioni su un trigger specifico</span><span class="sxs-lookup"><span data-stu-id="57fba-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="57fba-114">Ottiene un elenco di tutti i trigger creati nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="57fba-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="57fba-115">Esempio 2: ottenere informazioni su tutti i trigger</span><span class="sxs-lookup"><span data-stu-id="57fba-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="57fba-116">Ottiene un singolo trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="57fba-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="57fba-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57fba-117">PARAMETERS</span></span>

### <span data-ttu-id="57fba-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="57fba-118">-DataFactory</span></span>
<span data-ttu-id="57fba-119">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="57fba-119">The data factory object.</span></span>

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

### <span data-ttu-id="57fba-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="57fba-120">-DataFactoryName</span></span>
<span data-ttu-id="57fba-121">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="57fba-121">The data factory name.</span></span>

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

### <span data-ttu-id="57fba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fba-122">-DefaultProfile</span></span>
<span data-ttu-id="57fba-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57fba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57fba-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="57fba-124">-Name</span></span>
<span data-ttu-id="57fba-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="57fba-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57fba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fba-126">-ResourceGroupName</span></span>
<span data-ttu-id="57fba-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57fba-127">The resource group name.</span></span>

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

### <span data-ttu-id="57fba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57fba-128">-ResourceId</span></span>
<span data-ttu-id="57fba-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="57fba-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="57fba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fba-130">CommonParameters</span></span>
<span data-ttu-id="57fba-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57fba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fba-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fba-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57fba-133">INPUTS</span></span>

### <span data-ttu-id="57fba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="57fba-134">System.String</span></span>

### <span data-ttu-id="57fba-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="57fba-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="57fba-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57fba-136">OUTPUTS</span></span>

### <span data-ttu-id="57fba-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="57fba-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="57fba-138">Note</span><span class="sxs-lookup"><span data-stu-id="57fba-138">NOTES</span></span>

## <span data-ttu-id="57fba-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57fba-139">RELATED LINKS</span></span>

[<span data-ttu-id="57fba-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57fba-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57fba-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57fba-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57fba-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57fba-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="57fba-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="57fba-143">Remove-AzDataFactoryV2Trigger</span></span>]()
