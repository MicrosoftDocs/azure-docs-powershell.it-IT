---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687652"
---
# <span data-ttu-id="42b40-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="42b40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42b40-102">SYNOPSIS</span></span>
<span data-ttu-id="42b40-103">Crea un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="42b40-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42b40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42b40-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b40-105">DESCRIPTION</span></span>
<span data-ttu-id="42b40-106">Il cmdlet **New-AzureRmAutomationRunbook** crea un Runbook di automazione Azure vuoto tramite APS.</span><span class="sxs-lookup"><span data-stu-id="42b40-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="42b40-107">Specificare un nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="42b40-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="42b40-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42b40-108">EXAMPLES</span></span>

### <span data-ttu-id="42b40-109">Esempio 1: creare un Runbook</span><span class="sxs-lookup"><span data-stu-id="42b40-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="42b40-110">Questo comando crea un Runbook denominato Runbook02 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="42b40-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="42b40-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42b40-111">PARAMETERS</span></span>

### <span data-ttu-id="42b40-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42b40-112">-AutomationAccountName</span></span>
<span data-ttu-id="42b40-113">Specifica il nome dell'account di automazione in cui questo cmdlet crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="42b40-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="42b40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b40-114">-DefaultProfile</span></span>
<span data-ttu-id="42b40-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="42b40-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42b40-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b40-116">-Description</span></span>
<span data-ttu-id="42b40-117">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="42b40-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="42b40-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="42b40-118">-LogProgress</span></span>
<span data-ttu-id="42b40-119">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="42b40-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="42b40-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="42b40-120">-LogVerbose</span></span>
<span data-ttu-id="42b40-121">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="42b40-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="42b40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="42b40-122">-Name</span></span>
<span data-ttu-id="42b40-123">Specifica un nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="42b40-123">Specifies a name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b40-124">-ResourceGroupName</span></span>
<span data-ttu-id="42b40-125">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="42b40-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="42b40-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="42b40-126">-Tags</span></span>
<span data-ttu-id="42b40-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="42b40-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42b40-128">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="42b40-128">For example:</span></span>

<span data-ttu-id="42b40-129">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="42b40-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="42b40-130">-Digitare</span><span class="sxs-lookup"><span data-stu-id="42b40-130">-Type</span></span>
<span data-ttu-id="42b40-131">Specifica il tipo di Runbook creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b40-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="42b40-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="42b40-132">Valid values are:</span></span>

- <span data-ttu-id="42b40-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="42b40-133">PowerShell</span></span>
- <span data-ttu-id="42b40-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="42b40-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="42b40-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="42b40-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="42b40-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="42b40-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="42b40-137">Grafico</span><span class="sxs-lookup"><span data-stu-id="42b40-137">Graph</span></span>

<span data-ttu-id="42b40-138">Il grafico del valore è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="42b40-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="42b40-139">Equivale a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="42b40-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b40-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b40-140">CommonParameters</span></span>
<span data-ttu-id="42b40-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b40-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b40-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b40-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b40-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42b40-143">INPUTS</span></span>

### <span data-ttu-id="42b40-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="42b40-144">None</span></span>
<span data-ttu-id="42b40-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="42b40-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42b40-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42b40-146">OUTPUTS</span></span>

### <span data-ttu-id="42b40-147">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="42b40-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="42b40-148">Note</span><span class="sxs-lookup"><span data-stu-id="42b40-148">NOTES</span></span>

## <span data-ttu-id="42b40-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42b40-149">RELATED LINKS</span></span>

[<span data-ttu-id="42b40-150">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="42b40-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="42b40-152">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="42b40-153">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="42b40-154">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="42b40-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="42b40-156">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42b40-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
