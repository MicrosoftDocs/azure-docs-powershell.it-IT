---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 89c1b96744ce67765bed53f850e21a457ead4b6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996979"
---
# <span data-ttu-id="73ff8-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="73ff8-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="73ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="73ff8-103">Recupera i gruppi di utenti del runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="73ff8-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="73ff8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73ff8-104">SYNTAX</span></span>

### <span data-ttu-id="73ff8-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73ff8-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73ff8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="73ff8-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73ff8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="73ff8-107">DESCRIPTION</span></span>
<span data-ttu-id="73ff8-108">Il cmdlet **Get-AzAutomationHybridWorkerGroup** ottiene i gruppi di runbook ibridi di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="73ff8-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="73ff8-109">Per ottenere un gruppo specifico, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="73ff8-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="73ff8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="73ff8-111">Esempio 1: Ottenere tutti i gruppi di utenti di runbook ibridi</span><span class="sxs-lookup"><span data-stu-id="73ff8-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="73ff8-112">Questo comando recupera tutti i gruppi di utenti con runbook ibridi nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="73ff8-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="73ff8-113">Esempio 2: Ottenere un singolo gruppo di utenti con runbook ibrido</span><span class="sxs-lookup"><span data-stu-id="73ff8-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="73ff8-114">Questo comando recupera il gruppo di utenti runbook ibridi denominato HybridRunbookWorkerGroup01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="73ff8-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="73ff8-115">Esempio 3: Raggruppare i dipendenti in un gruppo di utenti con runbook ibrido</span><span class="sxs-lookup"><span data-stu-id="73ff8-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="73ff8-116">Questo comando recupera i runbook di lavoro ibridi nel gruppo di utenti con runbook ibrido denominato HybridRunbookWorkerGroup01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="73ff8-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="73ff8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73ff8-117">PARAMETERS</span></span>

### <span data-ttu-id="73ff8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="73ff8-118">-AutomationAccountName</span></span>
<span data-ttu-id="73ff8-119">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="73ff8-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="73ff8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ff8-120">-DefaultProfile</span></span>
<span data-ttu-id="73ff8-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="73ff8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73ff8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="73ff8-122">-Name</span></span>
<span data-ttu-id="73ff8-123">Specifica il nome del gruppo di utenti del runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="73ff8-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ff8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ff8-124">-ResourceGroupName</span></span>
<span data-ttu-id="73ff8-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73ff8-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="73ff8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ff8-126">CommonParameters</span></span>
<span data-ttu-id="73ff8-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ff8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ff8-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ff8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ff8-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="73ff8-129">INPUTS</span></span>

### <span data-ttu-id="73ff8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="73ff8-130">System.String</span></span>

## <span data-ttu-id="73ff8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73ff8-131">OUTPUTS</span></span>

### <span data-ttu-id="73ff8-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="73ff8-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="73ff8-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="73ff8-133">NOTES</span></span>

## <span data-ttu-id="73ff8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73ff8-134">RELATED LINKS</span></span>
