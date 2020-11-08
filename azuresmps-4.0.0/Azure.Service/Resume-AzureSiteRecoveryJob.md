---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029902"
---
# <span data-ttu-id="d127d-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d127d-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="d127d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d127d-102">SYNOPSIS</span></span>
<span data-ttu-id="d127d-103">Riprende un processo di ripristino del sito sospeso.</span><span class="sxs-lookup"><span data-stu-id="d127d-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="d127d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d127d-104">SYNTAX</span></span>

### <span data-ttu-id="d127d-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d127d-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d127d-106">ById</span><span class="sxs-lookup"><span data-stu-id="d127d-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d127d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d127d-107">DESCRIPTION</span></span>
<span data-ttu-id="d127d-108">Il cmdlet **Resume-AzureSiteRecoveryJob** riprende un processo di ripristino del sito di Azure sospesa.</span><span class="sxs-lookup"><span data-stu-id="d127d-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="d127d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d127d-109">EXAMPLES</span></span>

### <span data-ttu-id="d127d-110">Esempio 1: riprendere tutti i processi</span><span class="sxs-lookup"><span data-stu-id="d127d-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="d127d-111">Il primo comando recupera tutti i processi di ripristino dei siti di Azure per il Vault di ripristino del sito corrente usando il cmdlet **Get-AzureSiteRecoveryJob** e quindi archivia i risultati nella variabile $Jobs.</span><span class="sxs-lookup"><span data-stu-id="d127d-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="d127d-112">Il secondo comando riprende il processo specificato da $Jobs.</span><span class="sxs-lookup"><span data-stu-id="d127d-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="d127d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d127d-113">PARAMETERS</span></span>

### <span data-ttu-id="d127d-114">-Commenti</span><span class="sxs-lookup"><span data-stu-id="d127d-114">-Comments</span></span>
<span data-ttu-id="d127d-115">Specifica i commenti per il log dei processi.</span><span class="sxs-lookup"><span data-stu-id="d127d-115">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="d127d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="d127d-116">-Id</span></span>
<span data-ttu-id="d127d-117">Specifica l'ID di un processo da riprendere.</span><span class="sxs-lookup"><span data-stu-id="d127d-117">Specifies the ID of a job to resume.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d127d-118">-Job</span><span class="sxs-lookup"><span data-stu-id="d127d-118">-Job</span></span>
<span data-ttu-id="d127d-119">Specifica il processo da riprendere.</span><span class="sxs-lookup"><span data-stu-id="d127d-119">Specifies the job to resume.</span></span>

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

### <span data-ttu-id="d127d-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="d127d-120">-Profile</span></span>
<span data-ttu-id="d127d-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d127d-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d127d-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d127d-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d127d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d127d-123">CommonParameters</span></span>
<span data-ttu-id="d127d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d127d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d127d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d127d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d127d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d127d-126">INPUTS</span></span>

## <span data-ttu-id="d127d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d127d-127">OUTPUTS</span></span>

## <span data-ttu-id="d127d-128">Note</span><span class="sxs-lookup"><span data-stu-id="d127d-128">NOTES</span></span>

## <span data-ttu-id="d127d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d127d-129">RELATED LINKS</span></span>

[<span data-ttu-id="d127d-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d127d-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d127d-131">Riavviare-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d127d-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d127d-132">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d127d-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


