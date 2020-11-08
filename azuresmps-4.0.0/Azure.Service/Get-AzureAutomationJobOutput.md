---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023616"
---
# <span data-ttu-id="20e52-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="20e52-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="20e52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20e52-102">SYNOPSIS</span></span>

<span data-ttu-id="20e52-103">Ottiene l'output di un processo di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="20e52-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="20e52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20e52-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20e52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20e52-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="20e52-106">Il cmdlet **Get-AzureAutomationJobOutput** Ottiene l'output di un processo di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20e52-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="20e52-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20e52-107">EXAMPLES</span></span>

### <span data-ttu-id="20e52-108">Esempio 1: ottenere l'output di un processo di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="20e52-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="20e52-109">Questo comando consente di ottenere tutto l'output del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="20e52-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="20e52-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20e52-110">PARAMETERS</span></span>

### <span data-ttu-id="20e52-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20e52-111">-AutomationAccountName</span></span>
<span data-ttu-id="20e52-112">Specifica il nome di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="20e52-112">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e52-113">-ID</span><span class="sxs-lookup"><span data-stu-id="20e52-113">-Id</span></span>
<span data-ttu-id="20e52-114">Specifica l'ID di un processo.</span><span class="sxs-lookup"><span data-stu-id="20e52-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e52-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="20e52-115">-Profile</span></span>
<span data-ttu-id="20e52-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20e52-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20e52-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="20e52-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20e52-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="20e52-118">-StartTime</span></span>
<span data-ttu-id="20e52-119">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="20e52-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e52-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="20e52-120">-Stream</span></span>
<span data-ttu-id="20e52-121">Specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="20e52-121">Specifies the type of output.</span></span>
<span data-ttu-id="20e52-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="20e52-122">Valid values are:</span></span> 

- <span data-ttu-id="20e52-123">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="20e52-123">Any</span></span>
- <span data-ttu-id="20e52-124">Debug</span><span class="sxs-lookup"><span data-stu-id="20e52-124">Debug</span></span>
- <span data-ttu-id="20e52-125">Errore</span><span class="sxs-lookup"><span data-stu-id="20e52-125">Error</span></span>
- <span data-ttu-id="20e52-126">Output</span><span class="sxs-lookup"><span data-stu-id="20e52-126">Output</span></span>
- <span data-ttu-id="20e52-127">Progresso</span><span class="sxs-lookup"><span data-stu-id="20e52-127">Progress</span></span>
- <span data-ttu-id="20e52-128">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="20e52-128">Verbose</span></span>
- <span data-ttu-id="20e52-129">Avviso</span><span class="sxs-lookup"><span data-stu-id="20e52-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20e52-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e52-130">CommonParameters</span></span>
<span data-ttu-id="20e52-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e52-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e52-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e52-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e52-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20e52-133">INPUTS</span></span>

## <span data-ttu-id="20e52-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20e52-134">OUTPUTS</span></span>

## <span data-ttu-id="20e52-135">Note</span><span class="sxs-lookup"><span data-stu-id="20e52-135">NOTES</span></span>

## <span data-ttu-id="20e52-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20e52-136">RELATED LINKS</span></span>

[<span data-ttu-id="20e52-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="20e52-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="20e52-138">Curriculum vitae-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="20e52-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="20e52-139">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="20e52-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="20e52-140">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="20e52-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


