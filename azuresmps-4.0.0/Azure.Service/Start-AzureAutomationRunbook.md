---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029494"
---
# <span data-ttu-id="c5f71-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="c5f71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5f71-102">SYNOPSIS</span></span>

<span data-ttu-id="c5f71-103">Avvia un processo di Runbook.</span><span class="sxs-lookup"><span data-stu-id="c5f71-103">Starts a runbook job.</span></span>

## <span data-ttu-id="c5f71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5f71-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c5f71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5f71-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c5f71-106">Il cmdlet **Start-AzureAutomationRunbook** avvia un processo di Runbook di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f71-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="c5f71-107">Specificare l'ID o il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="c5f71-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="c5f71-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5f71-108">EXAMPLES</span></span>

### <span data-ttu-id="c5f71-109">Esempio 1: avviare un processo di Runbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="c5f71-110">Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c5f71-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c5f71-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5f71-111">PARAMETERS</span></span>

### <span data-ttu-id="c5f71-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c5f71-112">-AutomationAccountName</span></span>
<span data-ttu-id="c5f71-113">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="c5f71-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c5f71-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5f71-114">-Name</span></span>
<span data-ttu-id="c5f71-115">Specifica il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="c5f71-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f71-116">-Parameters</span><span class="sxs-lookup"><span data-stu-id="c5f71-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f71-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="c5f71-117">-Profile</span></span>
<span data-ttu-id="c5f71-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5f71-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5f71-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c5f71-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5f71-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="c5f71-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f71-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f71-121">CommonParameters</span></span>
<span data-ttu-id="c5f71-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f71-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f71-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f71-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f71-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5f71-124">INPUTS</span></span>

## <span data-ttu-id="c5f71-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5f71-125">OUTPUTS</span></span>

### <span data-ttu-id="c5f71-126">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="c5f71-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="c5f71-127">Note</span><span class="sxs-lookup"><span data-stu-id="c5f71-127">NOTES</span></span>

## <span data-ttu-id="c5f71-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5f71-128">RELATED LINKS</span></span>

[<span data-ttu-id="c5f71-129">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="c5f71-130">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="c5f71-131">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="c5f71-132">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="c5f71-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c5f71-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


