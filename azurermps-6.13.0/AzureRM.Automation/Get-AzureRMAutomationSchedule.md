---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 78e34c5d3d94a964fbff6d0cbaa74c9dd3dd2177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519775"
---
# <span data-ttu-id="9e6e1-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9e6e1-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="9e6e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6e1-103">Ottiene una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e6e1-104">SYNTAX</span></span>

### <span data-ttu-id="9e6e1-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e6e1-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e6e1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e6e1-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6e1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e6e1-107">DESCRIPTION</span></span>
<span data-ttu-id="9e6e1-108">Il cmdlet **Get-AzureRmAutomationSchedule** ottiene una pianificazione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="9e6e1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e6e1-109">EXAMPLES</span></span>

### <span data-ttu-id="9e6e1-110">Esempio 1: ottenere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="9e6e1-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9e6e1-111">Questo comando consente di ottenere la pianificazione denominata DailySchedule08.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="9e6e1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e6e1-112">PARAMETERS</span></span>

### <span data-ttu-id="9e6e1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e6e1-113">-AutomationAccountName</span></span>
<span data-ttu-id="9e6e1-114">Specifica il nome di un account di automazione per cui questo cmdlet ottiene una programmazione.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="9e6e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6e1-115">-DefaultProfile</span></span>
<span data-ttu-id="9e6e1-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e6e1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e6e1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e6e1-117">-Name</span></span>
<span data-ttu-id="9e6e1-118">Specifica il nome di una pianificazione ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e6e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="9e6e1-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene una programmazione.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="9e6e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6e1-121">CommonParameters</span></span>
<span data-ttu-id="9e6e1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6e1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6e1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6e1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e6e1-124">INPUTS</span></span>

### <span data-ttu-id="9e6e1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9e6e1-125">System.String</span></span>

## <span data-ttu-id="9e6e1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e6e1-126">OUTPUTS</span></span>

### <span data-ttu-id="9e6e1-127">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="9e6e1-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="9e6e1-128">Note</span><span class="sxs-lookup"><span data-stu-id="9e6e1-128">NOTES</span></span>

## <span data-ttu-id="9e6e1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e6e1-129">RELATED LINKS</span></span>

[<span data-ttu-id="9e6e1-130">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9e6e1-130">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="9e6e1-131">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9e6e1-131">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="9e6e1-132">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="9e6e1-132">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


