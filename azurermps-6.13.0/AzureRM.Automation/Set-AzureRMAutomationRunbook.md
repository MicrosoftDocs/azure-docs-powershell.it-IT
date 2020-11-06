---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 26f3214cf98e43a805aab99eb3ad1b92f289b2bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513956"
---
# <span data-ttu-id="a3336-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="a3336-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3336-102">SYNOPSIS</span></span>
<span data-ttu-id="a3336-103">Modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a3336-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3336-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3336-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3336-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3336-105">DESCRIPTION</span></span>
<span data-ttu-id="a3336-106">Il cmdlet **set-AzureRmAutomationRunbook** modifica la configurazione di un Runbook di automazione di Azure in APS.</span><span class="sxs-lookup"><span data-stu-id="a3336-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="a3336-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3336-107">EXAMPLES</span></span>

### <span data-ttu-id="a3336-108">Esempio 1: abilitare la registrazione dettagliata per un Runbook</span><span class="sxs-lookup"><span data-stu-id="a3336-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a3336-109">Questo comando consente di abilitare la registrazione dettagliata per i processi del Runbook specificato nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a3336-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a3336-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3336-110">PARAMETERS</span></span>

### <span data-ttu-id="a3336-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a3336-111">-AutomationAccountName</span></span>
<span data-ttu-id="a3336-112">Specifica il nome dell'account di automazione in cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a3336-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="a3336-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3336-113">-DefaultProfile</span></span>
<span data-ttu-id="a3336-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a3336-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3336-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3336-115">-Description</span></span>
<span data-ttu-id="a3336-116">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="a3336-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="a3336-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="a3336-117">-LogProgress</span></span>
<span data-ttu-id="a3336-118">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a3336-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="a3336-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="a3336-119">-LogVerbose</span></span>
<span data-ttu-id="a3336-120">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="a3336-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="a3336-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3336-121">-Name</span></span>
<span data-ttu-id="a3336-122">Specifica il nome del Runbook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3336-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a3336-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3336-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3336-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a3336-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="a3336-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3336-125">-Tag</span></span>
<span data-ttu-id="a3336-126">I tag Runbook.</span><span class="sxs-lookup"><span data-stu-id="a3336-126">The runbook tags.</span></span>

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

### <span data-ttu-id="a3336-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3336-127">CommonParameters</span></span>
<span data-ttu-id="a3336-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3336-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3336-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3336-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3336-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3336-130">INPUTS</span></span>

### <span data-ttu-id="a3336-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a3336-131">System.String</span></span>

### <span data-ttu-id="a3336-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="a3336-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="a3336-133">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a3336-133">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a3336-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3336-134">OUTPUTS</span></span>

### <span data-ttu-id="a3336-135">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="a3336-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="a3336-136">Note</span><span class="sxs-lookup"><span data-stu-id="a3336-136">NOTES</span></span>

## <span data-ttu-id="a3336-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3336-137">RELATED LINKS</span></span>

[<span data-ttu-id="a3336-138">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-138">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-139">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-139">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-140">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-140">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-141">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-142">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-142">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-143">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-143">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-144">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-144">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a3336-145">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a3336-145">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


