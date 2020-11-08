---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 49adcdefac7fe3f06cfd9678137dd58cff021f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018853"
---
# <span data-ttu-id="b457b-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="b457b-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="b457b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b457b-102">SYNOPSIS</span></span>
<span data-ttu-id="b457b-103">Ottiene i dettagli dei server vCenter registrati per l'individuazione nel server di configurazione specificato dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="b457b-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="b457b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b457b-104">SYNTAX</span></span>

### <span data-ttu-id="b457b-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b457b-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b457b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b457b-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b457b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b457b-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b457b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b457b-108">DESCRIPTION</span></span>
<span data-ttu-id="b457b-109">Il cmdlet **Get-AzRecoveryServicesAsrvCenter** ottiene i dettagli dei server vCenter registrati per l'individuazione nel server di configurazione specificato dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="b457b-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="b457b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b457b-110">EXAMPLES</span></span>

### <span data-ttu-id="b457b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b457b-111">Example 1</span></span>
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

<span data-ttu-id="b457b-112">Ottenere il ripristino di un sito di Azure in base al nome del tessuto e al nome di vCenter.</span><span class="sxs-lookup"><span data-stu-id="b457b-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="b457b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b457b-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="b457b-114">Ottenere l'elenco di ripristino di Azure site in base al nome Fabric.</span><span class="sxs-lookup"><span data-stu-id="b457b-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="b457b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b457b-115">PARAMETERS</span></span>

### <span data-ttu-id="b457b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b457b-116">-DefaultProfile</span></span>
<span data-ttu-id="b457b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b457b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b457b-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="b457b-118">-Fabric</span></span>
<span data-ttu-id="b457b-119">Oggetto del tessuto ASR che rappresenta il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b457b-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="b457b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b457b-120">-Name</span></span>
<span data-ttu-id="b457b-121">Nome del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="b457b-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="b457b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b457b-122">-ResourceId</span></span>
<span data-ttu-id="b457b-123">Specifica il resourceId di vCenter.</span><span class="sxs-lookup"><span data-stu-id="b457b-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="b457b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b457b-124">CommonParameters</span></span>
<span data-ttu-id="b457b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b457b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b457b-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b457b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b457b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b457b-127">INPUTS</span></span>

### <span data-ttu-id="b457b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b457b-128">System.String</span></span>

### <span data-ttu-id="b457b-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b457b-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b457b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b457b-130">OUTPUTS</span></span>

### <span data-ttu-id="b457b-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="b457b-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="b457b-132">Note</span><span class="sxs-lookup"><span data-stu-id="b457b-132">NOTES</span></span>

## <span data-ttu-id="b457b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b457b-133">RELATED LINKS</span></span>
