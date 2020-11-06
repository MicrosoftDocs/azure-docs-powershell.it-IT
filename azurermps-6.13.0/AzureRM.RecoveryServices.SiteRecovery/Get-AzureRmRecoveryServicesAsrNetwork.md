---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514912"
---
# <span data-ttu-id="e935b-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="e935b-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="e935b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e935b-102">SYNOPSIS</span></span>
<span data-ttu-id="e935b-103">Ottiene informazioni sulle reti gestite dal ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="e935b-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e935b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e935b-104">SYNTAX</span></span>

### <span data-ttu-id="e935b-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e935b-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e935b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e935b-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e935b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e935b-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e935b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e935b-108">DESCRIPTION</span></span>
<span data-ttu-id="e935b-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrNetwork** ottiene informazioni sulle reti di ripristino dei siti di Azure per l'attuale archivio di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="e935b-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e935b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e935b-110">EXAMPLES</span></span>

### <span data-ttu-id="e935b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e935b-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="e935b-112">Ottiene tutte le reti note nel tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="e935b-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="e935b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e935b-113">PARAMETERS</span></span>

### <span data-ttu-id="e935b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e935b-114">-DefaultProfile</span></span>
<span data-ttu-id="e935b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e935b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e935b-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="e935b-116">-Fabric</span></span>
<span data-ttu-id="e935b-117">Oggetto del tessuto ASR</span><span class="sxs-lookup"><span data-stu-id="e935b-117">ASR fabric object</span></span>

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

### <span data-ttu-id="e935b-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e935b-118">-FriendlyName</span></span>
<span data-ttu-id="e935b-119">Nome descrittivo dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="e935b-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e935b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e935b-120">-Name</span></span>
<span data-ttu-id="e935b-121">Nome dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="e935b-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="e935b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e935b-122">CommonParameters</span></span>
<span data-ttu-id="e935b-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e935b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e935b-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e935b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e935b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e935b-125">INPUTS</span></span>

### <span data-ttu-id="e935b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e935b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e935b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e935b-127">OUTPUTS</span></span>

### <span data-ttu-id="e935b-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e935b-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e935b-129">Note</span><span class="sxs-lookup"><span data-stu-id="e935b-129">NOTES</span></span>

## <span data-ttu-id="e935b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e935b-130">RELATED LINKS</span></span>
