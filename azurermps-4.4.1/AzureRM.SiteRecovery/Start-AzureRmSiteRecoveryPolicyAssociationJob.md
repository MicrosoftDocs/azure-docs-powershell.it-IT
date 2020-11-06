---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3DDC8DD8-889C-4C76-B32E-3D2C2AD0AC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPolicyAssociationJob.md
ms.openlocfilehash: 477f31ea84c5cb3e9c06b79e1ae70f5ae8a93925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519963"
---
# <span data-ttu-id="0bf45-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span><span class="sxs-lookup"><span data-stu-id="0bf45-101">Start-AzureRmSiteRecoveryPolicyAssociationJob</span></span>

## <span data-ttu-id="0bf45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bf45-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf45-103">Avvia un processo di associazione dei criteri di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0bf45-103">Starts a Site Recovery replication policy association job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bf45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bf45-104">SYNTAX</span></span>

### <span data-ttu-id="0bf45-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bf45-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0bf45-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="0bf45-106">EnterpriseToEnterprise</span></span>
```
Start-AzureRmSiteRecoveryPolicyAssociationJob -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf45-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bf45-107">DESCRIPTION</span></span>
<span data-ttu-id="0bf45-108">Il cmdlet **Start-AzureRmSiteRecoveryPolicyAssociationJob** avvia un processo di associazione per associare un criterio di replica con un contenitore di protezione per il ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="0bf45-108">The **Start-AzureRmSiteRecoveryPolicyAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="0bf45-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bf45-109">EXAMPLES</span></span>

## <span data-ttu-id="0bf45-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bf45-110">PARAMETERS</span></span>

### <span data-ttu-id="0bf45-111">-Policy</span><span class="sxs-lookup"><span data-stu-id="0bf45-111">-Policy</span></span>
<span data-ttu-id="0bf45-112">Specifica l'oggetto Criteri di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0bf45-112">Specifies the Site Recovery policy object.</span></span>

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

### <span data-ttu-id="0bf45-113">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0bf45-113">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="0bf45-114">Specifica il contenitore di protezione principale in cui applicare le impostazioni del profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="0bf45-114">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="0bf45-115">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0bf45-115">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="0bf45-116">Specifica il contenitore di protezione per il recupero in cui applicare le impostazioni del profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="0bf45-116">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

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

### <span data-ttu-id="0bf45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf45-117">-DefaultProfile</span></span>
<span data-ttu-id="0bf45-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bf45-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bf45-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf45-119">CommonParameters</span></span>
<span data-ttu-id="0bf45-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf45-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf45-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bf45-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf45-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bf45-122">INPUTS</span></span>

### <span data-ttu-id="0bf45-123">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf45-123">ASRPolicy</span></span>
<span data-ttu-id="0bf45-124">Il parametro ' Policy ' accetta il valore di tipo ' ASRPolicy ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0bf45-124">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="0bf45-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bf45-125">OUTPUTS</span></span>

### <span data-ttu-id="0bf45-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0bf45-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0bf45-127">Note</span><span class="sxs-lookup"><span data-stu-id="0bf45-127">NOTES</span></span>

## <span data-ttu-id="0bf45-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bf45-128">RELATED LINKS</span></span>

