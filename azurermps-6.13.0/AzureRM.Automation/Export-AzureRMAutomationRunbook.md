---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: f982c68c49d6a8a92bb06bf150e352626730f67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513971"
---
# <span data-ttu-id="18153-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="18153-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18153-102">SYNOPSIS</span></span>
<span data-ttu-id="18153-103">Esporta un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="18153-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18153-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18153-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18153-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18153-105">DESCRIPTION</span></span>
<span data-ttu-id="18153-106">Il cmdlet **Export-AzureRmAutomationRunbook** esporta un Runbook di automazione di Azure in un file di script wps_2 (. ps1), per wps_2 o wps_2 flusso di lavoro manuali operativi o in un file Runbook (graphrunbook) grafico, per la manuali operativi grafica.</span><span class="sxs-lookup"><span data-stu-id="18153-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="18153-107">Il nome del Runbook diventa il nome del file esportato.</span><span class="sxs-lookup"><span data-stu-id="18153-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="18153-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18153-108">EXAMPLES</span></span>

### <span data-ttu-id="18153-109">Esempio 1: esportare un Runbook</span><span class="sxs-lookup"><span data-stu-id="18153-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="18153-110">Questo comando Esporta la versione pubblicata di un Runbook di automazione in un desktop utente.</span><span class="sxs-lookup"><span data-stu-id="18153-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="18153-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18153-111">PARAMETERS</span></span>

### <span data-ttu-id="18153-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="18153-112">-AutomationAccountName</span></span>
<span data-ttu-id="18153-113">Specifica il nome dell'account di automazione in cui questo cmdlet esporta un Runbook.</span><span class="sxs-lookup"><span data-stu-id="18153-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="18153-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18153-114">-DefaultProfile</span></span>
<span data-ttu-id="18153-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="18153-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18153-116">-Force</span><span class="sxs-lookup"><span data-stu-id="18153-116">-Force</span></span>
<span data-ttu-id="18153-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="18153-117">ps_force</span></span>

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

### <span data-ttu-id="18153-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="18153-118">-Name</span></span>
<span data-ttu-id="18153-119">Specifica il nome del Runbook che questo cmdlet Esporta.</span><span class="sxs-lookup"><span data-stu-id="18153-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="18153-120">Il nome del Runbook diventa il nome del file di esportazione.</span><span class="sxs-lookup"><span data-stu-id="18153-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="18153-121">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="18153-121">-OutputFolder</span></span>
<span data-ttu-id="18153-122">Specifica il percorso di una cartella in cui questo cmdlet crea il file di esportazione.</span><span class="sxs-lookup"><span data-stu-id="18153-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="18153-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18153-123">-ResourceGroupName</span></span>
<span data-ttu-id="18153-124">Specifica il nome del gruppo di risorse per cui questo cmdlet esporta un Runbook.</span><span class="sxs-lookup"><span data-stu-id="18153-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="18153-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="18153-125">-Slot</span></span>
<span data-ttu-id="18153-126">Specifica se questo cmdlet Esporta la bozza o il contenuto pubblicato di Runbook.</span><span class="sxs-lookup"><span data-stu-id="18153-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="18153-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="18153-127">Valid values are:</span></span> 
- <span data-ttu-id="18153-128">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="18153-128">Published</span></span> 
- <span data-ttu-id="18153-129">Progetto</span><span class="sxs-lookup"><span data-stu-id="18153-129">Draft</span></span>

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

### <span data-ttu-id="18153-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18153-130">-Confirm</span></span>
<span data-ttu-id="18153-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18153-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18153-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18153-132">-WhatIf</span></span>
<span data-ttu-id="18153-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18153-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18153-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18153-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18153-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18153-135">CommonParameters</span></span>
<span data-ttu-id="18153-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18153-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18153-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18153-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18153-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18153-138">INPUTS</span></span>

### <span data-ttu-id="18153-139">System. String</span><span class="sxs-lookup"><span data-stu-id="18153-139">System.String</span></span>

## <span data-ttu-id="18153-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18153-140">OUTPUTS</span></span>

### <span data-ttu-id="18153-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="18153-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="18153-142">Note</span><span class="sxs-lookup"><span data-stu-id="18153-142">NOTES</span></span>

## <span data-ttu-id="18153-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18153-143">RELATED LINKS</span></span>

[<span data-ttu-id="18153-144">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-144">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-145">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-145">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-146">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-147">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-148">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-148">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-149">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-149">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-150">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-150">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18153-151">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18153-151">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


