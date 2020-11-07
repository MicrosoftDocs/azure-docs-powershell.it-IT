---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687537"
---
# <span data-ttu-id="1369e-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="1369e-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="1369e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1369e-102">SYNOPSIS</span></span>
<span data-ttu-id="1369e-103">Restituisce informazioni sulle esecuzioni dei trigger.</span><span class="sxs-lookup"><span data-stu-id="1369e-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1369e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1369e-104">SYNTAX</span></span>

### <span data-ttu-id="1369e-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1369e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="1369e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1369e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="1369e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1369e-107">DESCRIPTION</span></span>
<span data-ttu-id="1369e-108">Il comando **Get-AzureRmDataFactoryV2TriggerRun** restituisce informazioni dettagliate sulle esecuzioni dei trigger per il trigger specificato nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="1369e-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="1369e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1369e-109">EXAMPLES</span></span>

### <span data-ttu-id="1369e-110">Esempio 1: ottenere informazioni sull'esecuzione del trigger</span><span class="sxs-lookup"><span data-stu-id="1369e-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="1369e-111">Questo comando Mostra le informazioni sulle esecuzioni per "WikiTrigger" nella Factory "WikiADF" iniziata tra "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="1369e-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="1369e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1369e-112">PARAMETERS</span></span>

### <span data-ttu-id="1369e-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1369e-113">-DataFactory</span></span>
<span data-ttu-id="1369e-114">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1369e-114">The data factory object.</span></span>

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

### <span data-ttu-id="1369e-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1369e-115">-DataFactoryName</span></span>
<span data-ttu-id="1369e-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="1369e-116">The data factory name.</span></span>

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

### <span data-ttu-id="1369e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1369e-117">-Name</span></span>
<span data-ttu-id="1369e-118">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="1369e-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1369e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1369e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1369e-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1369e-120">The resource group name.</span></span>

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

### <span data-ttu-id="1369e-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="1369e-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="1369e-122">Il tempo trascorso o dopo il quale l'esecuzione del trigger viene avviata in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="1369e-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1369e-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="1369e-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="1369e-124">L'ora in cui viene eseguito il trigger o prima del quale viene avviata l'esecuzione in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="1369e-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1369e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1369e-125">INPUTS</span></span>

### <span data-ttu-id="1369e-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1369e-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="1369e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1369e-127">System.String</span></span>


## <span data-ttu-id="1369e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1369e-128">OUTPUTS</span></span>

### <span data-ttu-id="1369e-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1369e-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="1369e-130">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="1369e-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="1369e-131">Note</span><span class="sxs-lookup"><span data-stu-id="1369e-131">NOTES</span></span>

## <span data-ttu-id="1369e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1369e-132">RELATED LINKS</span></span>
[<span data-ttu-id="1369e-133">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1369e-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="1369e-134">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="1369e-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

