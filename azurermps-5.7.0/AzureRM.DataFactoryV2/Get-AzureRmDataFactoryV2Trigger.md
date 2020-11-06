---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 5004b50cf5bb5b22a95ef00bf19f0e783fd04cb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521060"
---
# <span data-ttu-id="9f033-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9f033-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9f033-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f033-102">SYNOPSIS</span></span>
<span data-ttu-id="9f033-103">Ottiene informazioni sui trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="9f033-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f033-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f033-104">SYNTAX</span></span>

### <span data-ttu-id="9f033-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f033-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f033-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9f033-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f033-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f033-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f033-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f033-108">DESCRIPTION</span></span>
<span data-ttu-id="9f033-109">Il cmdlet **Get-AzureRmDataFactoryV2Trigger** ottiene le informazioni sui trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="9f033-109">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="9f033-110">Se specifichi il nome di un trigger, il cmdlet otterrà le informazioni sul trigger.</span><span class="sxs-lookup"><span data-stu-id="9f033-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="9f033-111">Se non specifichi un nome, il cmdlet riceverà informazioni su tutti i trigger nella data factory.</span><span class="sxs-lookup"><span data-stu-id="9f033-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="9f033-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f033-112">EXAMPLES</span></span>

### <span data-ttu-id="9f033-113">Esempio 1: ottenere informazioni su un trigger specifico</span><span class="sxs-lookup"><span data-stu-id="9f033-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="9f033-114">Ottiene un elenco di tutti i trigger creati nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9f033-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="9f033-115">Esempio 2: ottenere informazioni su tutti i trigger</span><span class="sxs-lookup"><span data-stu-id="9f033-115">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="9f033-116">Ottiene un singolo trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9f033-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="9f033-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f033-117">PARAMETERS</span></span>

### <span data-ttu-id="9f033-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9f033-118">-DataFactory</span></span>
<span data-ttu-id="9f033-119">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9f033-119">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f033-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9f033-120">-DataFactoryName</span></span>
<span data-ttu-id="9f033-121">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="9f033-121">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f033-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f033-122">-DefaultProfile</span></span>
<span data-ttu-id="9f033-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f033-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f033-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f033-124">-Name</span></span>
<span data-ttu-id="9f033-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="9f033-125">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f033-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f033-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f033-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f033-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f033-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f033-128">-ResourceId</span></span>
<span data-ttu-id="9f033-129">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f033-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f033-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f033-130">CommonParameters</span></span>
<span data-ttu-id="9f033-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f033-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f033-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f033-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f033-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f033-133">INPUTS</span></span>

### <span data-ttu-id="9f033-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9f033-134">System.String</span></span>
<span data-ttu-id="9f033-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9f033-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="9f033-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f033-136">OUTPUTS</span></span>

### <span data-ttu-id="9f033-137">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9f033-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9f033-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9f033-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9f033-139">Note</span><span class="sxs-lookup"><span data-stu-id="9f033-139">NOTES</span></span>

## <span data-ttu-id="9f033-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f033-140">RELATED LINKS</span></span>

[<span data-ttu-id="9f033-141">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9f033-141">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9f033-142">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9f033-142">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9f033-143">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9f033-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9f033-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9f033-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
