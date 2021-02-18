---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201167"
---
# <span data-ttu-id="474df-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="474df-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="474df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="474df-102">SYNOPSIS</span></span>
<span data-ttu-id="474df-103">Ottiene una pianificazione dell'automazione.</span><span class="sxs-lookup"><span data-stu-id="474df-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="474df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="474df-104">SYNTAX</span></span>

### <span data-ttu-id="474df-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="474df-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="474df-106">ByName</span><span class="sxs-lookup"><span data-stu-id="474df-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474df-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="474df-107">DESCRIPTION</span></span>
<span data-ttu-id="474df-108">Il cmdlet **Get-AzAutomationSchedule** ottiene una pianificazione di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="474df-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="474df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="474df-109">EXAMPLES</span></span>

### <span data-ttu-id="474df-110">Esempio 1: Ottenere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="474df-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="474df-111">Questo comando recupera la pianificazione denominata DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="474df-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="474df-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="474df-112">PARAMETERS</span></span>

### <span data-ttu-id="474df-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="474df-113">-AutomationAccountName</span></span>
<span data-ttu-id="474df-114">Specifica il nome di un account di automazione per cui questo cmdlet ottiene una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="474df-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="474df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474df-115">-DefaultProfile</span></span>
<span data-ttu-id="474df-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="474df-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="474df-117">-Name</span><span class="sxs-lookup"><span data-stu-id="474df-117">-Name</span></span>
<span data-ttu-id="474df-118">Specifica il nome di una pianificazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="474df-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="474df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474df-119">-ResourceGroupName</span></span>
<span data-ttu-id="474df-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="474df-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="474df-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474df-121">CommonParameters</span></span>
<span data-ttu-id="474df-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474df-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474df-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474df-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474df-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="474df-124">INPUTS</span></span>

### <span data-ttu-id="474df-125">System.String</span><span class="sxs-lookup"><span data-stu-id="474df-125">System.String</span></span>

## <span data-ttu-id="474df-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="474df-126">OUTPUTS</span></span>

### <span data-ttu-id="474df-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="474df-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="474df-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="474df-128">NOTES</span></span>

## <span data-ttu-id="474df-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="474df-129">RELATED LINKS</span></span>

[<span data-ttu-id="474df-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="474df-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="474df-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="474df-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="474df-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="474df-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


