---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193038"
---
# <span data-ttu-id="cc287-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cc287-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="cc287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc287-102">SYNOPSIS</span></span>
<span data-ttu-id="cc287-103">Recupera informazioni sui mapping di rete di Ripristino siti per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="cc287-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="cc287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc287-104">SYNTAX</span></span>

### <span data-ttu-id="cc287-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc287-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc287-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="cc287-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc287-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cc287-107">DESCRIPTION</span></span>
<span data-ttu-id="cc287-108">Il cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** ottiene informazioni sui mapping di rete di Azure Site Recovery per il vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cc287-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="cc287-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc287-109">EXAMPLES</span></span>

### <span data-ttu-id="cc287-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc287-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="cc287-111">Recupera tutti i mapping di rete per la rete passata.</span><span class="sxs-lookup"><span data-stu-id="cc287-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="cc287-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cc287-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="cc287-113">Recupera il mapping delle reti con il nome fornito nell'infrastruttura di ripristino del sito di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="cc287-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="cc287-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc287-114">PARAMETERS</span></span>

### <span data-ttu-id="cc287-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc287-115">-DefaultProfile</span></span>
<span data-ttu-id="cc287-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc287-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cc287-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc287-117">-Name</span></span>
<span data-ttu-id="cc287-118">Nome dell'oggetto mapping di rete ASR da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cc287-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc287-119">-Rete</span><span class="sxs-lookup"><span data-stu-id="cc287-119">-Network</span></span>
<span data-ttu-id="cc287-120">Ottenere i mapping di rete ASR corrispondenti all'oggetto ASR di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="cc287-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc287-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="cc287-121">-PrimaryFabric</span></span>
<span data-ttu-id="cc287-122">Ottenere i mapping di rete ASR corrispondenti all'oggetto tessuto primario specificato.</span><span class="sxs-lookup"><span data-stu-id="cc287-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc287-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc287-123">CommonParameters</span></span>
<span data-ttu-id="cc287-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc287-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc287-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc287-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc287-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="cc287-126">INPUTS</span></span>

### <span data-ttu-id="cc287-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="cc287-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="cc287-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="cc287-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="cc287-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc287-129">OUTPUTS</span></span>

### <span data-ttu-id="cc287-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cc287-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="cc287-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="cc287-131">NOTES</span></span>

## <span data-ttu-id="cc287-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc287-132">RELATED LINKS</span></span>

[<span data-ttu-id="cc287-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cc287-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="cc287-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="cc287-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
