---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519935"
---
# <span data-ttu-id="2314c-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="2314c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2314c-102">SYNOPSIS</span></span>
<span data-ttu-id="2314c-103">Modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="2314c-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2314c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2314c-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2314c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2314c-105">DESCRIPTION</span></span>
<span data-ttu-id="2314c-106">Il cmdlet **set-AzureRmAutomationRunbook** modifica la configurazione di un Runbook di automazione di Azure in APS.</span><span class="sxs-lookup"><span data-stu-id="2314c-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="2314c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2314c-107">EXAMPLES</span></span>

### <span data-ttu-id="2314c-108">Esempio 1: abilitare la registrazione dettagliata per un Runbook</span><span class="sxs-lookup"><span data-stu-id="2314c-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2314c-109">Questo comando consente di abilitare la registrazione dettagliata per i processi del Runbook specificato nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2314c-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2314c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2314c-110">PARAMETERS</span></span>

### <span data-ttu-id="2314c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2314c-111">-AutomationAccountName</span></span>
<span data-ttu-id="2314c-112">Specifica il nome dell'account di automazione in cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="2314c-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="2314c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2314c-113">-DefaultProfile</span></span>
<span data-ttu-id="2314c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2314c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2314c-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2314c-115">-Description</span></span>
<span data-ttu-id="2314c-116">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="2314c-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="2314c-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="2314c-117">-LogProgress</span></span>
<span data-ttu-id="2314c-118">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2314c-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="2314c-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="2314c-119">-LogVerbose</span></span>
<span data-ttu-id="2314c-120">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="2314c-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="2314c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2314c-121">-Name</span></span>
<span data-ttu-id="2314c-122">Specifica il nome del Runbook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2314c-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2314c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2314c-123">-ResourceGroupName</span></span>
<span data-ttu-id="2314c-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="2314c-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="2314c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2314c-125">-Tag</span></span>
<span data-ttu-id="2314c-126">I tag Runbook.</span><span class="sxs-lookup"><span data-stu-id="2314c-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2314c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2314c-127">CommonParameters</span></span>
<span data-ttu-id="2314c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2314c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2314c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2314c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2314c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2314c-130">INPUTS</span></span>

### <span data-ttu-id="2314c-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2314c-131">None</span></span>
<span data-ttu-id="2314c-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2314c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2314c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2314c-133">OUTPUTS</span></span>

### <span data-ttu-id="2314c-134">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="2314c-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="2314c-135">Note</span><span class="sxs-lookup"><span data-stu-id="2314c-135">NOTES</span></span>

## <span data-ttu-id="2314c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2314c-136">RELATED LINKS</span></span>

[<span data-ttu-id="2314c-137">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-138">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-139">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-140">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-141">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-142">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-143">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2314c-144">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2314c-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


