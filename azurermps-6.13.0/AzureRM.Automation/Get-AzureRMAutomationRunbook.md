---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: 5a47676a7c01052f44acba6362bd24eb65e4c05f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520293"
---
# <span data-ttu-id="ec61a-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ec61a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec61a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec61a-103">Ottiene un Runbook.</span><span class="sxs-lookup"><span data-stu-id="ec61a-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec61a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec61a-104">SYNTAX</span></span>

### <span data-ttu-id="ec61a-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec61a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec61a-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ec61a-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec61a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec61a-107">DESCRIPTION</span></span>
<span data-ttu-id="ec61a-108">Il cmdlet **Get-AzureRmAutomationRunbook** ottiene manuali operativi di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec61a-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="ec61a-109">Per ottenere uno specifico Runbook, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="ec61a-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="ec61a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec61a-110">EXAMPLES</span></span>

### <span data-ttu-id="ec61a-111">Esempio 1: ottenere tutti manuali operativi</span><span class="sxs-lookup"><span data-stu-id="ec61a-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ec61a-112">Questo comando ottiene tutti i manuali operativi nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ec61a-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ec61a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec61a-113">PARAMETERS</span></span>

### <span data-ttu-id="ec61a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ec61a-114">-AutomationAccountName</span></span>
<span data-ttu-id="ec61a-115">Specifica il nome di un account di automazione in cui questo cmdlet ottiene manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="ec61a-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="ec61a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec61a-116">-DefaultProfile</span></span>
<span data-ttu-id="ec61a-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ec61a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec61a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec61a-118">-Name</span></span>
<span data-ttu-id="ec61a-119">Specifica il nome di un Runbook ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec61a-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec61a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec61a-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec61a-121">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="ec61a-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="ec61a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec61a-122">CommonParameters</span></span>
<span data-ttu-id="ec61a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec61a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec61a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec61a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec61a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec61a-125">INPUTS</span></span>

### <span data-ttu-id="ec61a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ec61a-126">System.String</span></span>

## <span data-ttu-id="ec61a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec61a-127">OUTPUTS</span></span>

### <span data-ttu-id="ec61a-128">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ec61a-129">Note</span><span class="sxs-lookup"><span data-stu-id="ec61a-129">NOTES</span></span>

## <span data-ttu-id="ec61a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec61a-130">RELATED LINKS</span></span>

[<span data-ttu-id="ec61a-131">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-131">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-132">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-132">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-133">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-134">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-135">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-135">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-136">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-136">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-137">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-137">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ec61a-138">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ec61a-138">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


