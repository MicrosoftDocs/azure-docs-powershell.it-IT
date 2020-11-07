---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685026"
---
# <span data-ttu-id="60f46-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="60f46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60f46-102">SYNOPSIS</span></span>
<span data-ttu-id="60f46-103">Crea un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="60f46-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="60f46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60f46-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60f46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60f46-105">DESCRIPTION</span></span>
<span data-ttu-id="60f46-106">Il cmdlet **New-AzAutomationRunbook** crea un Runbook di automazione Azure vuoto tramite APS.</span><span class="sxs-lookup"><span data-stu-id="60f46-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="60f46-107">Specificare un nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="60f46-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="60f46-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60f46-108">EXAMPLES</span></span>

### <span data-ttu-id="60f46-109">Esempio 1: creare un Runbook</span><span class="sxs-lookup"><span data-stu-id="60f46-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60f46-110">Questo comando crea un Runbook denominato Runbook02 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="60f46-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="60f46-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60f46-111">PARAMETERS</span></span>

### <span data-ttu-id="60f46-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60f46-112">-AutomationAccountName</span></span>
<span data-ttu-id="60f46-113">Specifica il nome dell'account di automazione in cui questo cmdlet crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="60f46-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="60f46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f46-114">-DefaultProfile</span></span>
<span data-ttu-id="60f46-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="60f46-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f46-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="60f46-116">-Description</span></span>
<span data-ttu-id="60f46-117">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="60f46-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="60f46-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="60f46-118">-LogProgress</span></span>
<span data-ttu-id="60f46-119">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="60f46-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="60f46-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="60f46-120">-LogVerbose</span></span>
<span data-ttu-id="60f46-121">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="60f46-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="60f46-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="60f46-122">-Name</span></span>
<span data-ttu-id="60f46-123">Specifica un nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="60f46-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="60f46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f46-124">-ResourceGroupName</span></span>
<span data-ttu-id="60f46-125">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="60f46-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="60f46-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="60f46-126">-Tags</span></span>
<span data-ttu-id="60f46-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="60f46-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="60f46-128">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="60f46-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="60f46-129">-Digitare</span><span class="sxs-lookup"><span data-stu-id="60f46-129">-Type</span></span>
<span data-ttu-id="60f46-130">Specifica il tipo di Runbook creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60f46-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="60f46-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="60f46-131">Valid values are:</span></span>
- <span data-ttu-id="60f46-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="60f46-132">PowerShell</span></span>
- <span data-ttu-id="60f46-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="60f46-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="60f46-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="60f46-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="60f46-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="60f46-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="60f46-136">Grafico</span><span class="sxs-lookup"><span data-stu-id="60f46-136">Graph</span></span>
- <span data-ttu-id="60f46-137">Python2 il valore grafico è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="60f46-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="60f46-138">Equivale a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="60f46-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="60f46-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f46-139">CommonParameters</span></span>
<span data-ttu-id="60f46-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f46-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f46-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f46-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f46-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60f46-142">INPUTS</span></span>

### <span data-ttu-id="60f46-143">System. String</span><span class="sxs-lookup"><span data-stu-id="60f46-143">System.String</span></span>

### <span data-ttu-id="60f46-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="60f46-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="60f46-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60f46-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="60f46-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60f46-146">OUTPUTS</span></span>

### <span data-ttu-id="60f46-147">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="60f46-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="60f46-148">Note</span><span class="sxs-lookup"><span data-stu-id="60f46-148">NOTES</span></span>

## <span data-ttu-id="60f46-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60f46-149">RELATED LINKS</span></span>

[<span data-ttu-id="60f46-150">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="60f46-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="60f46-152">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="60f46-153">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="60f46-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="60f46-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="60f46-156">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60f46-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
