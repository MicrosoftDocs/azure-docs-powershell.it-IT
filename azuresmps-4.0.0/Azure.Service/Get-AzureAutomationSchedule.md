---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023613"
---
# <span data-ttu-id="c22fc-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c22fc-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="c22fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c22fc-102">SYNOPSIS</span></span>

<span data-ttu-id="c22fc-103">Ottiene una pianificazione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c22fc-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="c22fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c22fc-104">SYNTAX</span></span>

### <span data-ttu-id="c22fc-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c22fc-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c22fc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c22fc-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c22fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c22fc-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c22fc-108">Il cmdlet **Get-AzureAutomationSchedule** ottiene una pianificazione di Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c22fc-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="c22fc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c22fc-109">EXAMPLES</span></span>

### <span data-ttu-id="c22fc-110">Esempio 1: ottenere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="c22fc-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="c22fc-111">Questo comando consente di ottenere la pianificazione denominata DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="c22fc-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="c22fc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c22fc-112">PARAMETERS</span></span>

### <span data-ttu-id="c22fc-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c22fc-113">-AutomationAccountName</span></span>
<span data-ttu-id="c22fc-114">Specifica il nome di un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c22fc-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="c22fc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c22fc-115">-Name</span></span>
<span data-ttu-id="c22fc-116">Specifica il nome di una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c22fc-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22fc-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="c22fc-117">-Profile</span></span>
<span data-ttu-id="c22fc-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c22fc-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c22fc-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c22fc-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c22fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22fc-120">CommonParameters</span></span>
<span data-ttu-id="c22fc-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c22fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22fc-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22fc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22fc-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c22fc-123">INPUTS</span></span>

## <span data-ttu-id="c22fc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c22fc-124">OUTPUTS</span></span>

### <span data-ttu-id="c22fc-125">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="c22fc-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="c22fc-126">Note</span><span class="sxs-lookup"><span data-stu-id="c22fc-126">NOTES</span></span>

## <span data-ttu-id="c22fc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c22fc-127">RELATED LINKS</span></span>

[<span data-ttu-id="c22fc-128">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c22fc-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="c22fc-129">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c22fc-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="c22fc-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c22fc-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


