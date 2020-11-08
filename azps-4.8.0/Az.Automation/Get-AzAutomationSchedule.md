---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033549"
---
# <span data-ttu-id="976f1-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="976f1-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="976f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="976f1-102">SYNOPSIS</span></span>
<span data-ttu-id="976f1-103">Ottiene una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="976f1-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="976f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="976f1-104">SYNTAX</span></span>

### <span data-ttu-id="976f1-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="976f1-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="976f1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="976f1-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="976f1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="976f1-107">DESCRIPTION</span></span>
<span data-ttu-id="976f1-108">Il cmdlet **Get-AzAutomationSchedule** ottiene una pianificazione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="976f1-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="976f1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="976f1-109">EXAMPLES</span></span>

### <span data-ttu-id="976f1-110">Esempio 1: ottenere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="976f1-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="976f1-111">Questo comando consente di ottenere la pianificazione denominata DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="976f1-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="976f1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="976f1-112">PARAMETERS</span></span>

### <span data-ttu-id="976f1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="976f1-113">-AutomationAccountName</span></span>
<span data-ttu-id="976f1-114">Specifica il nome di un account di automazione per cui questo cmdlet ottiene una programmazione.</span><span class="sxs-lookup"><span data-stu-id="976f1-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="976f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976f1-115">-DefaultProfile</span></span>
<span data-ttu-id="976f1-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="976f1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="976f1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="976f1-117">-Name</span></span>
<span data-ttu-id="976f1-118">Specifica il nome di una pianificazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976f1-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="976f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="976f1-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene una programmazione.</span><span class="sxs-lookup"><span data-stu-id="976f1-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="976f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976f1-121">CommonParameters</span></span>
<span data-ttu-id="976f1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976f1-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976f1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976f1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="976f1-124">INPUTS</span></span>

### <span data-ttu-id="976f1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="976f1-125">System.String</span></span>

## <span data-ttu-id="976f1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="976f1-126">OUTPUTS</span></span>

### <span data-ttu-id="976f1-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="976f1-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="976f1-128">Note</span><span class="sxs-lookup"><span data-stu-id="976f1-128">NOTES</span></span>

## <span data-ttu-id="976f1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="976f1-129">RELATED LINKS</span></span>

[<span data-ttu-id="976f1-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="976f1-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="976f1-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="976f1-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="976f1-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="976f1-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


