---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverypolicyassociationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 140bec7738d107574db5d0d157cc3f8cfac46583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687415"
---
# <span data-ttu-id="afd11-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="afd11-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="afd11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afd11-102">SYNOPSIS</span></span>
<span data-ttu-id="afd11-103">Avvia un processo di associazione dei criteri di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="afd11-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afd11-104">SYNTAX</span></span>

### <span data-ttu-id="afd11-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afd11-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="afd11-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="afd11-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afd11-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afd11-107">DESCRIPTION</span></span>
<span data-ttu-id="afd11-108">Il cmdlet **Start-AzureRmSiteRecoveryPolicyAssociationJob** avvia un processo di associazione per associare un criterio di replica con un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="afd11-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="afd11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afd11-109">EXAMPLES</span></span>

## <span data-ttu-id="afd11-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afd11-110">PARAMETERS</span></span>

### <span data-ttu-id="afd11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd11-111">-DefaultProfile</span></span>
<span data-ttu-id="afd11-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afd11-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd11-113">-Policy</span><span class="sxs-lookup"><span data-stu-id="afd11-113">-Policy</span></span>
<span data-ttu-id="afd11-114">Specifica l'oggetto Criteri di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="afd11-114">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afd11-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="afd11-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="afd11-116">Specifica il contenitore di protezione principale in cui applicare le impostazioni del profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="afd11-116">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd11-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="afd11-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="afd11-118">Specifica il contenitore di protezione per il recupero in cui applicare le impostazioni del profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="afd11-118">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd11-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd11-119">CommonParameters</span></span>
<span data-ttu-id="afd11-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd11-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd11-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd11-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd11-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afd11-122">INPUTS</span></span>

### <span data-ttu-id="afd11-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="afd11-123">ASRPolicy</span></span>
<span data-ttu-id="afd11-124">Il parametro ' Policy ' accetta il valore di tipo ' ASRPolicy ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="afd11-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="afd11-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afd11-125">OUTPUTS</span></span>

### <span data-ttu-id="afd11-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="afd11-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="afd11-127">Note</span><span class="sxs-lookup"><span data-stu-id="afd11-127">NOTES</span></span>

## <span data-ttu-id="afd11-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afd11-128">RELATED LINKS</span></span>

