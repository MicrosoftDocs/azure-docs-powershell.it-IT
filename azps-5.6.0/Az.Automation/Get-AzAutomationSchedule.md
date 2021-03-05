---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a32b86ce308f18537ec1acda62c2694e7b621d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014221"
---
# <span data-ttu-id="8dd23-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd23-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="8dd23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dd23-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd23-103">Ottiene una pianificazione dell'automazione.</span><span class="sxs-lookup"><span data-stu-id="8dd23-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="8dd23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dd23-104">SYNTAX</span></span>

### <span data-ttu-id="8dd23-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8dd23-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd23-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8dd23-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dd23-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8dd23-107">DESCRIPTION</span></span>
<span data-ttu-id="8dd23-108">Il cmdlet **Get-AzAutomationSchedule** ottiene una pianificazione di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd23-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="8dd23-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dd23-109">EXAMPLES</span></span>

### <span data-ttu-id="8dd23-110">Esempio 1: Ottenere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="8dd23-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8dd23-111">Questo comando recupera la pianificazione denominata DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="8dd23-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="8dd23-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dd23-112">PARAMETERS</span></span>

### <span data-ttu-id="8dd23-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8dd23-113">-AutomationAccountName</span></span>
<span data-ttu-id="8dd23-114">Specifica il nome di un account di automazione per cui questo cmdlet ottiene una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8dd23-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd23-115">-DefaultProfile</span></span>
<span data-ttu-id="8dd23-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8dd23-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd23-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8dd23-117">-Name</span></span>
<span data-ttu-id="8dd23-118">Specifica il nome di una pianificazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd23-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd23-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd23-119">-ResourceGroupName</span></span>
<span data-ttu-id="8dd23-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="8dd23-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd23-121">CommonParameters</span></span>
<span data-ttu-id="8dd23-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd23-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd23-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd23-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="8dd23-124">INPUTS</span></span>

### <span data-ttu-id="8dd23-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8dd23-125">System.String</span></span>

## <span data-ttu-id="8dd23-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dd23-126">OUTPUTS</span></span>

### <span data-ttu-id="8dd23-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="8dd23-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="8dd23-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="8dd23-128">NOTES</span></span>

## <span data-ttu-id="8dd23-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dd23-129">RELATED LINKS</span></span>

[<span data-ttu-id="8dd23-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd23-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="8dd23-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd23-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="8dd23-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="8dd23-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


