---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201121"
---
# <span data-ttu-id="a7737-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a7737-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="a7737-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7737-102">SYNOPSIS</span></span>
<span data-ttu-id="a7737-103">Modifica una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="a7737-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="a7737-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7737-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7737-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7737-105">DESCRIPTION</span></span>
<span data-ttu-id="a7737-106">Il cmdlet **set-AzAutomationSchedule** modifica una programmazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a7737-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="a7737-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7737-107">EXAMPLES</span></span>

### <span data-ttu-id="a7737-108">Esempio 1: modificare una programmazione</span><span class="sxs-lookup"><span data-stu-id="a7737-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a7737-109">Questo comando modifica la descrizione della programmazione denominata Schedule01.</span><span class="sxs-lookup"><span data-stu-id="a7737-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="a7737-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7737-110">PARAMETERS</span></span>

### <span data-ttu-id="a7737-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7737-111">-AutomationAccountName</span></span>
<span data-ttu-id="a7737-112">Specifica il nome di un account di automazione per cui questo cmdlet modifica una programmazione.</span><span class="sxs-lookup"><span data-stu-id="a7737-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a7737-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7737-113">-DefaultProfile</span></span>
<span data-ttu-id="a7737-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a7737-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7737-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7737-115">-Description</span></span>
<span data-ttu-id="a7737-116">Specifica una descrizione per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="a7737-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7737-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a7737-117">-IsEnabled</span></span>
<span data-ttu-id="a7737-118">Specifica se questo cmdlet Abilita la programmazione.</span><span class="sxs-lookup"><span data-stu-id="a7737-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7737-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7737-119">-Name</span></span>
<span data-ttu-id="a7737-120">Specifica il nome della pianificazione modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7737-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7737-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7737-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7737-122">Specifica il nome di un gruppo di risorse per cui questo cmdlet modifica una programmazione.</span><span class="sxs-lookup"><span data-stu-id="a7737-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a7737-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7737-123">CommonParameters</span></span>
<span data-ttu-id="a7737-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7737-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7737-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7737-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7737-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7737-126">INPUTS</span></span>

### <span data-ttu-id="a7737-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a7737-127">System.String</span></span>

### <span data-ttu-id="a7737-128">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a7737-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a7737-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7737-129">OUTPUTS</span></span>

### <span data-ttu-id="a7737-130">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="a7737-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="a7737-131">Note</span><span class="sxs-lookup"><span data-stu-id="a7737-131">NOTES</span></span>

## <span data-ttu-id="a7737-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7737-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7737-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a7737-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="a7737-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a7737-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="a7737-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a7737-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


