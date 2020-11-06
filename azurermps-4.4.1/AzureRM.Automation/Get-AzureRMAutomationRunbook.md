---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: e543a7da3ce5502e0f78619ca4fbb455b29b82d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510779"
---
# <span data-ttu-id="62380-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="62380-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62380-102">SYNOPSIS</span></span>
<span data-ttu-id="62380-103">Ottiene un Runbook.</span><span class="sxs-lookup"><span data-stu-id="62380-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62380-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62380-104">SYNTAX</span></span>

### <span data-ttu-id="62380-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62380-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62380-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="62380-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62380-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62380-107">DESCRIPTION</span></span>
<span data-ttu-id="62380-108">Il cmdlet **Get-AzureRmAutomationRunbook** ottiene manuali operativi di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="62380-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="62380-109">Per ottenere uno specifico Runbook, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="62380-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="62380-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62380-110">EXAMPLES</span></span>

### <span data-ttu-id="62380-111">Esempio 1: ottenere tutti manuali operativi</span><span class="sxs-lookup"><span data-stu-id="62380-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="62380-112">Questo comando ottiene tutti i manuali operativi nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="62380-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="62380-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62380-113">PARAMETERS</span></span>

### <span data-ttu-id="62380-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62380-114">-AutomationAccountName</span></span>
<span data-ttu-id="62380-115">Specifica il nome di un account di automazione in cui questo cmdlet ottiene manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="62380-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="62380-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="62380-116">-Name</span></span>
<span data-ttu-id="62380-117">Specifica il nome di un Runbook ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62380-117">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62380-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62380-118">-ResourceGroupName</span></span>
<span data-ttu-id="62380-119">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene manuali operativi.</span><span class="sxs-lookup"><span data-stu-id="62380-119">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="62380-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62380-120">-DefaultProfile</span></span>
<span data-ttu-id="62380-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62380-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62380-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62380-122">CommonParameters</span></span>
<span data-ttu-id="62380-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62380-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62380-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62380-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62380-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62380-125">INPUTS</span></span>

## <span data-ttu-id="62380-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62380-126">OUTPUTS</span></span>

### <span data-ttu-id="62380-127">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="62380-127">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="62380-128">Note</span><span class="sxs-lookup"><span data-stu-id="62380-128">NOTES</span></span>

## <span data-ttu-id="62380-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62380-129">RELATED LINKS</span></span>

[<span data-ttu-id="62380-130">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-130">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-131">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-132">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-133">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-134">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-134">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-135">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-135">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-136">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-136">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62380-137">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62380-137">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


