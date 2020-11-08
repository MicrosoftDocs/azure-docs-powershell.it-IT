---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023615"
---
# <span data-ttu-id="59905-101">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59905-101">Get-AzureAutomationRunbook</span></span>

## <span data-ttu-id="59905-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59905-102">SYNOPSIS</span></span>

<span data-ttu-id="59905-103">Ottiene un Runbook.</span><span class="sxs-lookup"><span data-stu-id="59905-103">Gets a runbook.</span></span>

## <span data-ttu-id="59905-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59905-104">SYNTAX</span></span>

### <span data-ttu-id="59905-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59905-105">ByAll (Default)</span></span>
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="59905-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="59905-106">ByRunbookName</span></span>
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="59905-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59905-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="59905-108">Il cmdlet **Get-AzureAutomationRunbook** ottiene uno o più manuali operativi di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="59905-108">The **Get-AzureAutomationRunbook** cmdlet gets one or more Microsoft Azure Automation runbooks.</span></span>
<span data-ttu-id="59905-109">Per impostazione predefinita, vengono restituiti tutti i manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="59905-109">By default, all runbooks are returned.</span></span>
<span data-ttu-id="59905-110">Per ottenere uno specifico Runbook, specificare il nome o l'ID.</span><span class="sxs-lookup"><span data-stu-id="59905-110">To get a specific runbook, specify its name or ID.</span></span>
<span data-ttu-id="59905-111">Per ottenere tutti i manuali operativi collegati a una programmazione specifica, specificare il nome della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="59905-111">To get all runbooks linked to a specific schedule, specify the schedule name.</span></span>

## <span data-ttu-id="59905-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59905-112">EXAMPLES</span></span>

### <span data-ttu-id="59905-113">Esempio 1: ottenere tutti manuali operativi</span><span class="sxs-lookup"><span data-stu-id="59905-113">Example 1: Get all runbooks</span></span>
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="59905-114">Questo comando ottiene tutti i manuali operativi nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="59905-114">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="59905-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59905-115">PARAMETERS</span></span>

### <span data-ttu-id="59905-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="59905-116">-AutomationAccountName</span></span>
<span data-ttu-id="59905-117">Specifica il nome di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="59905-117">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="59905-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="59905-118">-Name</span></span>
<span data-ttu-id="59905-119">Specifica il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="59905-119">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59905-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="59905-120">-Profile</span></span>
<span data-ttu-id="59905-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59905-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59905-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="59905-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59905-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59905-123">CommonParameters</span></span>
<span data-ttu-id="59905-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59905-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59905-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59905-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59905-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59905-126">INPUTS</span></span>

## <span data-ttu-id="59905-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59905-127">OUTPUTS</span></span>

### <span data-ttu-id="59905-128">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="59905-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="59905-129">Note</span><span class="sxs-lookup"><span data-stu-id="59905-129">NOTES</span></span>

## <span data-ttu-id="59905-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59905-130">RELATED LINKS</span></span>

[<span data-ttu-id="59905-131">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59905-131">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="59905-132">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59905-132">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="59905-133">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59905-133">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="59905-134">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59905-134">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="59905-135">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59905-135">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


