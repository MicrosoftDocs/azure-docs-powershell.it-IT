---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1202ecbdaaf07b9ba5704a01449784172204bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510164"
---
# <span data-ttu-id="38552-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="38552-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38552-102">SYNOPSIS</span></span>
<span data-ttu-id="38552-103">Pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="38552-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38552-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38552-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38552-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38552-105">DESCRIPTION</span></span>
<span data-ttu-id="38552-106">Il cmdlet **Publish-AzureRmAutomationRunbook** pubblica un Runbook per l'uso nell'ambiente di produzione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="38552-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="38552-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38552-107">EXAMPLES</span></span>

### <span data-ttu-id="38552-108">Esempio 1: pubblicare un Runbook</span><span class="sxs-lookup"><span data-stu-id="38552-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="38552-109">Questo comando pubblica il Runbook denominato Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="38552-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="38552-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38552-110">PARAMETERS</span></span>

### <span data-ttu-id="38552-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38552-111">-AutomationAccountName</span></span>
<span data-ttu-id="38552-112">Specifica il nome dell'account di automazione in cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="38552-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="38552-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38552-113">-DefaultProfile</span></span>
<span data-ttu-id="38552-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="38552-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38552-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="38552-115">-Name</span></span>
<span data-ttu-id="38552-116">Specifica il nome del Runbook che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="38552-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="38552-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38552-117">-ResourceGroupName</span></span>
<span data-ttu-id="38552-118">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="38552-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="38552-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38552-119">CommonParameters</span></span>
<span data-ttu-id="38552-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38552-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38552-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38552-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38552-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38552-122">INPUTS</span></span>

### <span data-ttu-id="38552-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="38552-123">None</span></span>
<span data-ttu-id="38552-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="38552-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38552-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38552-125">OUTPUTS</span></span>

### <span data-ttu-id="38552-126">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="38552-126">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="38552-127">Note</span><span class="sxs-lookup"><span data-stu-id="38552-127">NOTES</span></span>

## <span data-ttu-id="38552-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38552-128">RELATED LINKS</span></span>

[<span data-ttu-id="38552-129">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-129">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-130">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-130">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-131">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-132">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-133">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-134">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-134">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-135">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-135">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38552-136">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38552-136">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


