---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c9c50e26e99493fb693b8bded693bceb24f5a40f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476763"
---
# <span data-ttu-id="d923b-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d923b-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="d923b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d923b-102">SYNOPSIS</span></span>
<span data-ttu-id="d923b-103">Ottenere gli elementi protettivi in un contenitore di protezione ASR.</span><span class="sxs-lookup"><span data-stu-id="d923b-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="d923b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d923b-104">SYNTAX</span></span>

### <span data-ttu-id="d923b-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d923b-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d923b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d923b-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d923b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d923b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d923b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d923b-108">DESCRIPTION</span></span>
<span data-ttu-id="d923b-109">Il cmdlet **Get-AzRecoveryServicesAsrProtectableItem** ottiene gli elementi protettivi in un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="d923b-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d923b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d923b-110">EXAMPLES</span></span>

### <span data-ttu-id="d923b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d923b-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="d923b-112">Ottiene tutti gli elementi protettivi nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="d923b-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="d923b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d923b-113">Example 2</span></span>
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

<span data-ttu-id="d923b-114">Ottenere gli elementi protettivi nel contenitore di protezione ASR specificato e con il nome descrittivo indicato.</span><span class="sxs-lookup"><span data-stu-id="d923b-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="d923b-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d923b-115">Example 3</span></span>
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

<span data-ttu-id="d923b-116">Ottiene tutti gli elementi protettivi nel contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="d923b-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="d923b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d923b-117">PARAMETERS</span></span>

### <span data-ttu-id="d923b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d923b-118">-DefaultProfile</span></span>
<span data-ttu-id="d923b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d923b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d923b-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d923b-120">-FriendlyName</span></span>
<span data-ttu-id="d923b-121">Specifica il nome descrittivo dell'elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="d923b-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="d923b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d923b-122">-Name</span></span>
<span data-ttu-id="d923b-123">Specifica il nome dell'elemento protetto da ASR.</span><span class="sxs-lookup"><span data-stu-id="d923b-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="d923b-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d923b-124">-ProtectionContainer</span></span>
<span data-ttu-id="d923b-125">Specifica l'oggetto contenitore di protezione per il ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d923b-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="d923b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d923b-126">CommonParameters</span></span>
<span data-ttu-id="d923b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d923b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d923b-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d923b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d923b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d923b-129">INPUTS</span></span>

### <span data-ttu-id="d923b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d923b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d923b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d923b-131">OUTPUTS</span></span>

### <span data-ttu-id="d923b-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d923b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d923b-133">Note</span><span class="sxs-lookup"><span data-stu-id="d923b-133">NOTES</span></span>

## <span data-ttu-id="d923b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d923b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d923b-135">Get-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d923b-135">Get-AzRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="d923b-136">Set-AzRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="d923b-136">Set-AzRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzRecoveryServicesAsrProtectionEntity.md)
