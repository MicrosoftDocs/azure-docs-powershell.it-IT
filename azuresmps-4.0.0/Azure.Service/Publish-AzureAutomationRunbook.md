---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023843"
---
# <span data-ttu-id="54d4c-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="54d4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54d4c-102">SYNOPSIS</span></span>

<span data-ttu-id="54d4c-103">Pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="54d4c-103">Publishes a runbook.</span></span>

## <span data-ttu-id="54d4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54d4c-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="54d4c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54d4c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="54d4c-106">Il cmdlet **Publish-AzureAutomationRunbook** pubblica un Runbook per l'uso nell'ambiente di produzione di Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="54d4c-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="54d4c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="54d4c-108">Esempio 1: pubblicare un Runbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="54d4c-109">Questo comando pubblica il Runbook denominato Runbk01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54d4c-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="54d4c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54d4c-110">PARAMETERS</span></span>

### <span data-ttu-id="54d4c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54d4c-111">-AutomationAccountName</span></span>
<span data-ttu-id="54d4c-112">Specifica il nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="54d4c-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="54d4c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="54d4c-113">-Name</span></span>
<span data-ttu-id="54d4c-114">Specifica il nome di Runbook.</span><span class="sxs-lookup"><span data-stu-id="54d4c-114">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="54d4c-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="54d4c-115">-Profile</span></span>
<span data-ttu-id="54d4c-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d4c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54d4c-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="54d4c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54d4c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d4c-118">CommonParameters</span></span>
<span data-ttu-id="54d4c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d4c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d4c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d4c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d4c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54d4c-121">INPUTS</span></span>

## <span data-ttu-id="54d4c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54d4c-122">OUTPUTS</span></span>

## <span data-ttu-id="54d4c-123">Note</span><span class="sxs-lookup"><span data-stu-id="54d4c-123">NOTES</span></span>

## <span data-ttu-id="54d4c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54d4c-124">RELATED LINKS</span></span>

[<span data-ttu-id="54d4c-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="54d4c-126">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="54d4c-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="54d4c-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="54d4c-129">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="54d4c-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


