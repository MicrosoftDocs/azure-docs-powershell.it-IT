---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 3d5db6b7aa1b7c2ffdd63292696230e2d12bd4c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511256"
---
# <span data-ttu-id="600fa-101">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="600fa-101">Get-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="600fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="600fa-102">SYNOPSIS</span></span>
<span data-ttu-id="600fa-103">Ottiene informazioni sui trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="600fa-103">Gets information about triggers in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="600fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="600fa-104">SYNTAX</span></span>

### <span data-ttu-id="600fa-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="600fa-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="600fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="600fa-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="600fa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="600fa-107">DESCRIPTION</span></span>
<span data-ttu-id="600fa-108">Il cmdlet **Get-AzureRmDataFactoryV2Trigger** ottiene le informazioni sui trigger in una data factory.</span><span class="sxs-lookup"><span data-stu-id="600fa-108">The **Get-AzureRmDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="600fa-109">Se specifichi il nome di un trigger, il cmdlet otterrà le informazioni sul trigger.</span><span class="sxs-lookup"><span data-stu-id="600fa-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="600fa-110">Se non specifichi un nome, il cmdlet riceverà informazioni su tutti i trigger nella data factory.</span><span class="sxs-lookup"><span data-stu-id="600fa-110">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="600fa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="600fa-111">EXAMPLES</span></span>

### <span data-ttu-id="600fa-112">Esempio 1: ottenere informazioni su un trigger specifico</span><span class="sxs-lookup"><span data-stu-id="600fa-112">Example 1: Get information about a specific trigger</span></span>
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

<span data-ttu-id="600fa-113">Ottiene un elenco di tutti i trigger creati nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="600fa-113">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="600fa-114">Esempio 2: ottenere informazioni su tutti i trigger</span><span class="sxs-lookup"><span data-stu-id="600fa-114">Example 2: Get information about all triggers</span></span>
```
Get-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="600fa-115">Ottiene un singolo trigger denominato "ScheduledTrigger" nella Factory di dati "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="600fa-115">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="600fa-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="600fa-116">PARAMETERS</span></span>

### <span data-ttu-id="600fa-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="600fa-117">-DataFactory</span></span>
<span data-ttu-id="600fa-118">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="600fa-118">The data factory object.</span></span>

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

### <span data-ttu-id="600fa-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="600fa-119">-DataFactoryName</span></span>
<span data-ttu-id="600fa-120">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="600fa-120">The data factory name.</span></span>

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

### <span data-ttu-id="600fa-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="600fa-121">-Name</span></span>
<span data-ttu-id="600fa-122">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="600fa-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="600fa-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="600fa-124">The resource group name.</span></span>

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

### <span data-ttu-id="600fa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600fa-125">-DefaultProfile</span></span>
<span data-ttu-id="600fa-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="600fa-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="600fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600fa-127">CommonParameters</span></span>
<span data-ttu-id="600fa-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600fa-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600fa-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="600fa-130">INPUTS</span></span>

### <span data-ttu-id="600fa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="600fa-131">System.String</span></span>
<span data-ttu-id="600fa-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="600fa-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="600fa-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="600fa-133">OUTPUTS</span></span>

### <span data-ttu-id="600fa-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="600fa-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="600fa-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="600fa-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="600fa-136">Note</span><span class="sxs-lookup"><span data-stu-id="600fa-136">NOTES</span></span>

## <span data-ttu-id="600fa-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="600fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="600fa-138">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="600fa-138">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="600fa-139">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="600fa-139">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="600fa-140">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="600fa-140">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="600fa-141">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="600fa-141">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
