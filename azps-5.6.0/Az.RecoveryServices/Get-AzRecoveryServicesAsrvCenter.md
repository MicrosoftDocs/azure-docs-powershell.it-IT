---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: eb358a0caf2b1ea5ccba8d92c39562d2c39706c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995299"
---
# <span data-ttu-id="6c4b3-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="6c4b3-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="6c4b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4b3-103">Recupera i dettagli dei server vCenter registrati per l'individuazione nel server di configurazione specificato dall'infrastruttura ASR.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="6c4b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c4b3-104">SYNTAX</span></span>

### <span data-ttu-id="6c4b3-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c4b3-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c4b3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4b3-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c4b3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6c4b3-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c4b3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c4b3-108">DESCRIPTION</span></span>
<span data-ttu-id="6c4b3-109">Il cmdlet **Get-AzRecoveryServicesAsrvCenter** ottiene i dettagli dei server vCenter registrati per l'individuazione nel server di configurazione specificato dall'infrastruttura ASR.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="6c4b3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c4b3-110">EXAMPLES</span></span>

### <span data-ttu-id="6c4b3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c4b3-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="6c4b3-112">Ottenere il vCenter di ripristino del sito di Azure in base al nome del tessuto e al nome del vCenter.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="6c4b3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6c4b3-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="6c4b3-114">Ottenere l'elenco del vCenter di ripristino del sito di Azure in base al nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="6c4b3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c4b3-115">PARAMETERS</span></span>

### <span data-ttu-id="6c4b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4b3-116">-DefaultProfile</span></span>
<span data-ttu-id="6c4b3-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c4b3-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="6c4b3-118">-Fabric</span></span>
<span data-ttu-id="6c4b3-119">Oggetto tessuto ASR che rappresenta il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6c4b3-120">-Name</span></span>
<span data-ttu-id="6c4b3-121">Nome del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4b3-122">-ResourceId</span></span>
<span data-ttu-id="6c4b3-123">Specifica il valore resourceId del vCenter.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4b3-124">CommonParameters</span></span>
<span data-ttu-id="6c4b3-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4b3-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c4b3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4b3-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c4b3-127">INPUTS</span></span>

### <span data-ttu-id="6c4b3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6c4b3-128">System.String</span></span>

### <span data-ttu-id="6c4b3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6c4b3-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6c4b3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c4b3-130">OUTPUTS</span></span>

### <span data-ttu-id="6c4b3-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="6c4b3-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="6c4b3-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c4b3-132">NOTES</span></span>

## <span data-ttu-id="6c4b3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c4b3-133">RELATED LINKS</span></span>
