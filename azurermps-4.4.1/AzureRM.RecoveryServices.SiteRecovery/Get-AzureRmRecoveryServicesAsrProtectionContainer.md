---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521558"
---
# <span data-ttu-id="1a4ea-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a4ea-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="1a4ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4ea-103">Ottiene i contenitori di protezione ASR nel Vault di Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a4ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a4ea-104">SYNTAX</span></span>

### <span data-ttu-id="1a4ea-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a4ea-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="1a4ea-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1a4ea-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="1a4ea-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1a4ea-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="1a4ea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a4ea-108">DESCRIPTION</span></span>
<span data-ttu-id="1a4ea-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrProtectionContainer** ottiene i contenitori di protezione dal ripristino dei siti di Azure nell'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="1a4ea-110">Un contenitore di protezione è un contenitore logico per gli oggetti protetti (rilevati) e per le protezioni, ad esempio le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="1a4ea-111">I criteri di replica definiscono le impostazioni di replica per gli elementi protetti e possono essere associati a un contenitore di protezione e applicati a un elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="1a4ea-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a4ea-112">EXAMPLES</span></span>

### <span data-ttu-id="1a4ea-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a4ea-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="1a4ea-114">Ottiene tutti i contenitori di protezione ASR nel tessuto ASR specificato (l'input della pipeline nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="1a4ea-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="1a4ea-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a4ea-115">PARAMETERS</span></span>

### <span data-ttu-id="1a4ea-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="1a4ea-116">-Fabric</span></span>
<span data-ttu-id="1a4ea-117">Cercare il contenitore di protezione nel tessuto ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-117">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="1a4ea-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1a4ea-118">-FriendlyName</span></span>
<span data-ttu-id="1a4ea-119">Specifica il nome descrittivo del contenitore di protezione ASR da cercare.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="1a4ea-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a4ea-120">-Name</span></span>
<span data-ttu-id="1a4ea-121">Specifica il nome del contenitore di protezione ASR da cercare.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="1a4ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4ea-122">CommonParameters</span></span>
<span data-ttu-id="1a4ea-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a4ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4ea-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a4ea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4ea-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a4ea-125">INPUTS</span></span>

### <span data-ttu-id="1a4ea-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="1a4ea-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="1a4ea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a4ea-127">OUTPUTS</span></span>

### <span data-ttu-id="1a4ea-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a4ea-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1a4ea-129">Note</span><span class="sxs-lookup"><span data-stu-id="1a4ea-129">NOTES</span></span>

## <span data-ttu-id="1a4ea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a4ea-130">RELATED LINKS</span></span>

