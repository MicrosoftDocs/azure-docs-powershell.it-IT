---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182167"
---
# <span data-ttu-id="d42c5-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d42c5-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="d42c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d42c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d42c5-103">Recupera i gruppi di utenti del runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="d42c5-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="d42c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d42c5-104">SYNTAX</span></span>

### <span data-ttu-id="d42c5-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d42c5-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d42c5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d42c5-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d42c5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d42c5-107">DESCRIPTION</span></span>
<span data-ttu-id="d42c5-108">Il cmdlet **Get-AzAutomationHybridWorkerGroup** ottiene i gruppi di runbook ibridi di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d42c5-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="d42c5-109">Per ottenere un gruppo specifico, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="d42c5-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="d42c5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d42c5-110">EXAMPLES</span></span>

### <span data-ttu-id="d42c5-111">Esempio 1: Ottenere tutti i gruppi di utenti di runbook ibridi</span><span class="sxs-lookup"><span data-stu-id="d42c5-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d42c5-112">Questo comando recupera tutti i gruppi di utenti con runbook ibridi nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d42c5-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d42c5-113">Esempio 2: Ottenere un singolo gruppo di utenti con runbook ibrido</span><span class="sxs-lookup"><span data-stu-id="d42c5-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="d42c5-114">Questo comando ottiene il gruppo di utenti runbook ibridi denominato HybridRunbookWorkerGroup01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d42c5-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d42c5-115">Esempio 3: Raggruppare i dipendenti in un gruppo di utenti con runbook ibrido</span><span class="sxs-lookup"><span data-stu-id="d42c5-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="d42c5-116">Questo comando recupera i runbook di lavoro ibridi nel gruppo di utenti con runbook ibrido denominato HybridRunbookWorkerGroup01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d42c5-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d42c5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d42c5-117">PARAMETERS</span></span>

### <span data-ttu-id="d42c5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d42c5-118">-AutomationAccountName</span></span>
<span data-ttu-id="d42c5-119">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="d42c5-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="d42c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42c5-120">-DefaultProfile</span></span>
<span data-ttu-id="d42c5-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d42c5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d42c5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d42c5-122">-Name</span></span>
<span data-ttu-id="d42c5-123">Specifica il nome del gruppo di utenti del runbook ibrido.</span><span class="sxs-lookup"><span data-stu-id="d42c5-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="d42c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d42c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="d42c5-125">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d42c5-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d42c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42c5-126">CommonParameters</span></span>
<span data-ttu-id="d42c5-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d42c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42c5-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42c5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42c5-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="d42c5-129">INPUTS</span></span>

### <span data-ttu-id="d42c5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d42c5-130">System.String</span></span>

## <span data-ttu-id="d42c5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d42c5-131">OUTPUTS</span></span>

### <span data-ttu-id="d42c5-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d42c5-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="d42c5-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="d42c5-133">NOTES</span></span>

## <span data-ttu-id="d42c5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d42c5-134">RELATED LINKS</span></span>
