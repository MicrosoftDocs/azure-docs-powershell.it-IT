---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: e344dd4b5284a29c84b4f4c4b90d5a99f5d8d4ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855801"
---
# <span data-ttu-id="d2714-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="d2714-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="d2714-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2714-102">SYNOPSIS</span></span>
<span data-ttu-id="d2714-103">Ottiene informazioni sulle reti gestite dal ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="d2714-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="d2714-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2714-104">SYNTAX</span></span>

### <span data-ttu-id="d2714-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2714-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2714-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d2714-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2714-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d2714-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2714-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2714-108">DESCRIPTION</span></span>
<span data-ttu-id="d2714-109">Il cmdlet **Get-AzRecoveryServicesAsrNetwork** ottiene informazioni sulle reti di ripristino dei siti di Azure per l'attuale archivio di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="d2714-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d2714-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2714-110">EXAMPLES</span></span>

### <span data-ttu-id="d2714-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2714-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="d2714-112">Ottiene tutte le reti note nel tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="d2714-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="d2714-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2714-113">PARAMETERS</span></span>

### <span data-ttu-id="d2714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2714-114">-DefaultProfile</span></span>
<span data-ttu-id="d2714-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2714-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d2714-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="d2714-116">-Fabric</span></span>
<span data-ttu-id="d2714-117">Oggetto del tessuto ASR</span><span class="sxs-lookup"><span data-stu-id="d2714-117">ASR fabric object</span></span>

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

### <span data-ttu-id="d2714-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d2714-118">-FriendlyName</span></span>
<span data-ttu-id="d2714-119">Nome descrittivo dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="d2714-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="d2714-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2714-120">-Name</span></span>
<span data-ttu-id="d2714-121">Nome dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="d2714-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="d2714-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2714-122">CommonParameters</span></span>
<span data-ttu-id="d2714-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2714-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2714-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2714-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2714-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2714-125">INPUTS</span></span>

### <span data-ttu-id="d2714-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d2714-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d2714-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2714-127">OUTPUTS</span></span>

### <span data-ttu-id="d2714-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="d2714-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="d2714-129">Note</span><span class="sxs-lookup"><span data-stu-id="d2714-129">NOTES</span></span>

## <span data-ttu-id="d2714-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2714-130">RELATED LINKS</span></span>
