---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 80e5e698183cdba8489f0978c5b34ee7be575140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677682"
---
# <span data-ttu-id="ed379-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ed379-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="ed379-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed379-102">SYNOPSIS</span></span>
<span data-ttu-id="ed379-103">Ottiene i dettagli dei provider di servizi di ripristino ASR registrati nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ed379-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="ed379-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed379-104">SYNTAX</span></span>

### <span data-ttu-id="ed379-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed379-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed379-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ed379-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed379-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed379-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed379-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed379-108">DESCRIPTION</span></span>
<span data-ttu-id="ed379-109">Il cmdlet **Get-AzRecoveryServicesAsrServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="ed379-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="ed379-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed379-110">EXAMPLES</span></span>

### <span data-ttu-id="ed379-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed379-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="ed379-112">Elenca tutti i provider di servizi di replica ASR registrati nel Vault di servizi di ripristino che corrispondono al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="ed379-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="ed379-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed379-113">PARAMETERS</span></span>

### <span data-ttu-id="ed379-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed379-114">-DefaultProfile</span></span>
<span data-ttu-id="ed379-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed379-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ed379-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="ed379-116">-Fabric</span></span>
<span data-ttu-id="ed379-117">Specifica l'oggetto del tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="ed379-117">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="ed379-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed379-118">-FriendlyName</span></span>
<span data-ttu-id="ed379-119">Specifica il nome descrittivo del provider di servizi di ripristino ASR per ottenere informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="ed379-119">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="ed379-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed379-120">-Name</span></span>
<span data-ttu-id="ed379-121">Specifica il nome del provider di servizi di ripristino ASR per cui ottenere i dettagli.</span><span class="sxs-lookup"><span data-stu-id="ed379-121">Specifies the name of the ASR recovery services provider to get details for.</span></span>

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

### <span data-ttu-id="ed379-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed379-122">CommonParameters</span></span>
<span data-ttu-id="ed379-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed379-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed379-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed379-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed379-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed379-125">INPUTS</span></span>

### <span data-ttu-id="ed379-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ed379-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ed379-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed379-127">OUTPUTS</span></span>

### <span data-ttu-id="ed379-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ed379-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="ed379-129">Note</span><span class="sxs-lookup"><span data-stu-id="ed379-129">NOTES</span></span>

## <span data-ttu-id="ed379-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed379-130">RELATED LINKS</span></span>

[<span data-ttu-id="ed379-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ed379-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="ed379-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ed379-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)