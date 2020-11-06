---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: a4f65e20253ef979cba5d3907faeba3fb58e7fe6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521458"
---
# <span data-ttu-id="2d749-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="2d749-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d749-102">SYNOPSIS</span></span>
<span data-ttu-id="2d749-103">Rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d749-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d749-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d749-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d749-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d749-105">DESCRIPTION</span></span>
<span data-ttu-id="2d749-106">Il cmdlet **Remove-AzureRmAutomationRunbook** rimuove un Runbook da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2d749-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="2d749-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d749-107">EXAMPLES</span></span>

### <span data-ttu-id="2d749-108">Esempio 1: rimuovere un Runbook</span><span class="sxs-lookup"><span data-stu-id="2d749-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d749-109">Questo comando rimuove il Runbook denominato Runbook03 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2d749-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2d749-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d749-110">PARAMETERS</span></span>

### <span data-ttu-id="2d749-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d749-111">-AutomationAccountName</span></span>
<span data-ttu-id="2d749-112">Specifica il nome dell'account di automazione in cui questo cmdlet rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d749-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="2d749-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d749-113">-DefaultProfile</span></span>
<span data-ttu-id="2d749-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2d749-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d749-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d749-115">-Force</span></span>
<span data-ttu-id="2d749-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="2d749-116">ps_force</span></span>

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

### <span data-ttu-id="2d749-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d749-117">-Name</span></span>
<span data-ttu-id="2d749-118">Specifica il nome del Runbook rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d749-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d749-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d749-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d749-120">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d749-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="2d749-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d749-121">-Confirm</span></span>
<span data-ttu-id="2d749-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d749-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d749-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d749-123">-WhatIf</span></span>
<span data-ttu-id="2d749-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d749-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d749-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d749-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d749-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d749-126">CommonParameters</span></span>
<span data-ttu-id="2d749-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d749-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d749-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d749-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d749-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d749-129">INPUTS</span></span>

### <span data-ttu-id="2d749-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2d749-130">None</span></span>
<span data-ttu-id="2d749-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2d749-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d749-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d749-132">OUTPUTS</span></span>

## <span data-ttu-id="2d749-133">Note</span><span class="sxs-lookup"><span data-stu-id="2d749-133">NOTES</span></span>

## <span data-ttu-id="2d749-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d749-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d749-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-140">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2d749-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d749-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


