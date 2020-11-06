---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 79ad35a00fcd0aef62e99a217071589e10f973c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512872"
---
# <span data-ttu-id="7a529-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7a529-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="7a529-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a529-102">SYNOPSIS</span></span>
<span data-ttu-id="7a529-103">Interrompe un processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="7a529-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a529-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a529-104">SYNTAX</span></span>

### <span data-ttu-id="7a529-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a529-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a529-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7a529-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a529-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a529-107">DESCRIPTION</span></span>
<span data-ttu-id="7a529-108">Il cmdlet **Stop-AzureRmSiteRecoveryJob** arresta un processo di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="7a529-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="7a529-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a529-109">EXAMPLES</span></span>

## <span data-ttu-id="7a529-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a529-110">PARAMETERS</span></span>

### <span data-ttu-id="7a529-111">-Job</span><span class="sxs-lookup"><span data-stu-id="7a529-111">-Job</span></span>
<span data-ttu-id="7a529-112">Specifica l'oggetto processo di ripristino del sito da interrompere.</span><span class="sxs-lookup"><span data-stu-id="7a529-112">Specifies the Site Recovery job object to stop.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a529-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a529-113">-Name</span></span>
<span data-ttu-id="7a529-114">Specifica il nome univoco per cui il processo di ripristino del sito si arresta.</span><span class="sxs-lookup"><span data-stu-id="7a529-114">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="7a529-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a529-115">-DefaultProfile</span></span>
<span data-ttu-id="7a529-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a529-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a529-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a529-117">CommonParameters</span></span>
<span data-ttu-id="7a529-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a529-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a529-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a529-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a529-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a529-120">INPUTS</span></span>

### <span data-ttu-id="7a529-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="7a529-121">ASRJob</span></span>
<span data-ttu-id="7a529-122">Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7a529-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="7a529-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a529-123">OUTPUTS</span></span>

### <span data-ttu-id="7a529-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7a529-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7a529-125">Note</span><span class="sxs-lookup"><span data-stu-id="7a529-125">NOTES</span></span>

## <span data-ttu-id="7a529-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a529-126">RELATED LINKS</span></span>

[<span data-ttu-id="7a529-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7a529-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="7a529-128">Riavviare-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7a529-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="7a529-129">Curriculum vitae-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7a529-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
