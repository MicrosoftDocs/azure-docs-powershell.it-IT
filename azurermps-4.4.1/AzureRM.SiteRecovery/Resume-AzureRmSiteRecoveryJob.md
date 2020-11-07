---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686772"
---
# <span data-ttu-id="9819a-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9819a-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="9819a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9819a-102">SYNOPSIS</span></span>
<span data-ttu-id="9819a-103">Riprende un processo di ripristino del sito sospeso.</span><span class="sxs-lookup"><span data-stu-id="9819a-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9819a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9819a-104">SYNTAX</span></span>

### <span data-ttu-id="9819a-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9819a-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9819a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9819a-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9819a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9819a-107">DESCRIPTION</span></span>
<span data-ttu-id="9819a-108">Il cmdlet **Resume-AzureRmSiteRecoveryJob** riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="9819a-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="9819a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9819a-109">EXAMPLES</span></span>

## <span data-ttu-id="9819a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9819a-110">PARAMETERS</span></span>

### <span data-ttu-id="9819a-111">-Commenti</span><span class="sxs-lookup"><span data-stu-id="9819a-111">-Comments</span></span>
<span data-ttu-id="9819a-112">Specifica i commenti per il log dei processi.</span><span class="sxs-lookup"><span data-stu-id="9819a-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9819a-113">-Job</span><span class="sxs-lookup"><span data-stu-id="9819a-113">-Job</span></span>
<span data-ttu-id="9819a-114">Specifica l'oggetto processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="9819a-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="9819a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9819a-115">-Name</span></span>
<span data-ttu-id="9819a-116">Specifica il nome univoco per il processo.</span><span class="sxs-lookup"><span data-stu-id="9819a-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="9819a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9819a-117">-DefaultProfile</span></span>
<span data-ttu-id="9819a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9819a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9819a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9819a-119">CommonParameters</span></span>
<span data-ttu-id="9819a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9819a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9819a-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9819a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9819a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9819a-122">INPUTS</span></span>

### <span data-ttu-id="9819a-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="9819a-123">ASRJob</span></span>
<span data-ttu-id="9819a-124">Il parametro "Job" accetta il valore di tipo "ASRJob" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9819a-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="9819a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9819a-125">OUTPUTS</span></span>

### <span data-ttu-id="9819a-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9819a-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9819a-127">Note</span><span class="sxs-lookup"><span data-stu-id="9819a-127">NOTES</span></span>

## <span data-ttu-id="9819a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9819a-128">RELATED LINKS</span></span>

[<span data-ttu-id="9819a-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9819a-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9819a-130">Riavviare-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9819a-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="9819a-131">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="9819a-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
