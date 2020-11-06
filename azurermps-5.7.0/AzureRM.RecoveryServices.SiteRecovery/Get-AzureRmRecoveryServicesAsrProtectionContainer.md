---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 5862d76c574b469d3bc0e559892b505e1b90beab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512423"
---
# <span data-ttu-id="f4f84-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f4f84-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f4f84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4f84-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f84-103">Ottiene i contenitori di protezione ASR nel Vault di Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="f4f84-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4f84-104">SYNTAX</span></span>

### <span data-ttu-id="f4f84-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4f84-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f84-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f4f84-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f84-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f4f84-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f84-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4f84-108">DESCRIPTION</span></span>
<span data-ttu-id="f4f84-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainer** ottiene i contenitori di protezione dal ripristino dei siti di Azure nell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f4f84-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="f4f84-110">Un contenitore di protezione è un contenitore logico per gli oggetti protetti (rilevati) e per le protezioni, ad esempio le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f4f84-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="f4f84-111">I criteri di replica definiscono le impostazioni di replica per gli elementi protetti e possono essere associati a un contenitore di protezione e applicati a un elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="f4f84-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="f4f84-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4f84-112">EXAMPLES</span></span>

### <span data-ttu-id="f4f84-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4f84-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="f4f84-114">Elenco dei contenitori di protezione in tessuto $fabric.</span><span class="sxs-lookup"><span data-stu-id="f4f84-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="f4f84-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f4f84-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="f4f84-116">Contenitore di protezione in tessuto $fabric con nome.</span><span class="sxs-lookup"><span data-stu-id="f4f84-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="f4f84-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f4f84-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="f4f84-118">Contenitore di protezione in tessuto $fabric con nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="f4f84-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="f4f84-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4f84-119">PARAMETERS</span></span>

### <span data-ttu-id="f4f84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f84-120">-DefaultProfile</span></span>
<span data-ttu-id="f4f84-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f4f84-122">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="f4f84-122">-Fabric</span></span>
<span data-ttu-id="f4f84-123">Cercare il contenitore di protezione nel tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="f4f84-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f84-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f4f84-124">-FriendlyName</span></span>
<span data-ttu-id="f4f84-125">Specifica il nome descrittivo del contenitore di protezione ASR da cercare.</span><span class="sxs-lookup"><span data-stu-id="f4f84-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f84-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4f84-126">-Name</span></span>
<span data-ttu-id="f4f84-127">Specifica il nome del contenitore di protezione ASR da cercare.</span><span class="sxs-lookup"><span data-stu-id="f4f84-127">Specifies the name of the ASR protection container to look for.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f84-128">CommonParameters</span></span>
<span data-ttu-id="f4f84-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f84-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f84-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f84-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4f84-131">INPUTS</span></span>

### <span data-ttu-id="f4f84-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="f4f84-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f4f84-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4f84-133">OUTPUTS</span></span>

### <span data-ttu-id="f4f84-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f4f84-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f4f84-135">Note</span><span class="sxs-lookup"><span data-stu-id="f4f84-135">NOTES</span></span>

## <span data-ttu-id="f4f84-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4f84-136">RELATED LINKS</span></span>
