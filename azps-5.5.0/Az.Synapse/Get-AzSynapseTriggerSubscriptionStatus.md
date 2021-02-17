---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190607"
---
# <span data-ttu-id="03d4b-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="03d4b-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="03d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="03d4b-103">Ottenere lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="03d4b-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="03d4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03d4b-104">SYNTAX</span></span>

### <span data-ttu-id="03d4b-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03d4b-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03d4b-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="03d4b-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03d4b-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="03d4b-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03d4b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03d4b-108">DESCRIPTION</span></span>
<span data-ttu-id="03d4b-109">Il cmdlet **Get-AzSynapseTriggerSubscriptionStatus** ottiene lo stato della sottoscrizione per il trigger di evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="03d4b-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="03d4b-110">Il trigger non può essere avviato finché lo stato restituito non è "Abilitato".</span><span class="sxs-lookup"><span data-stu-id="03d4b-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="03d4b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03d4b-111">EXAMPLES</span></span>

### <span data-ttu-id="03d4b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03d4b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="03d4b-113">Questo comando otterrà lo stato dell'iscrizione per il trigger denominato ContosoTrigger agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="03d4b-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="03d4b-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="03d4b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="03d4b-115">Questo comando ottiene lo stato dell'iscrizione per il trigger denominato ContosoTrigger agli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="03d4b-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="03d4b-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="03d4b-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="03d4b-117">Questo comando ottiene lo stato dell'iscrizione per il trigger denominato ContosoTrigger agli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="03d4b-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="03d4b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03d4b-118">PARAMETERS</span></span>

### <span data-ttu-id="03d4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d4b-119">-DefaultProfile</span></span>
<span data-ttu-id="03d4b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03d4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03d4b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03d4b-121">-InputObject</span></span>
<span data-ttu-id="03d4b-122">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="03d4b-122">The trigger object.</span></span>

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

### <span data-ttu-id="03d4b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="03d4b-123">-Name</span></span>
<span data-ttu-id="03d4b-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="03d4b-124">The trigger name.</span></span>

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

### <span data-ttu-id="03d4b-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03d4b-125">-WorkspaceName</span></span>
<span data-ttu-id="03d4b-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="03d4b-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="03d4b-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="03d4b-127">-WorkspaceObject</span></span>
<span data-ttu-id="03d4b-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="03d4b-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="03d4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d4b-129">CommonParameters</span></span>
<span data-ttu-id="03d4b-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d4b-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03d4b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d4b-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="03d4b-132">INPUTS</span></span>

### <span data-ttu-id="03d4b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03d4b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="03d4b-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="03d4b-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="03d4b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03d4b-135">OUTPUTS</span></span>

### <span data-ttu-id="03d4b-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="03d4b-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="03d4b-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="03d4b-137">NOTES</span></span>

## <span data-ttu-id="03d4b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03d4b-138">RELATED LINKS</span></span>
