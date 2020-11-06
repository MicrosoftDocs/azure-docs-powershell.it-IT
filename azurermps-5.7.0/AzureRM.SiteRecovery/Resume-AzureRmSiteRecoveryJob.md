---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/resume-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: aae0bf7c2ec4a166d48edb032d6c21918dc3ae6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514103"
---
# <span data-ttu-id="7eaf5-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7eaf5-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="7eaf5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="7eaf5-103">Riprende un processo di ripristino del sito sospeso.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eaf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eaf5-104">SYNTAX</span></span>

### <span data-ttu-id="7eaf5-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7eaf5-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7eaf5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7eaf5-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eaf5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eaf5-107">DESCRIPTION</span></span>
<span data-ttu-id="7eaf5-108">Il cmdlet **Resume-AzureRmSiteRecoveryJob** riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="7eaf5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eaf5-109">EXAMPLES</span></span>

## <span data-ttu-id="7eaf5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eaf5-110">PARAMETERS</span></span>

### <span data-ttu-id="7eaf5-111">-Commenti</span><span class="sxs-lookup"><span data-stu-id="7eaf5-111">-Comments</span></span>
<span data-ttu-id="7eaf5-112">Specifica i commenti per il log dei processi.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-112">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="7eaf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eaf5-113">-DefaultProfile</span></span>
<span data-ttu-id="7eaf5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eaf5-115">-Job</span><span class="sxs-lookup"><span data-stu-id="7eaf5-115">-Job</span></span>
<span data-ttu-id="7eaf5-116">Specifica l'oggetto processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-116">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eaf5-117">-Name</span></span>
<span data-ttu-id="7eaf5-118">Specifica il nome univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-118">Specifies the unique name for the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eaf5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eaf5-119">CommonParameters</span></span>
<span data-ttu-id="7eaf5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eaf5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eaf5-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eaf5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eaf5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eaf5-122">INPUTS</span></span>

### <span data-ttu-id="7eaf5-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="7eaf5-123">ASRJob</span></span>
<span data-ttu-id="7eaf5-124">Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7eaf5-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="7eaf5-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eaf5-125">OUTPUTS</span></span>

### <span data-ttu-id="7eaf5-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7eaf5-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7eaf5-127">Note</span><span class="sxs-lookup"><span data-stu-id="7eaf5-127">NOTES</span></span>

## <span data-ttu-id="7eaf5-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eaf5-128">RELATED LINKS</span></span>

[<span data-ttu-id="7eaf5-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7eaf5-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="7eaf5-130">Riavviare-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7eaf5-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="7eaf5-131">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7eaf5-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
