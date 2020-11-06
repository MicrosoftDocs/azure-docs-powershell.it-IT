---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 689f432f117e67a3770518a3b2e86f1678f3662b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518052"
---
# <span data-ttu-id="067bc-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="067bc-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="067bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="067bc-102">SYNOPSIS</span></span>
<span data-ttu-id="067bc-103">Ottiene i dettagli dei server vCenter registrati per l'individuazione nel server di configurazione specificato dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="067bc-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="067bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="067bc-104">SYNTAX</span></span>

### <span data-ttu-id="067bc-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="067bc-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="067bc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="067bc-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="067bc-107">ByName</span><span class="sxs-lookup"><span data-stu-id="067bc-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="067bc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="067bc-108">DESCRIPTION</span></span>
<span data-ttu-id="067bc-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrvCenter** ottiene i dettagli dei server vCenter registrati per l'individuazione nel server di configurazione specificato dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="067bc-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="067bc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="067bc-110">EXAMPLES</span></span>

### <span data-ttu-id="067bc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="067bc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="067bc-112">Ottenere il ripristino di un sito di Azure in base al nome del tessuto e al nome di vCenter.</span><span class="sxs-lookup"><span data-stu-id="067bc-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="067bc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="067bc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="067bc-114">Ottenere l'elenco di ripristino di Azure site in base al nome Fabric.</span><span class="sxs-lookup"><span data-stu-id="067bc-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="067bc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="067bc-115">PARAMETERS</span></span>

### <span data-ttu-id="067bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067bc-116">-DefaultProfile</span></span>
<span data-ttu-id="067bc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="067bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="067bc-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="067bc-118">-Fabric</span></span>
<span data-ttu-id="067bc-119">Oggetto del tessuto ASR che rappresenta il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="067bc-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="067bc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="067bc-120">-Name</span></span>
<span data-ttu-id="067bc-121">Nome del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="067bc-121">Name of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="067bc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="067bc-122">-ResourceId</span></span>
<span data-ttu-id="067bc-123">Specifica il resourceId di vCenter.</span><span class="sxs-lookup"><span data-stu-id="067bc-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="067bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067bc-124">CommonParameters</span></span>
<span data-ttu-id="067bc-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="067bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067bc-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="067bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067bc-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="067bc-127">INPUTS</span></span>

### <span data-ttu-id="067bc-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="067bc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="067bc-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="067bc-129">OUTPUTS</span></span>

### <span data-ttu-id="067bc-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="067bc-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="067bc-131">Note</span><span class="sxs-lookup"><span data-stu-id="067bc-131">NOTES</span></span>

## <span data-ttu-id="067bc-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="067bc-132">RELATED LINKS</span></span>
