---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202063"
---
# <span data-ttu-id="28c1e-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="28c1e-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="28c1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="28c1e-103">Recupera informazioni sulle reti gestite da Ripristino siti per il vault corrente.</span><span class="sxs-lookup"><span data-stu-id="28c1e-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="28c1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28c1e-104">SYNTAX</span></span>

### <span data-ttu-id="28c1e-105">ByFabricObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28c1e-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28c1e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="28c1e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28c1e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="28c1e-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28c1e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28c1e-108">DESCRIPTION</span></span>
<span data-ttu-id="28c1e-109">Il cmdlet **Get-AzRecoveryServicesAsrNetwork** ottiene informazioni sulle reti di Ripristino siti di Azure per l'attuale vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="28c1e-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="28c1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28c1e-110">EXAMPLES</span></span>

### <span data-ttu-id="28c1e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28c1e-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="28c1e-112">Recupera tutte le reti note nel tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="28c1e-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="28c1e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28c1e-113">PARAMETERS</span></span>

### <span data-ttu-id="28c1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c1e-114">-DefaultProfile</span></span>
<span data-ttu-id="28c1e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28c1e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="28c1e-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="28c1e-116">-Fabric</span></span>
<span data-ttu-id="28c1e-117">Oggetto tessuto ASR</span><span class="sxs-lookup"><span data-stu-id="28c1e-117">ASR fabric object</span></span>

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

### <span data-ttu-id="28c1e-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="28c1e-118">-FriendlyName</span></span>
<span data-ttu-id="28c1e-119">Nome descrittivo dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="28c1e-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="28c1e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="28c1e-120">-Name</span></span>
<span data-ttu-id="28c1e-121">Nome dell'oggetto ASR di rete.</span><span class="sxs-lookup"><span data-stu-id="28c1e-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="28c1e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c1e-122">CommonParameters</span></span>
<span data-ttu-id="28c1e-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c1e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c1e-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28c1e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c1e-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="28c1e-125">INPUTS</span></span>

### <span data-ttu-id="28c1e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="28c1e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="28c1e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28c1e-127">OUTPUTS</span></span>

### <span data-ttu-id="28c1e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="28c1e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="28c1e-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="28c1e-129">NOTES</span></span>

## <span data-ttu-id="28c1e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28c1e-130">RELATED LINKS</span></span>
