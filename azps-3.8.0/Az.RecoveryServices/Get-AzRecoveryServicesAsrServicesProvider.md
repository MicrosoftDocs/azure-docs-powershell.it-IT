---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 4be24acddf1f02ecd9216a06690958feed2d6c57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018566"
---
# <span data-ttu-id="8de52-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8de52-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="8de52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8de52-102">SYNOPSIS</span></span>
<span data-ttu-id="8de52-103">Ottiene i dettagli dei provider di servizi di ripristino ASR registrati nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8de52-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="8de52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8de52-104">SYNTAX</span></span>

### <span data-ttu-id="8de52-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8de52-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8de52-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8de52-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8de52-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8de52-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8de52-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8de52-108">DESCRIPTION</span></span>
<span data-ttu-id="8de52-109">Il cmdlet **Get-AzRecoveryServicesAsrServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="8de52-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="8de52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8de52-110">EXAMPLES</span></span>

### <span data-ttu-id="8de52-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8de52-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="8de52-112">Elenca tutti i provider di servizi di replica ASR registrati nel Vault di servizi di ripristino che corrispondono al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="8de52-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="8de52-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8de52-113">PARAMETERS</span></span>

### <span data-ttu-id="8de52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de52-114">-DefaultProfile</span></span>
<span data-ttu-id="8de52-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8de52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8de52-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="8de52-116">-Fabric</span></span>
<span data-ttu-id="8de52-117">Specifica l'oggetto del tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="8de52-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="8de52-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8de52-118">-FriendlyName</span></span>
<span data-ttu-id="8de52-119">Specifica il nome descrittivo del provider di servizi di ripristino ASR per ottenere informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="8de52-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="8de52-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8de52-120">-Name</span></span>
<span data-ttu-id="8de52-121">Specifica il nome del provider di servizi di ripristino ASR per cui ottenere i dettagli.</span><span class="sxs-lookup"><span data-stu-id="8de52-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="8de52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de52-122">CommonParameters</span></span>
<span data-ttu-id="8de52-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de52-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de52-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8de52-125">INPUTS</span></span>

### <span data-ttu-id="8de52-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8de52-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8de52-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8de52-127">OUTPUTS</span></span>

### <span data-ttu-id="8de52-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8de52-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="8de52-129">Note</span><span class="sxs-lookup"><span data-stu-id="8de52-129">NOTES</span></span>

## <span data-ttu-id="8de52-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8de52-130">RELATED LINKS</span></span>

[<span data-ttu-id="8de52-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8de52-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="8de52-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8de52-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
