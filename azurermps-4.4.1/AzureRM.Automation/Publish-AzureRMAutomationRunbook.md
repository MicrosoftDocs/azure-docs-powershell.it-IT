---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519638"
---
# <span data-ttu-id="90430-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="90430-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90430-102">SYNOPSIS</span></span>
<span data-ttu-id="90430-103">Pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="90430-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90430-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90430-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90430-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90430-105">DESCRIPTION</span></span>
<span data-ttu-id="90430-106">Il cmdlet **Publish-AzureRmAutomationRunbook** pubblica un Runbook per l'uso nell'ambiente di produzione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="90430-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="90430-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90430-107">EXAMPLES</span></span>

### <span data-ttu-id="90430-108">Esempio 1: pubblicare un Runbook</span><span class="sxs-lookup"><span data-stu-id="90430-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="90430-109">Questo comando pubblica il Runbook denominato Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="90430-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="90430-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90430-110">PARAMETERS</span></span>

### <span data-ttu-id="90430-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="90430-111">-AutomationAccountName</span></span>
<span data-ttu-id="90430-112">Specifica il nome dell'account di automazione in cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="90430-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="90430-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="90430-113">-Name</span></span>
<span data-ttu-id="90430-114">Specifica il nome del Runbook che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="90430-114">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="90430-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90430-115">-ResourceGroupName</span></span>
<span data-ttu-id="90430-116">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="90430-116">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="90430-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90430-117">-DefaultProfile</span></span>
<span data-ttu-id="90430-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90430-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90430-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90430-119">CommonParameters</span></span>
<span data-ttu-id="90430-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90430-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90430-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90430-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90430-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90430-122">INPUTS</span></span>

## <span data-ttu-id="90430-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90430-123">OUTPUTS</span></span>

### <span data-ttu-id="90430-124">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="90430-124">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="90430-125">Note</span><span class="sxs-lookup"><span data-stu-id="90430-125">NOTES</span></span>

## <span data-ttu-id="90430-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90430-126">RELATED LINKS</span></span>

[<span data-ttu-id="90430-127">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-127">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-128">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-128">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-129">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-129">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-130">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-130">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-131">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-132">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-132">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-133">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-133">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="90430-134">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="90430-134">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


