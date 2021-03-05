---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: f26e85684aa6565fed88dcbb79cef8637be258ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003245"
---
# <span data-ttu-id="d0558-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d0558-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="d0558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0558-102">SYNOPSIS</span></span>
<span data-ttu-id="d0558-103">Recuperare gli elementi proteggibili in un contenitore di protezione ASR.</span><span class="sxs-lookup"><span data-stu-id="d0558-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="d0558-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0558-104">SYNTAX</span></span>

### <span data-ttu-id="d0558-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0558-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0558-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d0558-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0558-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d0558-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0558-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0558-108">DESCRIPTION</span></span>
<span data-ttu-id="d0558-109">Il cmdlet **Get-AzRecoveryServicesAsrProtectableItem** ottiene gli elementi proteggibili in un contenitore di protezione del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0558-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d0558-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0558-110">EXAMPLES</span></span>

### <span data-ttu-id="d0558-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0558-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="d0558-112">Ottiene tutti gli elementi proteggibili nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="d0558-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="d0558-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d0558-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="d0558-114">Ottenere gli elementi proteggibili nel contenitore di protezione ASR specificato e con un nome descrittivo specificato.</span><span class="sxs-lookup"><span data-stu-id="d0558-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="d0558-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d0558-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="d0558-116">Ottiene tutti gli elementi proteggibili nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="d0558-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="d0558-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0558-117">PARAMETERS</span></span>

### <span data-ttu-id="d0558-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0558-118">-DefaultProfile</span></span>
<span data-ttu-id="d0558-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0558-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d0558-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d0558-120">-FriendlyName</span></span>
<span data-ttu-id="d0558-121">Specifica il nome descrittivo dell'elemento protetto da AsR.</span><span class="sxs-lookup"><span data-stu-id="d0558-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0558-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d0558-122">-Name</span></span>
<span data-ttu-id="d0558-123">Specifica il nome dell'elemento protetto da AsR.</span><span class="sxs-lookup"><span data-stu-id="d0558-123">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0558-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d0558-124">-ProtectionContainer</span></span>
<span data-ttu-id="d0558-125">Specifica l'oggetto contenitore di Azure Site Protection.</span><span class="sxs-lookup"><span data-stu-id="d0558-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0558-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0558-126">CommonParameters</span></span>
<span data-ttu-id="d0558-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0558-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0558-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0558-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0558-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0558-129">INPUTS</span></span>

### <span data-ttu-id="d0558-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d0558-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d0558-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0558-131">OUTPUTS</span></span>

### <span data-ttu-id="d0558-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d0558-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d0558-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0558-133">NOTES</span></span>

## <span data-ttu-id="d0558-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0558-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0558-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d0558-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="d0558-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d0558-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
