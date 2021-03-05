---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: c0c1b83f177b568e7058b973b788a633cfefe48c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970126"
---
# <span data-ttu-id="f4cd6-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f4cd6-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="f4cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cd6-103">Ottenere lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="f4cd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4cd6-104">SYNTAX</span></span>

### <span data-ttu-id="f4cd6-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4cd6-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4cd6-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="f4cd6-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4cd6-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f4cd6-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4cd6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4cd6-108">DESCRIPTION</span></span>
<span data-ttu-id="f4cd6-109">Il cmdlet **Get-AzSynapseTriggerSubscriptionStatus** ottiene lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="f4cd6-110">Il trigger non può essere avviato finché lo stato restituito non è "Abilitato".</span><span class="sxs-lookup"><span data-stu-id="f4cd6-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="f4cd6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4cd6-111">EXAMPLES</span></span>

### <span data-ttu-id="f4cd6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4cd6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="f4cd6-113">Questo comando ottiene lo stato dell'iscrizione per il trigger denominato ContosoTrigger agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="f4cd6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f4cd6-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="f4cd6-115">Questo comando consente di ottenere lo stato dell'iscrizione per il trigger denominato ContosoTrigger agli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="f4cd6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f4cd6-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="f4cd6-117">Questo comando ottiene lo stato dell'iscrizione per il trigger denominato ContosoTrigger agli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="f4cd6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4cd6-118">PARAMETERS</span></span>

### <span data-ttu-id="f4cd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4cd6-119">-DefaultProfile</span></span>
<span data-ttu-id="f4cd6-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4cd6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4cd6-121">-InputObject</span></span>
<span data-ttu-id="f4cd6-122">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cd6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f4cd6-123">-Name</span></span>
<span data-ttu-id="f4cd6-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cd6-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4cd6-125">-WorkspaceName</span></span>
<span data-ttu-id="f4cd6-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4cd6-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f4cd6-127">-WorkspaceObject</span></span>
<span data-ttu-id="f4cd6-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4cd6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cd6-129">CommonParameters</span></span>
<span data-ttu-id="f4cd6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cd6-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4cd6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cd6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4cd6-132">INPUTS</span></span>

### <span data-ttu-id="f4cd6-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f4cd6-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f4cd6-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="f4cd6-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="f4cd6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4cd6-135">OUTPUTS</span></span>

### <span data-ttu-id="f4cd6-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f4cd6-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="f4cd6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4cd6-137">NOTES</span></span>

## <span data-ttu-id="f4cd6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4cd6-138">RELATED LINKS</span></span>
