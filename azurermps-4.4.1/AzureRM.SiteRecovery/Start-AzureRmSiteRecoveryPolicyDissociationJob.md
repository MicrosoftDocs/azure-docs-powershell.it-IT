---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4F71DC85-B2E0-4E0B-96F6-69D52C577B22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyDissociationJob.md
ms.openlocfilehash: 7dc64ea2bdbfb5dcbc648143dd094313eb765782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512875"
---
# <span data-ttu-id="3436d-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span><span class="sxs-lookup"><span data-stu-id="3436d-101">Start-AzureRmSiteRecoveryPolicyDissociationJob</span></span>

## <span data-ttu-id="3436d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3436d-102">SYNOPSIS</span></span>
<span data-ttu-id="3436d-103">Avvia un processo di dissociazione in un criterio di replica associato a un contenitore di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="3436d-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3436d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3436d-104">SYNTAX</span></span>

### <span data-ttu-id="3436d-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3436d-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3436d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3436d-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyDissociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3436d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3436d-107">DESCRIPTION</span></span>
<span data-ttu-id="3436d-108">Il cmdlet **Start-AzureRmSiteRecoveryPolicyDissociationJob** avvia un processo di dissociazione sui criteri di replica associati a un contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="3436d-108">The **Start-AzureRmSiteRecoveryPolicyDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="3436d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3436d-109">EXAMPLES</span></span>

## <span data-ttu-id="3436d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3436d-110">PARAMETERS</span></span>

### <span data-ttu-id="3436d-111">-Policy</span><span class="sxs-lookup"><span data-stu-id="3436d-111">-Policy</span></span>
<span data-ttu-id="3436d-112">Specifica un oggetto Criteri di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="3436d-112">Specifies an Azure Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3436d-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3436d-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="3436d-114">Specifica un contenitore di protezione principale.</span><span class="sxs-lookup"><span data-stu-id="3436d-114">Specifies a primary protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3436d-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3436d-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="3436d-116">Specifica un contenitore di protezione per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="3436d-116">Specifies a recovery protection container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3436d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3436d-117">-DefaultProfile</span></span>
<span data-ttu-id="3436d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3436d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3436d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3436d-119">CommonParameters</span></span>
<span data-ttu-id="3436d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3436d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3436d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3436d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3436d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3436d-122">INPUTS</span></span>

### <span data-ttu-id="3436d-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="3436d-123">ASRPolicy</span></span>
<span data-ttu-id="3436d-124">Il parametro ' Policy ' accetta il valore di tipo ' ASRPolicy ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3436d-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="3436d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3436d-125">OUTPUTS</span></span>

### <span data-ttu-id="3436d-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3436d-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3436d-127">Note</span><span class="sxs-lookup"><span data-stu-id="3436d-127">NOTES</span></span>

## <span data-ttu-id="3436d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3436d-128">RELATED LINKS</span></span>

