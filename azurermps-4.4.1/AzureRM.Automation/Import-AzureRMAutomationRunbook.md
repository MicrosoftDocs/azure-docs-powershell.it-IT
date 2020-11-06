---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517128"
---
# <span data-ttu-id="83b85-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="83b85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b85-102">SYNOPSIS</span></span>
<span data-ttu-id="83b85-103">Importa un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="83b85-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b85-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b85-105">DESCRIPTION</span></span>
<span data-ttu-id="83b85-106">Il cmdlet **Import-AzureRmAutomationRunbook** importa un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83b85-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="83b85-107">Specificare il percorso di un file di script wps_2 (con estensione ps1) da importare per wps_2 e wps_2 flusso di lavoro manuali operativi o in un file Runbook (graphrunbook) grafico per la manuali operativi grafica.</span><span class="sxs-lookup"><span data-stu-id="83b85-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="83b85-108">Il nome del file diventa il nome del Runbook.</span><span class="sxs-lookup"><span data-stu-id="83b85-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="83b85-109">Per wps_2 flusso di lavoro manuali operativi, lo script deve contenere una singola definizione di flusso di lavoro wps_2 che corrisponda al nome del file.</span><span class="sxs-lookup"><span data-stu-id="83b85-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="83b85-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b85-110">EXAMPLES</span></span>

### <span data-ttu-id="83b85-111">Esempio 1: importare un Runbook da un file</span><span class="sxs-lookup"><span data-stu-id="83b85-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="83b85-112">Il primo comando assegna due coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="83b85-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="83b85-113">Con il secondo comando viene importata una Runbook grafica denominata GraphicalRunbook06 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="83b85-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="83b85-114">Il comando assegna anche i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="83b85-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="83b85-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b85-115">PARAMETERS</span></span>

### <span data-ttu-id="83b85-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="83b85-116">-AutomationAccountName</span></span>
<span data-ttu-id="83b85-117">Specifica il nome dell'account di automazione in cui questo cmdlet importa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="83b85-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="83b85-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b85-118">-Description</span></span>
<span data-ttu-id="83b85-119">Specifica una descrizione per il Runbook importato.</span><span class="sxs-lookup"><span data-stu-id="83b85-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="83b85-120">-Force</span><span class="sxs-lookup"><span data-stu-id="83b85-120">-Force</span></span>
<span data-ttu-id="83b85-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="83b85-121">ps_force</span></span>

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

### <span data-ttu-id="83b85-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="83b85-122">-LogProgress</span></span>
<span data-ttu-id="83b85-123">Specifica se Runbook registra le informazioni sull'avanzamento.</span><span class="sxs-lookup"><span data-stu-id="83b85-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="83b85-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="83b85-124">-LogVerbose</span></span>
<span data-ttu-id="83b85-125">Specifica se Runbook registra informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="83b85-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="83b85-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="83b85-126">-Name</span></span>
<span data-ttu-id="83b85-127">Specifica il nome del Runbook importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b85-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="83b85-128">-Path</span><span class="sxs-lookup"><span data-stu-id="83b85-128">-Path</span></span>
<span data-ttu-id="83b85-129">Specifica il percorso di un file con estensione ps1 o graphrunbook che questo cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="83b85-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="83b85-130">-Pubblicato</span><span class="sxs-lookup"><span data-stu-id="83b85-130">-Published</span></span>
<span data-ttu-id="83b85-131">Indica che questo cmdlet pubblica il Runbook importato.</span><span class="sxs-lookup"><span data-stu-id="83b85-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="83b85-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b85-132">-ResourceGroupName</span></span>
<span data-ttu-id="83b85-133">Specifica il nome del gruppo di risorse per cui questo cmdlet importa un Runbook.</span><span class="sxs-lookup"><span data-stu-id="83b85-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="83b85-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="83b85-134">-Tags</span></span>
<span data-ttu-id="83b85-135">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83b85-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="83b85-136">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="83b85-136">For example:</span></span>

<span data-ttu-id="83b85-137">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="83b85-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="83b85-138">-Digitare</span><span class="sxs-lookup"><span data-stu-id="83b85-138">-Type</span></span>
<span data-ttu-id="83b85-139">Specifica il tipo di Runbook creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b85-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="83b85-140">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="83b85-140">Valid values are:</span></span>

- <span data-ttu-id="83b85-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="83b85-141">PowerShell</span></span>
- <span data-ttu-id="83b85-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="83b85-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="83b85-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="83b85-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="83b85-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="83b85-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="83b85-145">Grafico</span><span class="sxs-lookup"><span data-stu-id="83b85-145">Graph</span></span>

<span data-ttu-id="83b85-146">Il grafico del valore è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="83b85-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="83b85-147">Equivale a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="83b85-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b85-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83b85-148">-Confirm</span></span>
<span data-ttu-id="83b85-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b85-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b85-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b85-150">-WhatIf</span></span>
<span data-ttu-id="83b85-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b85-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b85-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b85-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b85-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b85-153">-DefaultProfile</span></span>
<span data-ttu-id="83b85-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83b85-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83b85-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b85-155">CommonParameters</span></span>
<span data-ttu-id="83b85-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b85-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b85-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b85-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b85-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b85-158">INPUTS</span></span>

## <span data-ttu-id="83b85-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b85-159">OUTPUTS</span></span>

### <span data-ttu-id="83b85-160">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="83b85-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="83b85-161">Note</span><span class="sxs-lookup"><span data-stu-id="83b85-161">NOTES</span></span>

## <span data-ttu-id="83b85-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b85-162">RELATED LINKS</span></span>

[<span data-ttu-id="83b85-163">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-165">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-166">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-167">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="83b85-170">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="83b85-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
