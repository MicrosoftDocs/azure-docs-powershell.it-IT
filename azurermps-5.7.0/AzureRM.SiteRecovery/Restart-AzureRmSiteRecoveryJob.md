---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507939"
---
# <span data-ttu-id="1ca32-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1ca32-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="1ca32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ca32-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca32-103">Riavvia un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca32-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ca32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ca32-104">SYNTAX</span></span>

### <span data-ttu-id="1ca32-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ca32-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ca32-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1ca32-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ca32-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ca32-107">DESCRIPTION</span></span>
<span data-ttu-id="1ca32-108">Il cmdlet **Restart-AzureRmSiteRecoveryJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca32-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="1ca32-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ca32-109">EXAMPLES</span></span>

## <span data-ttu-id="1ca32-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ca32-110">PARAMETERS</span></span>

### <span data-ttu-id="1ca32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca32-111">-DefaultProfile</span></span>
<span data-ttu-id="1ca32-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca32-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ca32-113">-Job</span><span class="sxs-lookup"><span data-stu-id="1ca32-113">-Job</span></span>
<span data-ttu-id="1ca32-114">Specifica l'oggetto processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="1ca32-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="1ca32-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ca32-115">-Name</span></span>
<span data-ttu-id="1ca32-116">Specifica il nome univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="1ca32-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="1ca32-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca32-117">CommonParameters</span></span>
<span data-ttu-id="1ca32-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca32-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca32-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca32-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca32-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ca32-120">INPUTS</span></span>

### <span data-ttu-id="1ca32-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ca32-121">ASRJob</span></span>
<span data-ttu-id="1ca32-122">Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1ca32-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="1ca32-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ca32-123">OUTPUTS</span></span>

### <span data-ttu-id="1ca32-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1ca32-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1ca32-125">Note</span><span class="sxs-lookup"><span data-stu-id="1ca32-125">NOTES</span></span>

## <span data-ttu-id="1ca32-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ca32-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ca32-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1ca32-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="1ca32-128">Curriculum vitae-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1ca32-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="1ca32-129">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1ca32-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
