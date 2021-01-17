---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359306"
---
# <span data-ttu-id="52b34-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="52b34-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="52b34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52b34-102">SYNOPSIS</span></span>
<span data-ttu-id="52b34-103">Ottenere lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="52b34-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="52b34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52b34-104">SYNTAX</span></span>

### <span data-ttu-id="52b34-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52b34-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b34-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="52b34-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b34-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="52b34-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52b34-108">DESCRIPTION</span></span>
<span data-ttu-id="52b34-109">Il cmdlet **Get-AzSynapseTriggerSubscriptionStatus** ottiene lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="52b34-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="52b34-110">Il trigger non può essere avviato finché lo stato restituito non è "Enabled".</span><span class="sxs-lookup"><span data-stu-id="52b34-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="52b34-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52b34-111">EXAMPLES</span></span>

### <span data-ttu-id="52b34-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52b34-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="52b34-113">Questo comando otterrà lo stato di abbonamento per trigger denominato ContosoTrigger per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="52b34-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="52b34-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="52b34-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="52b34-115">Questo comando otterrà lo stato di abbonamento per trigger denominato ContosoTrigger per gli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="52b34-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="52b34-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="52b34-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="52b34-117">Questo comando otterrà lo stato di abbonamento per trigger denominato ContosoTrigger per gli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="52b34-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="52b34-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52b34-118">PARAMETERS</span></span>

### <span data-ttu-id="52b34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b34-119">-DefaultProfile</span></span>
<span data-ttu-id="52b34-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52b34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b34-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52b34-121">-InputObject</span></span>
<span data-ttu-id="52b34-122">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="52b34-122">The trigger object.</span></span>

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

### <span data-ttu-id="52b34-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b34-123">-Name</span></span>
<span data-ttu-id="52b34-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="52b34-124">The trigger name.</span></span>

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

### <span data-ttu-id="52b34-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52b34-125">-WorkspaceName</span></span>
<span data-ttu-id="52b34-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="52b34-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="52b34-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="52b34-127">-WorkspaceObject</span></span>
<span data-ttu-id="52b34-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="52b34-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="52b34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b34-129">CommonParameters</span></span>
<span data-ttu-id="52b34-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b34-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52b34-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b34-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52b34-132">INPUTS</span></span>

### <span data-ttu-id="52b34-133">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="52b34-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="52b34-134">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="52b34-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="52b34-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52b34-135">OUTPUTS</span></span>

### <span data-ttu-id="52b34-136">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="52b34-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="52b34-137">Note</span><span class="sxs-lookup"><span data-stu-id="52b34-137">NOTES</span></span>

## <span data-ttu-id="52b34-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52b34-138">RELATED LINKS</span></span>
