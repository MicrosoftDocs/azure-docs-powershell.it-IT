---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 38e993068bec6e4a2fd8e627ed7201fb0f966633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014317"
---
# <span data-ttu-id="1bf20-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="1bf20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf20-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf20-103">Esporta un runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="1bf20-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="1bf20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bf20-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf20-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1bf20-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf20-106">Il cmdlet **Export-AzAutomationRunbook** esporta un runbook di automazione di Azure in un file di script di wps_2 (ps1), per runbook di wps_2 o flusso di lavoro di wps_2 oppure in un file di runbook grafico (con estensione graphrunbook) per runbook grafici.</span><span class="sxs-lookup"><span data-stu-id="1bf20-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="1bf20-107">Il nome del runbook diventa il nome del file esportato.</span><span class="sxs-lookup"><span data-stu-id="1bf20-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="1bf20-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bf20-108">EXAMPLES</span></span>

### <span data-ttu-id="1bf20-109">Esempio 1: Esportare un runbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1bf20-110">Questo comando esporta la versione pubblicata di un runbook di automazione in un desktop utente.</span><span class="sxs-lookup"><span data-stu-id="1bf20-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="1bf20-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf20-111">PARAMETERS</span></span>

### <span data-ttu-id="1bf20-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1bf20-112">-AutomationAccountName</span></span>
<span data-ttu-id="1bf20-113">Specifica il nome dell'account di automazione in cui questo cmdlet esporta un runbook.</span><span class="sxs-lookup"><span data-stu-id="1bf20-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="1bf20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf20-114">-DefaultProfile</span></span>
<span data-ttu-id="1bf20-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1bf20-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bf20-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1bf20-116">-Force</span></span>
<span data-ttu-id="1bf20-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="1bf20-117">ps_force</span></span>

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

### <span data-ttu-id="1bf20-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf20-118">-Name</span></span>
<span data-ttu-id="1bf20-119">Specifica il nome del runbook esportato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf20-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="1bf20-120">Il nome del runbook diventa il nome del file di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1bf20-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="1bf20-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1bf20-121">-OutputFolder</span></span>
<span data-ttu-id="1bf20-122">Specifica il percorso di una cartella in cui questo cmdlet crea il file di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1bf20-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="1bf20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf20-123">-ResourceGroupName</span></span>
<span data-ttu-id="1bf20-124">Specifica il nome del gruppo di risorse per cui il cmdlet esporta un runbook.</span><span class="sxs-lookup"><span data-stu-id="1bf20-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="1bf20-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="1bf20-125">-Slot</span></span>
<span data-ttu-id="1bf20-126">Specifica se questo cmdlet esporta la bozza o il contenuto pubblicato del runbook.</span><span class="sxs-lookup"><span data-stu-id="1bf20-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="1bf20-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1bf20-127">Valid values are:</span></span> 
- <span data-ttu-id="1bf20-128">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="1bf20-128">Published</span></span> 
- <span data-ttu-id="1bf20-129">Bozza</span><span class="sxs-lookup"><span data-stu-id="1bf20-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf20-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bf20-130">-Confirm</span></span>
<span data-ttu-id="1bf20-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bf20-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf20-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf20-132">-WhatIf</span></span>
<span data-ttu-id="1bf20-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf20-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf20-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bf20-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf20-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf20-135">CommonParameters</span></span>
<span data-ttu-id="1bf20-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf20-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf20-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf20-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf20-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="1bf20-138">INPUTS</span></span>

### <span data-ttu-id="1bf20-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf20-139">System.String</span></span>

## <span data-ttu-id="1bf20-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bf20-140">OUTPUTS</span></span>

### <span data-ttu-id="1bf20-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1bf20-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1bf20-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="1bf20-142">NOTES</span></span>

## <span data-ttu-id="1bf20-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bf20-143">RELATED LINKS</span></span>

[<span data-ttu-id="1bf20-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="1bf20-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1bf20-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


