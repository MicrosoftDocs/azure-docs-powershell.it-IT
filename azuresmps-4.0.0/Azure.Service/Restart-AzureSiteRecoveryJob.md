---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029538"
---
# <span data-ttu-id="d8708-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8708-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="d8708-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8708-102">SYNOPSIS</span></span>
<span data-ttu-id="d8708-103">Riavvia un processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="d8708-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="d8708-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8708-104">SYNTAX</span></span>

### <span data-ttu-id="d8708-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8708-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8708-106">ById</span><span class="sxs-lookup"><span data-stu-id="d8708-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8708-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8708-107">DESCRIPTION</span></span>
<span data-ttu-id="d8708-108">Il cmdlet **Restart-AzureSiteRecoveryJob riavvia** un processo di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8708-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d8708-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8708-109">EXAMPLES</span></span>

### <span data-ttu-id="d8708-110">Esempio 1: riavviare un processo</span><span class="sxs-lookup"><span data-stu-id="d8708-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="d8708-111">Questo comando Riavvia il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="d8708-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="d8708-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8708-112">PARAMETERS</span></span>

### <span data-ttu-id="d8708-113">-ID</span><span class="sxs-lookup"><span data-stu-id="d8708-113">-Id</span></span>
<span data-ttu-id="d8708-114">Specifica l'ID del processo da riavviare.</span><span class="sxs-lookup"><span data-stu-id="d8708-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="d8708-115">-Job</span><span class="sxs-lookup"><span data-stu-id="d8708-115">-Job</span></span>
<span data-ttu-id="d8708-116">Specifica il processo da riavviare.</span><span class="sxs-lookup"><span data-stu-id="d8708-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="d8708-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="d8708-117">-Profile</span></span>
<span data-ttu-id="d8708-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8708-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8708-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d8708-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8708-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8708-120">CommonParameters</span></span>
<span data-ttu-id="d8708-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8708-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8708-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8708-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8708-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8708-123">INPUTS</span></span>

## <span data-ttu-id="d8708-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8708-124">OUTPUTS</span></span>

## <span data-ttu-id="d8708-125">Note</span><span class="sxs-lookup"><span data-stu-id="d8708-125">NOTES</span></span>

## <span data-ttu-id="d8708-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8708-126">RELATED LINKS</span></span>

[<span data-ttu-id="d8708-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8708-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d8708-128">Curriculum vitae-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8708-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="d8708-129">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d8708-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


