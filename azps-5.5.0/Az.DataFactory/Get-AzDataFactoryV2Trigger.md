---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d315ae997a468abc3cd5f4e33601c1c9e770a40a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198862"
---
# <span data-ttu-id="170e3-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="170e3-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="170e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170e3-102">SYNOPSIS</span></span>
<span data-ttu-id="170e3-103">Ottiene informazioni sui trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="170e3-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="170e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="170e3-104">SYNTAX</span></span>

### <span data-ttu-id="170e3-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="170e3-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="170e3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="170e3-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="170e3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="170e3-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="170e3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="170e3-108">DESCRIPTION</span></span>
<span data-ttu-id="170e3-109">Il **cmdlet Get-AzDataFactoryV2Trigger** ottiene informazioni sui trigger in un data factory.</span><span class="sxs-lookup"><span data-stu-id="170e3-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="170e3-110">Se si specifica il nome di un trigger, il cmdlet riceverà informazioni sul trigger.</span><span class="sxs-lookup"><span data-stu-id="170e3-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="170e3-111">Se non si specifica un nome, il cmdlet riceve informazioni su tutti i trigger nel data factory.</span><span class="sxs-lookup"><span data-stu-id="170e3-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="170e3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="170e3-112">EXAMPLES</span></span>

### <span data-ttu-id="170e3-113">Esempio 1: Ottenere informazioni su tutti i trigger</span><span class="sxs-lookup"><span data-stu-id="170e3-113">Example 1: Get information about all triggers</span></span>
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

<span data-ttu-id="170e3-114">Ottiene un elenco di tutti i trigger creati nel data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="170e3-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="170e3-115">Esempio 2: Ottenere informazioni su un trigger specifico</span><span class="sxs-lookup"><span data-stu-id="170e3-115">Example 2: Get information about a specific trigger</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="170e3-116">Ottiene un singolo trigger denominato "ScheduledTrigger" nel data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="170e3-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="170e3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="170e3-117">PARAMETERS</span></span>

### <span data-ttu-id="170e3-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="170e3-118">-DataFactory</span></span>
<span data-ttu-id="170e3-119">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="170e3-119">The data factory object.</span></span>

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

### <span data-ttu-id="170e3-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="170e3-120">-DataFactoryName</span></span>
<span data-ttu-id="170e3-121">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="170e3-121">The data factory name.</span></span>

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

### <span data-ttu-id="170e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170e3-122">-DefaultProfile</span></span>
<span data-ttu-id="170e3-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="170e3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170e3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="170e3-124">-Name</span></span>
<span data-ttu-id="170e3-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="170e3-125">The trigger name.</span></span>

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

### <span data-ttu-id="170e3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170e3-126">-ResourceGroupName</span></span>
<span data-ttu-id="170e3-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="170e3-127">The resource group name.</span></span>

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

### <span data-ttu-id="170e3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="170e3-128">-ResourceId</span></span>
<span data-ttu-id="170e3-129">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="170e3-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="170e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170e3-130">CommonParameters</span></span>
<span data-ttu-id="170e3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170e3-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170e3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170e3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="170e3-133">INPUTS</span></span>

### <span data-ttu-id="170e3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="170e3-134">System.String</span></span>

### <span data-ttu-id="170e3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="170e3-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="170e3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="170e3-136">OUTPUTS</span></span>

### <span data-ttu-id="170e3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="170e3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="170e3-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="170e3-138">NOTES</span></span>

## <span data-ttu-id="170e3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="170e3-139">RELATED LINKS</span></span>

[<span data-ttu-id="170e3-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="170e3-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="170e3-141">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="170e3-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="170e3-142">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="170e3-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="170e3-143">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="170e3-143">Remove-AzDataFactoryV2Trigger</span></span>]()
