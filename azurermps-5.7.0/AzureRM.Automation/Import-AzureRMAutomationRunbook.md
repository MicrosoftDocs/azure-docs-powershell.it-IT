---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508408"
---
# <span data-ttu-id="5bb9c-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="5bb9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5bb9c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb9c-103">Importa un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bb9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bb9c-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bb9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bb9c-105">DESCRIPTION</span></span>
<span data-ttu-id="5bb9c-106">Il cmdlet **Import-AzureRmAutomationRunbook** importa un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="5bb9c-107">Specificare il percorso di un file di script wps_2 (. ps1) da importare per wps_2 e wps_2 flusso di lavoro manuali operativi, (. graphrunbook) file per manuali operativi grafico o (. py) file per Python 2 manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="5bb9c-108">Per wps_2 flusso di lavoro manuali operativi, lo script deve contenere una singola definizione di flusso di lavoro wps_2 che corrisponda al nome del file.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="5bb9c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bb9c-109">EXAMPLES</span></span>

### <span data-ttu-id="5bb9c-110">Esempio 1: importare un Runbook da un file</span><span class="sxs-lookup"><span data-stu-id="5bb9c-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="5bb9c-111">Il primo comando assegna due coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="5bb9c-112">Con il secondo comando viene importata una Runbook grafica denominata GraphicalRunbook06 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5bb9c-113">Il comando assegna anche i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="5bb9c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5bb9c-114">PARAMETERS</span></span>

### <span data-ttu-id="5bb9c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5bb9c-115">-AutomationAccountName</span></span>
<span data-ttu-id="5bb9c-116">Specifica il nome dell'account di automazione in cui questo cmdlet importa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb9c-117">-DefaultProfile</span></span>
<span data-ttu-id="5bb9c-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5bb9c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bb9c-119">-Description</span></span>
<span data-ttu-id="5bb9c-120">Specifica una descrizione per il Runbook importato.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5bb9c-121">-Force</span></span>
<span data-ttu-id="5bb9c-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="5bb9c-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="5bb9c-123">-LogProgress</span></span>
<span data-ttu-id="5bb9c-124">Specifica se Runbook registra le informazioni sull'avanzamento.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="5bb9c-125">-LogVerbose</span></span>
<span data-ttu-id="5bb9c-126">Specifica se Runbook registra informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bb9c-127">-Name</span></span>
<span data-ttu-id="5bb9c-128">Specifica il nome del Runbook importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5bb9c-129">-Path</span></span>
<span data-ttu-id="5bb9c-130">Specifica il percorso di un file con estensione ps1 o graphrunbook che questo cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-131">-Pubblicato</span><span class="sxs-lookup"><span data-stu-id="5bb9c-131">-Published</span></span>
<span data-ttu-id="5bb9c-132">Indica che questo cmdlet pubblica il Runbook importato.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb9c-133">-ResourceGroupName</span></span>
<span data-ttu-id="5bb9c-134">Specifica il nome del gruppo di risorse per cui questo cmdlet importa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bb9c-135">-Tags</span></span>
<span data-ttu-id="5bb9c-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5bb9c-137">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="5bb9c-137">For example:</span></span>

<span data-ttu-id="5bb9c-138">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5bb9c-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-139">-Digitare</span><span class="sxs-lookup"><span data-stu-id="5bb9c-139">-Type</span></span>
<span data-ttu-id="5bb9c-140">Specifica il tipo di Runbook creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="5bb9c-141">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5bb9c-141">Valid values are:</span></span>

- <span data-ttu-id="5bb9c-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5bb9c-142">PowerShell</span></span>
- <span data-ttu-id="5bb9c-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="5bb9c-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="5bb9c-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="5bb9c-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="5bb9c-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="5bb9c-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="5bb9c-146">Grafico</span><span class="sxs-lookup"><span data-stu-id="5bb9c-146">Graph</span></span>
- <span data-ttu-id="5bb9c-147">Python2</span><span class="sxs-lookup"><span data-stu-id="5bb9c-147">Python2</span></span>

<span data-ttu-id="5bb9c-148">Il grafico del valore è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="5bb9c-149">Equivale a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5bb9c-150">-Confirm</span></span>
<span data-ttu-id="5bb9c-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb9c-152">-WhatIf</span></span>
<span data-ttu-id="5bb9c-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bb9c-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb9c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb9c-155">CommonParameters</span></span>
<span data-ttu-id="5bb9c-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb9c-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bb9c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb9c-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5bb9c-158">INPUTS</span></span>

### <span data-ttu-id="5bb9c-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5bb9c-159">None</span></span>
<span data-ttu-id="5bb9c-160">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5bb9c-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bb9c-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bb9c-161">OUTPUTS</span></span>

### <span data-ttu-id="5bb9c-162">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="5bb9c-163">Note</span><span class="sxs-lookup"><span data-stu-id="5bb9c-163">NOTES</span></span>

## <span data-ttu-id="5bb9c-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bb9c-164">RELATED LINKS</span></span>

[<span data-ttu-id="5bb9c-165">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-167">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-168">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-169">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5bb9c-172">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5bb9c-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
