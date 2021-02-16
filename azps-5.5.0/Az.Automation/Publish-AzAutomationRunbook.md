---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177974"
---
# <span data-ttu-id="79789-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="79789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79789-102">SYNOPSIS</span></span>
<span data-ttu-id="79789-103">Pubblica un runbook.</span><span class="sxs-lookup"><span data-stu-id="79789-103">Publishes a runbook.</span></span>

## <span data-ttu-id="79789-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79789-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79789-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79789-105">DESCRIPTION</span></span>
<span data-ttu-id="79789-106">Il cmdlet **Publish-AzAutomationRunbook** pubblica un runbook da usare nell'ambiente di produzione di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="79789-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="79789-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79789-107">EXAMPLES</span></span>

### <span data-ttu-id="79789-108">Esempio 1: Pubblicare un runbook</span><span class="sxs-lookup"><span data-stu-id="79789-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="79789-109">Questo comando pubblica il runbook denominato Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="79789-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="79789-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79789-110">PARAMETERS</span></span>

### <span data-ttu-id="79789-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="79789-111">-AutomationAccountName</span></span>
<span data-ttu-id="79789-112">Specifica il nome dell'account di automazione in cui questo cmdlet pubblica un runbook.</span><span class="sxs-lookup"><span data-stu-id="79789-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="79789-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79789-113">-DefaultProfile</span></span>
<span data-ttu-id="79789-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="79789-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79789-115">-Name</span><span class="sxs-lookup"><span data-stu-id="79789-115">-Name</span></span>
<span data-ttu-id="79789-116">Specifica il nome del runbook pubblicato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79789-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79789-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79789-117">-ResourceGroupName</span></span>
<span data-ttu-id="79789-118">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un runbook.</span><span class="sxs-lookup"><span data-stu-id="79789-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="79789-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79789-119">CommonParameters</span></span>
<span data-ttu-id="79789-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79789-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79789-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79789-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79789-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="79789-122">INPUTS</span></span>

### <span data-ttu-id="79789-123">System.String</span><span class="sxs-lookup"><span data-stu-id="79789-123">System.String</span></span>

## <span data-ttu-id="79789-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79789-124">OUTPUTS</span></span>

### <span data-ttu-id="79789-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="79789-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="79789-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="79789-126">NOTES</span></span>

## <span data-ttu-id="79789-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79789-127">RELATED LINKS</span></span>

[<span data-ttu-id="79789-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="79789-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="79789-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="79789-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="79789-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="79789-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="79789-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="79789-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79789-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


