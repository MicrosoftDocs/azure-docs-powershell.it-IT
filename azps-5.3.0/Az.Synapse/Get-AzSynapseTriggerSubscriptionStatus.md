---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383711"
---
# <span data-ttu-id="b8150-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b8150-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b8150-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8150-102">SYNOPSIS</span></span>
<span data-ttu-id="b8150-103">Ottenere lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="b8150-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="b8150-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8150-104">SYNTAX</span></span>

### <span data-ttu-id="b8150-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b8150-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8150-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b8150-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8150-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b8150-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8150-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8150-108">DESCRIPTION</span></span>
<span data-ttu-id="b8150-109">Il cmdlet **Get-AzSynapseTriggerSubscriptionStatus** ottiene lo stato della sottoscrizione per il trigger dell'evento per gli eventi del servizio esterno specificati.</span><span class="sxs-lookup"><span data-stu-id="b8150-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="b8150-110">Il trigger non può essere avviato finché lo stato restituito non è "Enabled".</span><span class="sxs-lookup"><span data-stu-id="b8150-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="b8150-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8150-111">EXAMPLES</span></span>

### <span data-ttu-id="b8150-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b8150-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b8150-113">Questo comando otterrà lo stato di abbonamento per trigger denominato ContosoTrigger per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="b8150-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="b8150-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b8150-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="b8150-115">Questo comando otterrà lo stato di abbonamento per trigger denominato ContosoTrigger per gli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8150-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="b8150-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b8150-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="b8150-117">Questo comando otterrà lo stato di abbonamento per trigger denominato ContosoTrigger per gli eventi del servizio esterno tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8150-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="b8150-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8150-118">PARAMETERS</span></span>

### <span data-ttu-id="b8150-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8150-119">-DefaultProfile</span></span>
<span data-ttu-id="b8150-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8150-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8150-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8150-121">-InputObject</span></span>
<span data-ttu-id="b8150-122">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="b8150-122">The trigger object.</span></span>

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

### <span data-ttu-id="b8150-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8150-123">-Name</span></span>
<span data-ttu-id="b8150-124">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="b8150-124">The trigger name.</span></span>

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

### <span data-ttu-id="b8150-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b8150-125">-WorkspaceName</span></span>
<span data-ttu-id="b8150-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b8150-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b8150-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b8150-127">-WorkspaceObject</span></span>
<span data-ttu-id="b8150-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8150-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b8150-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8150-129">CommonParameters</span></span>
<span data-ttu-id="b8150-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8150-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8150-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8150-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8150-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8150-132">INPUTS</span></span>

### <span data-ttu-id="b8150-133">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b8150-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b8150-134">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b8150-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b8150-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8150-135">OUTPUTS</span></span>

### <span data-ttu-id="b8150-136">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b8150-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="b8150-137">Note</span><span class="sxs-lookup"><span data-stu-id="b8150-137">NOTES</span></span>

## <span data-ttu-id="b8150-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8150-138">RELATED LINKS</span></span>
