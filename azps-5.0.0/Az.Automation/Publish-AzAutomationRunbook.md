---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299761"
---
# <span data-ttu-id="ab9a8-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="ab9a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9a8-103">Pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-103">Publishes a runbook.</span></span>

## <span data-ttu-id="ab9a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab9a8-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab9a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab9a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9a8-106">Il cmdlet **Publish-AzAutomationRunbook** pubblica un Runbook per l'uso nell'ambiente di produzione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="ab9a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab9a8-107">EXAMPLES</span></span>

### <span data-ttu-id="ab9a8-108">Esempio 1: pubblicare un Runbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ab9a8-109">Questo comando pubblica il Runbook denominato Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ab9a8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab9a8-110">PARAMETERS</span></span>

### <span data-ttu-id="ab9a8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab9a8-111">-AutomationAccountName</span></span>
<span data-ttu-id="ab9a8-112">Specifica il nome dell'account di automazione in cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="ab9a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab9a8-113">-DefaultProfile</span></span>
<span data-ttu-id="ab9a8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab9a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab9a8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab9a8-115">-Name</span></span>
<span data-ttu-id="ab9a8-116">Specifica il nome del Runbook che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="ab9a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab9a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab9a8-118">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="ab9a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9a8-119">CommonParameters</span></span>
<span data-ttu-id="ab9a8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab9a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9a8-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab9a8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9a8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab9a8-122">INPUTS</span></span>

### <span data-ttu-id="ab9a8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ab9a8-123">System.String</span></span>

## <span data-ttu-id="ab9a8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab9a8-124">OUTPUTS</span></span>

### <span data-ttu-id="ab9a8-125">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ab9a8-126">Note</span><span class="sxs-lookup"><span data-stu-id="ab9a8-126">NOTES</span></span>

## <span data-ttu-id="ab9a8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab9a8-127">RELATED LINKS</span></span>

[<span data-ttu-id="ab9a8-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="ab9a8-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ab9a8-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


