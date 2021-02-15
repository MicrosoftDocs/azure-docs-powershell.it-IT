---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182119"
---
# <span data-ttu-id="3ba91-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="3ba91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ba91-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba91-103">Modifica un runbook.</span><span class="sxs-lookup"><span data-stu-id="3ba91-103">Modifies a runbook.</span></span>

## <span data-ttu-id="3ba91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ba91-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ba91-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ba91-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba91-106">Il cmdlet **Set-AzAutomationRunbook** modifica la configurazione di un runbook di automazione di Azure in APS.</span><span class="sxs-lookup"><span data-stu-id="3ba91-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="3ba91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ba91-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba91-108">Esempio 1: Abilitare la registrazione dettagliata per un runbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3ba91-109">Questo comando abilita la registrazione dettagliata per i processi del runbook specificato nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3ba91-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3ba91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ba91-110">PARAMETERS</span></span>

### <span data-ttu-id="3ba91-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ba91-111">-AutomationAccountName</span></span>
<span data-ttu-id="3ba91-112">Specifica il nome dell'account di automazione in cui questo cmdlet modifica un runbook.</span><span class="sxs-lookup"><span data-stu-id="3ba91-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="3ba91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba91-113">-DefaultProfile</span></span>
<span data-ttu-id="3ba91-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3ba91-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ba91-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ba91-115">-Description</span></span>
<span data-ttu-id="3ba91-116">Specifica una descrizione per il runbook.</span><span class="sxs-lookup"><span data-stu-id="3ba91-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="3ba91-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="3ba91-117">-LogProgress</span></span>
<span data-ttu-id="3ba91-118">Specifica se il runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="3ba91-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="3ba91-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3ba91-119">-LogVerbose</span></span>
<span data-ttu-id="3ba91-120">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="3ba91-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="3ba91-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3ba91-121">-Name</span></span>
<span data-ttu-id="3ba91-122">Specifica il nome del runbook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ba91-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3ba91-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ba91-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ba91-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un runbook.</span><span class="sxs-lookup"><span data-stu-id="3ba91-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="3ba91-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ba91-125">-Tag</span></span>
<span data-ttu-id="3ba91-126">I tag del runbook.</span><span class="sxs-lookup"><span data-stu-id="3ba91-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba91-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba91-127">CommonParameters</span></span>
<span data-ttu-id="3ba91-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ba91-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba91-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba91-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba91-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ba91-130">INPUTS</span></span>

### <span data-ttu-id="3ba91-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3ba91-131">System.String</span></span>

### <span data-ttu-id="3ba91-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="3ba91-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="3ba91-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ba91-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3ba91-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ba91-134">OUTPUTS</span></span>

### <span data-ttu-id="3ba91-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="3ba91-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ba91-136">NOTES</span></span>

## <span data-ttu-id="3ba91-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ba91-137">RELATED LINKS</span></span>

[<span data-ttu-id="3ba91-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="3ba91-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3ba91-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


