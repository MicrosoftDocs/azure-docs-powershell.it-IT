---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029533"
---
# <span data-ttu-id="2534e-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2534e-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="2534e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2534e-102">SYNOPSIS</span></span>

<span data-ttu-id="2534e-103">Modifica una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="2534e-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="2534e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2534e-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2534e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2534e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2534e-106">Il cmdlet **set-AzureAutomationSchedule** modifica una programmazione in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2534e-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="2534e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2534e-107">EXAMPLES</span></span>

### <span data-ttu-id="2534e-108">Esempio 1: modificare una programmazione</span><span class="sxs-lookup"><span data-stu-id="2534e-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="2534e-109">Questo comando modifica la descrizione della programmazione denominata Schedule01.</span><span class="sxs-lookup"><span data-stu-id="2534e-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="2534e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2534e-110">PARAMETERS</span></span>

### <span data-ttu-id="2534e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2534e-111">-AutomationAccountName</span></span>
<span data-ttu-id="2534e-112">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="2534e-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="2534e-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2534e-113">-Description</span></span>
<span data-ttu-id="2534e-114">Specifica una descrizione per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="2534e-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2534e-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="2534e-115">-IsEnabled</span></span>
<span data-ttu-id="2534e-116">Indica se la pianificazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2534e-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2534e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2534e-117">-Name</span></span>
<span data-ttu-id="2534e-118">Specifica un nome per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="2534e-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="2534e-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="2534e-119">-Profile</span></span>
<span data-ttu-id="2534e-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2534e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2534e-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2534e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2534e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2534e-122">CommonParameters</span></span>
<span data-ttu-id="2534e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2534e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2534e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2534e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2534e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2534e-125">INPUTS</span></span>

## <span data-ttu-id="2534e-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2534e-126">OUTPUTS</span></span>

### <span data-ttu-id="2534e-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="2534e-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="2534e-128">Note</span><span class="sxs-lookup"><span data-stu-id="2534e-128">NOTES</span></span>

## <span data-ttu-id="2534e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2534e-129">RELATED LINKS</span></span>

[<span data-ttu-id="2534e-130">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2534e-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="2534e-131">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2534e-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="2534e-132">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2534e-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


