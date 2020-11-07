---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 7d3f1ca73712753ad38b46c186a51bd7aa159b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685734"
---
# <span data-ttu-id="32a70-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="32a70-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="32a70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32a70-102">SYNOPSIS</span></span>
<span data-ttu-id="32a70-103">Restituisce informazioni sulle esecuzioni dei trigger.</span><span class="sxs-lookup"><span data-stu-id="32a70-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32a70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32a70-104">SYNTAX</span></span>

### <span data-ttu-id="32a70-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32a70-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32a70-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="32a70-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32a70-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32a70-107">DESCRIPTION</span></span>
<span data-ttu-id="32a70-108">Il comando **Get-AzureRmDataFactoryV2TriggerRun** restituisce informazioni dettagliate sulle esecuzioni dei trigger per il trigger specificato nell'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="32a70-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="32a70-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32a70-109">EXAMPLES</span></span>

### <span data-ttu-id="32a70-110">Esempio 1: ottenere informazioni sull'esecuzione del trigger</span><span class="sxs-lookup"><span data-stu-id="32a70-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="32a70-111">Questo comando Mostra le informazioni sulle esecuzioni per "WikiTrigger" nella Factory "WikiADF" iniziata tra "2017-09-01" e "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="32a70-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="32a70-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32a70-112">PARAMETERS</span></span>

### <span data-ttu-id="32a70-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="32a70-113">-DataFactory</span></span>
<span data-ttu-id="32a70-114">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="32a70-114">The data factory object.</span></span>

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

### <span data-ttu-id="32a70-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="32a70-115">-DataFactoryName</span></span>
<span data-ttu-id="32a70-116">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="32a70-116">The data factory name.</span></span>

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

### <span data-ttu-id="32a70-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="32a70-117">-Name</span></span>
<span data-ttu-id="32a70-118">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="32a70-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a70-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a70-119">-ResourceGroupName</span></span>
<span data-ttu-id="32a70-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32a70-120">The resource group name.</span></span>

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

### <span data-ttu-id="32a70-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="32a70-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="32a70-122">Il tempo trascorso o dopo il quale l'esecuzione del trigger viene avviata in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="32a70-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a70-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="32a70-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="32a70-124">L'ora in cui viene eseguito il trigger o prima del quale viene avviata l'esecuzione in formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="32a70-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a70-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a70-125">-DefaultProfile</span></span>
<span data-ttu-id="32a70-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32a70-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a70-127">CommonParameters</span></span>
<span data-ttu-id="32a70-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a70-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a70-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a70-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32a70-130">INPUTS</span></span>

### <span data-ttu-id="32a70-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="32a70-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="32a70-132">System. String</span><span class="sxs-lookup"><span data-stu-id="32a70-132">System.String</span></span>

## <span data-ttu-id="32a70-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32a70-133">OUTPUTS</span></span>

### <span data-ttu-id="32a70-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="32a70-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="32a70-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="32a70-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="32a70-136">Note</span><span class="sxs-lookup"><span data-stu-id="32a70-136">NOTES</span></span>

## <span data-ttu-id="32a70-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32a70-137">RELATED LINKS</span></span>

[<span data-ttu-id="32a70-138">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="32a70-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="32a70-139">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="32a70-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

