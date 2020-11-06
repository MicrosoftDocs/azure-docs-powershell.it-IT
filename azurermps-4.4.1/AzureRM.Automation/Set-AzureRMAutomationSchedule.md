---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 03763ad7c2212eb89650749eb6d407d9ce973693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511364"
---
# <span data-ttu-id="0eaed-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0eaed-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="0eaed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0eaed-102">SYNOPSIS</span></span>
<span data-ttu-id="0eaed-103">Modifica una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="0eaed-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eaed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eaed-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eaed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eaed-105">DESCRIPTION</span></span>
<span data-ttu-id="0eaed-106">Il cmdlet **set-AzureRmAutomationSchedule** modifica una programmazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0eaed-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="0eaed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eaed-107">EXAMPLES</span></span>

### <span data-ttu-id="0eaed-108">Esempio 1: modificare una programmazione</span><span class="sxs-lookup"><span data-stu-id="0eaed-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0eaed-109">Questo comando modifica la descrizione della programmazione denominata Schedule01.</span><span class="sxs-lookup"><span data-stu-id="0eaed-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="0eaed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0eaed-110">PARAMETERS</span></span>

### <span data-ttu-id="0eaed-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0eaed-111">-AutomationAccountName</span></span>
<span data-ttu-id="0eaed-112">Specifica il nome di un account di automazione per cui questo cmdlet modifica una programmazione.</span><span class="sxs-lookup"><span data-stu-id="0eaed-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="0eaed-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eaed-113">-Description</span></span>
<span data-ttu-id="0eaed-114">Specifica una descrizione per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0eaed-114">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="0eaed-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="0eaed-115">-IsEnabled</span></span>
<span data-ttu-id="0eaed-116">Specifica se questo cmdlet Abilita la programmazione.</span><span class="sxs-lookup"><span data-stu-id="0eaed-116">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="0eaed-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0eaed-117">-Name</span></span>
<span data-ttu-id="0eaed-118">Specifica il nome della pianificazione modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eaed-118">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0eaed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eaed-119">-ResourceGroupName</span></span>
<span data-ttu-id="0eaed-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet modifica una programmazione.</span><span class="sxs-lookup"><span data-stu-id="0eaed-120">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="0eaed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eaed-121">-DefaultProfile</span></span>
<span data-ttu-id="0eaed-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0eaed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eaed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eaed-123">CommonParameters</span></span>
<span data-ttu-id="0eaed-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eaed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eaed-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eaed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eaed-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0eaed-126">INPUTS</span></span>

## <span data-ttu-id="0eaed-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eaed-127">OUTPUTS</span></span>

### <span data-ttu-id="0eaed-128">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="0eaed-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="0eaed-129">Note</span><span class="sxs-lookup"><span data-stu-id="0eaed-129">NOTES</span></span>

## <span data-ttu-id="0eaed-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eaed-130">RELATED LINKS</span></span>

[<span data-ttu-id="0eaed-131">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0eaed-131">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="0eaed-132">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0eaed-132">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="0eaed-133">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0eaed-133">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

