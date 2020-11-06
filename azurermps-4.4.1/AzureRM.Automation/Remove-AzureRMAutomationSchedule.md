---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518387"
---
# <span data-ttu-id="71c2f-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71c2f-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="71c2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="71c2f-103">Elimina una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="71c2f-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71c2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71c2f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71c2f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="71c2f-106">Il cmdlet **Remove-AzureRmAutomationSchedule** Elimina una programmazione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="71c2f-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="71c2f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71c2f-107">EXAMPLES</span></span>

### <span data-ttu-id="71c2f-108">Esempio 1: rimuovere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="71c2f-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71c2f-109">Questo comando modifica la descrizione della programmazione denominata Schedule01.</span><span class="sxs-lookup"><span data-stu-id="71c2f-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="71c2f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="71c2f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71c2f-111">-AutomationAccountName</span></span>
<span data-ttu-id="71c2f-112">Specifica il nome di un account di automazione per cui questo cmdlet modifica una programmazione.</span><span class="sxs-lookup"><span data-stu-id="71c2f-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="71c2f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="71c2f-113">-Force</span></span>
<span data-ttu-id="71c2f-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="71c2f-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c2f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="71c2f-115">-Name</span></span>
<span data-ttu-id="71c2f-116">Specifica il nome per la pianificazione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c2f-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71c2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="71c2f-118">Specifica il nome di un gruppo di risorse per cui questo cmdlet rimuove una programmazione.</span><span class="sxs-lookup"><span data-stu-id="71c2f-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="71c2f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71c2f-119">-Confirm</span></span>
<span data-ttu-id="71c2f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c2f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71c2f-121">-WhatIf</span></span>
<span data-ttu-id="71c2f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71c2f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71c2f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71c2f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71c2f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c2f-124">-DefaultProfile</span></span>
<span data-ttu-id="71c2f-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71c2f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c2f-126">CommonParameters</span></span>
<span data-ttu-id="71c2f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c2f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c2f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71c2f-129">INPUTS</span></span>

## <span data-ttu-id="71c2f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71c2f-130">OUTPUTS</span></span>

## <span data-ttu-id="71c2f-131">Note</span><span class="sxs-lookup"><span data-stu-id="71c2f-131">NOTES</span></span>

## <span data-ttu-id="71c2f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71c2f-132">RELATED LINKS</span></span>

[<span data-ttu-id="71c2f-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71c2f-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="71c2f-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71c2f-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="71c2f-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="71c2f-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


