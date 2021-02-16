---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199654"
---
# <span data-ttu-id="f74d7-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="f74d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f74d7-103">Ottiene un runbook.</span><span class="sxs-lookup"><span data-stu-id="f74d7-103">Gets a runbook.</span></span>

## <span data-ttu-id="f74d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f74d7-104">SYNTAX</span></span>

### <span data-ttu-id="f74d7-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f74d7-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f74d7-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="f74d7-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f74d7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f74d7-107">DESCRIPTION</span></span>
<span data-ttu-id="f74d7-108">Il cmdlet **Get-AzAutomationRunbook** ottiene i runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f74d7-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="f74d7-109">Per ottenere un runbook specifico, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="f74d7-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="f74d7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f74d7-110">EXAMPLES</span></span>

### <span data-ttu-id="f74d7-111">Esempio 1: Ottenere tutti i runbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f74d7-112">Questo comando recupera tutti i runbook nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f74d7-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f74d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f74d7-113">PARAMETERS</span></span>

### <span data-ttu-id="f74d7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f74d7-114">-AutomationAccountName</span></span>
<span data-ttu-id="f74d7-115">Specifica il nome di un account di automazione in cui questo cmdlet ottiene runbook.</span><span class="sxs-lookup"><span data-stu-id="f74d7-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="f74d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74d7-116">-DefaultProfile</span></span>
<span data-ttu-id="f74d7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f74d7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f74d7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f74d7-118">-Name</span></span>
<span data-ttu-id="f74d7-119">Specifica il nome di un runbook che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f74d7-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="f74d7-121">Specifica il nome del gruppo di risorse per cui il cmdlet ottiene i runbook.</span><span class="sxs-lookup"><span data-stu-id="f74d7-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="f74d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74d7-122">CommonParameters</span></span>
<span data-ttu-id="f74d7-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74d7-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74d7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74d7-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="f74d7-125">INPUTS</span></span>

### <span data-ttu-id="f74d7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f74d7-126">System.String</span></span>

## <span data-ttu-id="f74d7-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f74d7-127">OUTPUTS</span></span>

### <span data-ttu-id="f74d7-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f74d7-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="f74d7-129">NOTES</span></span>

## <span data-ttu-id="f74d7-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f74d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="f74d7-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="f74d7-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f74d7-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


