---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475017"
---
# <span data-ttu-id="38304-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="38304-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="38304-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38304-102">SYNOPSIS</span></span>
<span data-ttu-id="38304-103">Ottiene informazioni sui mapping di rete di ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="38304-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="38304-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38304-104">SYNTAX</span></span>

### <span data-ttu-id="38304-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38304-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38304-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="38304-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38304-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38304-107">DESCRIPTION</span></span>
<span data-ttu-id="38304-108">Il cmdlet **Get-AzRecoveryServicesAsrNetworkMapping** ottiene le informazioni sui mapping di rete di ripristino dei siti di Azure per il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="38304-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="38304-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38304-109">EXAMPLES</span></span>

### <span data-ttu-id="38304-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38304-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="38304-111">Ottiene tutti i mapping delle reti per la rete passata.</span><span class="sxs-lookup"><span data-stu-id="38304-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="38304-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38304-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="38304-113">Ottiene il mapping delle reti con il nome specificato in un tessuto di ripristino del sito Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="38304-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="38304-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38304-114">PARAMETERS</span></span>

### <span data-ttu-id="38304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38304-115">-DefaultProfile</span></span>
<span data-ttu-id="38304-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38304-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="38304-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="38304-117">-Name</span></span>
<span data-ttu-id="38304-118">Nome dell'oggetto mapping di rete ASR da ottenere.</span><span class="sxs-lookup"><span data-stu-id="38304-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="38304-119">-Rete</span><span class="sxs-lookup"><span data-stu-id="38304-119">-Network</span></span>
<span data-ttu-id="38304-120">Ottenere i mapping di rete ASR corrispondenti all'oggetto ASR di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="38304-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="38304-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="38304-121">-PrimaryFabric</span></span>
<span data-ttu-id="38304-122">Ottenere i mapping di rete ASR corrispondenti all'oggetto tessuto primario specificato.</span><span class="sxs-lookup"><span data-stu-id="38304-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="38304-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38304-123">CommonParameters</span></span>
<span data-ttu-id="38304-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38304-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38304-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38304-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38304-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38304-126">INPUTS</span></span>

### <span data-ttu-id="38304-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="38304-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="38304-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="38304-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="38304-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38304-129">OUTPUTS</span></span>

### <span data-ttu-id="38304-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="38304-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="38304-131">Note</span><span class="sxs-lookup"><span data-stu-id="38304-131">NOTES</span></span>

## <span data-ttu-id="38304-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38304-132">RELATED LINKS</span></span>

[<span data-ttu-id="38304-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="38304-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="38304-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="38304-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
