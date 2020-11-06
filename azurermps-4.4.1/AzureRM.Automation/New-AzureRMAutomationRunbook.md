---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517115"
---
# <span data-ttu-id="34bde-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="34bde-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34bde-102">SYNOPSIS</span></span>
<span data-ttu-id="34bde-103">Crea un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="34bde-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34bde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34bde-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34bde-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34bde-105">DESCRIPTION</span></span>
<span data-ttu-id="34bde-106">Il cmdlet **New-AzureRmAutomationRunbook** crea un Runbook di automazione Azure vuoto tramite APS.</span><span class="sxs-lookup"><span data-stu-id="34bde-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="34bde-107">Specificare un nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="34bde-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="34bde-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34bde-108">EXAMPLES</span></span>

### <span data-ttu-id="34bde-109">Esempio 1: creare un Runbook</span><span class="sxs-lookup"><span data-stu-id="34bde-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="34bde-110">Questo comando crea un Runbook denominato Runbook02 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="34bde-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="34bde-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34bde-111">PARAMETERS</span></span>

### <span data-ttu-id="34bde-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34bde-112">-AutomationAccountName</span></span>
<span data-ttu-id="34bde-113">Specifica il nome dell'account di automazione in cui questo cmdlet crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="34bde-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="34bde-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="34bde-114">-Description</span></span>
<span data-ttu-id="34bde-115">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="34bde-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="34bde-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="34bde-116">-LogProgress</span></span>
<span data-ttu-id="34bde-117">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="34bde-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="34bde-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="34bde-118">-LogVerbose</span></span>
<span data-ttu-id="34bde-119">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="34bde-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="34bde-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="34bde-120">-Name</span></span>
<span data-ttu-id="34bde-121">Specifica un nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="34bde-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="34bde-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34bde-122">-ResourceGroupName</span></span>
<span data-ttu-id="34bde-123">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="34bde-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="34bde-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="34bde-124">-Tags</span></span>
<span data-ttu-id="34bde-125">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="34bde-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34bde-126">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="34bde-126">For example:</span></span>

<span data-ttu-id="34bde-127">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="34bde-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="34bde-128">-Digitare</span><span class="sxs-lookup"><span data-stu-id="34bde-128">-Type</span></span>
<span data-ttu-id="34bde-129">Specifica il tipo di Runbook creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34bde-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="34bde-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="34bde-130">Valid values are:</span></span>

- <span data-ttu-id="34bde-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="34bde-131">PowerShell</span></span>
- <span data-ttu-id="34bde-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="34bde-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="34bde-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="34bde-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="34bde-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="34bde-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="34bde-135">Grafico</span><span class="sxs-lookup"><span data-stu-id="34bde-135">Graph</span></span>

<span data-ttu-id="34bde-136">Il grafico del valore è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="34bde-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="34bde-137">Equivale a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="34bde-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="34bde-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bde-138">-DefaultProfile</span></span>
<span data-ttu-id="34bde-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34bde-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34bde-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bde-140">CommonParameters</span></span>
<span data-ttu-id="34bde-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bde-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bde-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34bde-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bde-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34bde-143">INPUTS</span></span>

## <span data-ttu-id="34bde-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34bde-144">OUTPUTS</span></span>

### <span data-ttu-id="34bde-145">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="34bde-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="34bde-146">Note</span><span class="sxs-lookup"><span data-stu-id="34bde-146">NOTES</span></span>

## <span data-ttu-id="34bde-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34bde-147">RELATED LINKS</span></span>

[<span data-ttu-id="34bde-148">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="34bde-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="34bde-150">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="34bde-151">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="34bde-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="34bde-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="34bde-154">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="34bde-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
