---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 1b17284a5b0dfbdc8ee031df714c9f9f03533697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519503"
---
# <span data-ttu-id="94104-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="94104-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="94104-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94104-102">SYNOPSIS</span></span>
<span data-ttu-id="94104-103">Riavvia un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="94104-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94104-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94104-104">SYNTAX</span></span>

### <span data-ttu-id="94104-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94104-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94104-106">ByName</span><span class="sxs-lookup"><span data-stu-id="94104-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94104-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94104-107">DESCRIPTION</span></span>
<span data-ttu-id="94104-108">Il cmdlet **Restart-AzureRmSiteRecoveryJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="94104-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="94104-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94104-109">EXAMPLES</span></span>

## <span data-ttu-id="94104-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94104-110">PARAMETERS</span></span>

### <span data-ttu-id="94104-111">-Job</span><span class="sxs-lookup"><span data-stu-id="94104-111">-Job</span></span>
<span data-ttu-id="94104-112">Specifica l'oggetto processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="94104-112">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="94104-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="94104-113">-Name</span></span>
<span data-ttu-id="94104-114">Specifica il nome univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="94104-114">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="94104-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94104-115">-DefaultProfile</span></span>
<span data-ttu-id="94104-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94104-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94104-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94104-117">CommonParameters</span></span>
<span data-ttu-id="94104-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94104-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94104-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94104-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94104-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94104-120">INPUTS</span></span>

### <span data-ttu-id="94104-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="94104-121">ASRJob</span></span>
<span data-ttu-id="94104-122">Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="94104-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="94104-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94104-123">OUTPUTS</span></span>

### <span data-ttu-id="94104-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="94104-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="94104-125">Note</span><span class="sxs-lookup"><span data-stu-id="94104-125">NOTES</span></span>

## <span data-ttu-id="94104-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94104-126">RELATED LINKS</span></span>

[<span data-ttu-id="94104-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="94104-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="94104-128">Curriculum vitae-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="94104-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="94104-129">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="94104-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
