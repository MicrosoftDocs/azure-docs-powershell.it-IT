---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865362"
---
# <span data-ttu-id="b637c-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="b637c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b637c-102">SYNOPSIS</span></span>
<span data-ttu-id="b637c-103">Modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="b637c-103">Modifies a runbook.</span></span>

## <span data-ttu-id="b637c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b637c-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b637c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b637c-105">DESCRIPTION</span></span>
<span data-ttu-id="b637c-106">Il cmdlet **set-AzAutomationRunbook** modifica la configurazione di un Runbook di automazione di Azure in APS.</span><span class="sxs-lookup"><span data-stu-id="b637c-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="b637c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b637c-107">EXAMPLES</span></span>

### <span data-ttu-id="b637c-108">Esempio 1: abilitare la registrazione dettagliata per un Runbook</span><span class="sxs-lookup"><span data-stu-id="b637c-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b637c-109">Questo comando consente di abilitare la registrazione dettagliata per i processi del Runbook specificato nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b637c-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b637c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b637c-110">PARAMETERS</span></span>

### <span data-ttu-id="b637c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b637c-111">-AutomationAccountName</span></span>
<span data-ttu-id="b637c-112">Specifica il nome dell'account di automazione in cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="b637c-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="b637c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b637c-113">-DefaultProfile</span></span>
<span data-ttu-id="b637c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b637c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b637c-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b637c-115">-Description</span></span>
<span data-ttu-id="b637c-116">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="b637c-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="b637c-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="b637c-117">-LogProgress</span></span>
<span data-ttu-id="b637c-118">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b637c-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="b637c-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="b637c-119">-LogVerbose</span></span>
<span data-ttu-id="b637c-120">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="b637c-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="b637c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b637c-121">-Name</span></span>
<span data-ttu-id="b637c-122">Specifica il nome del Runbook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b637c-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b637c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b637c-123">-ResourceGroupName</span></span>
<span data-ttu-id="b637c-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="b637c-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="b637c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b637c-125">-Tag</span></span>
<span data-ttu-id="b637c-126">I tag Runbook.</span><span class="sxs-lookup"><span data-stu-id="b637c-126">The runbook tags.</span></span>

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

### <span data-ttu-id="b637c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b637c-127">CommonParameters</span></span>
<span data-ttu-id="b637c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b637c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b637c-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b637c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b637c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b637c-130">INPUTS</span></span>

### <span data-ttu-id="b637c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b637c-131">System.String</span></span>

### <span data-ttu-id="b637c-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="b637c-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="b637c-133">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b637c-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b637c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b637c-134">OUTPUTS</span></span>

### <span data-ttu-id="b637c-135">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="b637c-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="b637c-136">Note</span><span class="sxs-lookup"><span data-stu-id="b637c-136">NOTES</span></span>

## <span data-ttu-id="b637c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b637c-137">RELATED LINKS</span></span>

[<span data-ttu-id="b637c-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="b637c-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b637c-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


