---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511367"
---
# <span data-ttu-id="f8802-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="f8802-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8802-102">SYNOPSIS</span></span>
<span data-ttu-id="f8802-103">Modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8802-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8802-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8802-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8802-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8802-105">DESCRIPTION</span></span>
<span data-ttu-id="f8802-106">Il cmdlet **set-AzureRmAutomationRunbook** modifica la configurazione di un Runbook di automazione di Azure in APS.</span><span class="sxs-lookup"><span data-stu-id="f8802-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="f8802-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8802-107">EXAMPLES</span></span>

### <span data-ttu-id="f8802-108">Esempio 1: abilitare la registrazione dettagliata per un Runbook</span><span class="sxs-lookup"><span data-stu-id="f8802-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8802-109">Questo comando consente di abilitare la registrazione dettagliata per i processi del Runbook specificato nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8802-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f8802-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8802-110">PARAMETERS</span></span>

### <span data-ttu-id="f8802-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8802-111">-AutomationAccountName</span></span>
<span data-ttu-id="f8802-112">Specifica il nome dell'account di automazione in cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8802-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="f8802-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8802-113">-Description</span></span>
<span data-ttu-id="f8802-114">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8802-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="f8802-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="f8802-115">-LogProgress</span></span>
<span data-ttu-id="f8802-116">Specifica se il Runbook registra lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f8802-116">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="f8802-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f8802-117">-LogVerbose</span></span>
<span data-ttu-id="f8802-118">Specifica se la registrazione include informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="f8802-118">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="f8802-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8802-119">-Name</span></span>
<span data-ttu-id="f8802-120">Specifica il nome del Runbook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8802-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f8802-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8802-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8802-122">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8802-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="f8802-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8802-123">-Tags</span></span>
<span data-ttu-id="f8802-124">Specifica un dizionario di tag per sostituire i tag correnti della Runbook modificata.</span><span class="sxs-lookup"><span data-stu-id="f8802-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

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

### <span data-ttu-id="f8802-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8802-125">-DefaultProfile</span></span>
<span data-ttu-id="f8802-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8802-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8802-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8802-127">CommonParameters</span></span>
<span data-ttu-id="f8802-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8802-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8802-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8802-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8802-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8802-130">INPUTS</span></span>

## <span data-ttu-id="f8802-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8802-131">OUTPUTS</span></span>

### <span data-ttu-id="f8802-132">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="f8802-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f8802-133">Note</span><span class="sxs-lookup"><span data-stu-id="f8802-133">NOTES</span></span>

## <span data-ttu-id="f8802-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8802-134">RELATED LINKS</span></span>

[<span data-ttu-id="f8802-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-140">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-141">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8802-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8802-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


