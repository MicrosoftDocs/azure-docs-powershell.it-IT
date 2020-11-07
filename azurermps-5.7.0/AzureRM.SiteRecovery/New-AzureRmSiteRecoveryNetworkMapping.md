---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 36f5c6e535cc67029fac7c951cbc6dbbe3c73091
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687431"
---
# <span data-ttu-id="00124-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00124-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="00124-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00124-102">SYNOPSIS</span></span>
<span data-ttu-id="00124-103">Crea un mapping tra reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="00124-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00124-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00124-104">SYNTAX</span></span>

### <span data-ttu-id="00124-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="00124-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00124-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="00124-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00124-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00124-107">DESCRIPTION</span></span>
<span data-ttu-id="00124-108">Il cmdlet **New-AzureRMSiteRecoveryNetworkMapping** crea un mapping tra due reti virtuali e restituisce un processo di ripristino del sito di Azure per monitorarlo.</span><span class="sxs-lookup"><span data-stu-id="00124-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="00124-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00124-109">EXAMPLES</span></span>

## <span data-ttu-id="00124-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00124-110">PARAMETERS</span></span>

### <span data-ttu-id="00124-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="00124-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="00124-112">Specifica l'ID rete virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="00124-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00124-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00124-113">-DefaultProfile</span></span>
<span data-ttu-id="00124-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00124-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00124-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="00124-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00124-116">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="00124-116">-PrimaryNetwork</span></span>
<span data-ttu-id="00124-117">Specifica l'oggetto di rete principale.</span><span class="sxs-lookup"><span data-stu-id="00124-117">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00124-118">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="00124-118">-RecoveryNetwork</span></span>
<span data-ttu-id="00124-119">Specifica l'oggetto rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="00124-119">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00124-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00124-120">CommonParameters</span></span>
<span data-ttu-id="00124-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00124-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00124-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00124-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00124-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00124-123">INPUTS</span></span>

### <span data-ttu-id="00124-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="00124-124">ASRNetwork</span></span>
<span data-ttu-id="00124-125">Il parametro ' PrimaryNetwork ' accetta il valore di tipo ' ASRNetwork ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="00124-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="00124-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00124-126">OUTPUTS</span></span>

### <span data-ttu-id="00124-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="00124-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="00124-128">Note</span><span class="sxs-lookup"><span data-stu-id="00124-128">NOTES</span></span>

## <span data-ttu-id="00124-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00124-129">RELATED LINKS</span></span>

[<span data-ttu-id="00124-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00124-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="00124-131">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00124-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
