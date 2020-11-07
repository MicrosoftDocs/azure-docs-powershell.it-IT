---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: e043496f421ec6602fea61018cbaa254192def10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685039"
---
# <span data-ttu-id="bf3b2-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="bf3b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf3b2-103">Importa un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="bf3b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf3b2-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf3b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf3b2-105">DESCRIPTION</span></span>
<span data-ttu-id="bf3b2-106">Il cmdlet **Import-AzAutomationRunbook** importa un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="bf3b2-107">Specificare il percorso di un file di script wps_2 (. ps1) da importare per wps_2 e wps_2 flusso di lavoro manuali operativi, (. graphrunbook) file per manuali operativi grafico o (. py) file per Python 2 manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="bf3b2-108">Per wps_2 flusso di lavoro manuali operativi, lo script deve contenere una singola definizione di flusso di lavoro wps_2 che corrisponda al nome del file.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="bf3b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf3b2-109">EXAMPLES</span></span>

### <span data-ttu-id="bf3b2-110">Esempio 1: importare un Runbook da un file</span><span class="sxs-lookup"><span data-stu-id="bf3b2-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="bf3b2-111">Il primo comando assegna due coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="bf3b2-112">Con il secondo comando viene importata una Runbook grafica denominata GraphicalRunbook06 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="bf3b2-113">Il comando assegna anche i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="bf3b2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf3b2-114">PARAMETERS</span></span>

### <span data-ttu-id="bf3b2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf3b2-115">-AutomationAccountName</span></span>
<span data-ttu-id="bf3b2-116">Specifica il nome dell'account di automazione in cui questo cmdlet importa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="bf3b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf3b2-117">-DefaultProfile</span></span>
<span data-ttu-id="bf3b2-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bf3b2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf3b2-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf3b2-119">-Description</span></span>
<span data-ttu-id="bf3b2-120">Specifica una descrizione per il Runbook importato.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="bf3b2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bf3b2-121">-Force</span></span>
<span data-ttu-id="bf3b2-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="bf3b2-122">ps_force</span></span>

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

### <span data-ttu-id="bf3b2-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="bf3b2-123">-LogProgress</span></span>
<span data-ttu-id="bf3b2-124">Specifica se Runbook registra le informazioni sull'avanzamento.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="bf3b2-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="bf3b2-125">-LogVerbose</span></span>
<span data-ttu-id="bf3b2-126">Specifica se Runbook registra informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="bf3b2-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf3b2-127">-Name</span></span>
<span data-ttu-id="bf3b2-128">Specifica il nome del Runbook importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b2-129">-Path</span><span class="sxs-lookup"><span data-stu-id="bf3b2-129">-Path</span></span>
<span data-ttu-id="bf3b2-130">Specifica il percorso di un file con estensione ps1 o graphrunbook che questo cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b2-131">-Pubblicato</span><span class="sxs-lookup"><span data-stu-id="bf3b2-131">-Published</span></span>
<span data-ttu-id="bf3b2-132">Indica che questo cmdlet pubblica il Runbook importato.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="bf3b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf3b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="bf3b2-134">Specifica il nome del gruppo di risorse per cui questo cmdlet importa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="bf3b2-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf3b2-135">-Tags</span></span>
<span data-ttu-id="bf3b2-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bf3b2-137">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bf3b2-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b2-138">-Digitare</span><span class="sxs-lookup"><span data-stu-id="bf3b2-138">-Type</span></span>
<span data-ttu-id="bf3b2-139">Specifica il tipo di Runbook creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="bf3b2-140">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bf3b2-140">Valid values are:</span></span>
- <span data-ttu-id="bf3b2-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf3b2-141">PowerShell</span></span>
- <span data-ttu-id="bf3b2-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="bf3b2-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="bf3b2-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bf3b2-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="bf3b2-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bf3b2-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="bf3b2-145">Grafico</span><span class="sxs-lookup"><span data-stu-id="bf3b2-145">Graph</span></span>
- <span data-ttu-id="bf3b2-146">Python2 il valore grafico è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="bf3b2-147">Equivale a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf3b2-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bf3b2-148">-Confirm</span></span>
<span data-ttu-id="bf3b2-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf3b2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf3b2-150">-WhatIf</span></span>
<span data-ttu-id="bf3b2-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf3b2-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf3b2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf3b2-153">CommonParameters</span></span>
<span data-ttu-id="bf3b2-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf3b2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf3b2-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf3b2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf3b2-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf3b2-156">INPUTS</span></span>

### <span data-ttu-id="bf3b2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bf3b2-157">System.String</span></span>

### <span data-ttu-id="bf3b2-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bf3b2-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="bf3b2-159">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bf3b2-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bf3b2-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf3b2-160">OUTPUTS</span></span>

### <span data-ttu-id="bf3b2-161">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="bf3b2-162">Note</span><span class="sxs-lookup"><span data-stu-id="bf3b2-162">NOTES</span></span>

## <span data-ttu-id="bf3b2-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf3b2-163">RELATED LINKS</span></span>

[<span data-ttu-id="bf3b2-164">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-166">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-167">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-167">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-168">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-168">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-169">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-169">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-170">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-170">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="bf3b2-171">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bf3b2-171">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
