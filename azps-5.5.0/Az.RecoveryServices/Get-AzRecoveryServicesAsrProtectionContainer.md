---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6db09c69d112e2638026fde97d586f7945f0508e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202047"
---
# <span data-ttu-id="c737f-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c737f-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="c737f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c737f-102">SYNOPSIS</span></span>
<span data-ttu-id="c737f-103">Recupera i contenitori di protezione asr nel Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c737f-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="c737f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c737f-104">SYNTAX</span></span>

### <span data-ttu-id="c737f-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c737f-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c737f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="c737f-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c737f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="c737f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c737f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c737f-108">DESCRIPTION</span></span>
<span data-ttu-id="c737f-109">Il cmdlet **Get-AzRecoveryServicesAsrProtectionContainer** ottiene i contenitori di protezione di Azure Site Recovery nel vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c737f-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="c737f-110">Un contenitore di protezione è un contenitore logico per oggetti proteggibili(individuati) e protetti come le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="c737f-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="c737f-111">I criteri di replica definiscono le impostazioni di replica per gli elementi protetti e possono essere associati a un contenitore di protezione e applicati a un elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="c737f-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="c737f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c737f-112">EXAMPLES</span></span>

### <span data-ttu-id="c737f-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c737f-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="c737f-114">Elenco di contenitori di protezione in tessuto $fabric.</span><span class="sxs-lookup"><span data-stu-id="c737f-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="c737f-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c737f-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="c737f-116">Contenitore di protezione in tessuto $fabric nome.</span><span class="sxs-lookup"><span data-stu-id="c737f-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="c737f-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c737f-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="c737f-118">Contenitore di protezione in tessuto $fabric nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="c737f-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="c737f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c737f-119">PARAMETERS</span></span>

### <span data-ttu-id="c737f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c737f-120">-DefaultProfile</span></span>
<span data-ttu-id="c737f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c737f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c737f-122">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="c737f-122">-Fabric</span></span>
<span data-ttu-id="c737f-123">Cercare il contenitore di protezione nel tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="c737f-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c737f-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c737f-124">-FriendlyName</span></span>
<span data-ttu-id="c737f-125">Specifica il nome descrittivo del contenitore di protezione ASR da cercare.</span><span class="sxs-lookup"><span data-stu-id="c737f-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c737f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c737f-126">-Name</span></span>
<span data-ttu-id="c737f-127">Specifica il nome del contenitore di protezione ASR da cercare.</span><span class="sxs-lookup"><span data-stu-id="c737f-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="c737f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c737f-128">CommonParameters</span></span>
<span data-ttu-id="c737f-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c737f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c737f-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c737f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c737f-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c737f-131">INPUTS</span></span>

### <span data-ttu-id="c737f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="c737f-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="c737f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c737f-133">OUTPUTS</span></span>

### <span data-ttu-id="c737f-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c737f-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c737f-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c737f-135">NOTES</span></span>

## <span data-ttu-id="c737f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c737f-136">RELATED LINKS</span></span>
