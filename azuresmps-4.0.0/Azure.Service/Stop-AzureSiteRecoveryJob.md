---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029869"
---
# <span data-ttu-id="14b13-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="14b13-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="14b13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14b13-102">SYNOPSIS</span></span>
<span data-ttu-id="14b13-103">Interrompe un processo di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="14b13-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="14b13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14b13-104">SYNTAX</span></span>

### <span data-ttu-id="14b13-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14b13-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="14b13-106">ById</span><span class="sxs-lookup"><span data-stu-id="14b13-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="14b13-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14b13-107">DESCRIPTION</span></span>
<span data-ttu-id="14b13-108">Il cmdlet **Stop-AzureSiteRecoveryJob** arresta un processo di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="14b13-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="14b13-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14b13-109">EXAMPLES</span></span>

### <span data-ttu-id="14b13-110">Esempio 1: arrestare tutti i processi</span><span class="sxs-lookup"><span data-stu-id="14b13-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="14b13-111">Il primo comando ottiene i processi di ripristino dei siti di Azure per il Vault di ripristino del sito di Azure corrente usando il cmdlet **Get-AzureSiteRecoveryJob** e quindi archivia i risultati nella variabile $Jobs.</span><span class="sxs-lookup"><span data-stu-id="14b13-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="14b13-112">Il secondo comando arresta i processi specificati da $Jobs.</span><span class="sxs-lookup"><span data-stu-id="14b13-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="14b13-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14b13-113">PARAMETERS</span></span>

### <span data-ttu-id="14b13-114">-ID</span><span class="sxs-lookup"><span data-stu-id="14b13-114">-Id</span></span>
<span data-ttu-id="14b13-115">Specifica l'ID del processo da interrompere.</span><span class="sxs-lookup"><span data-stu-id="14b13-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="14b13-116">-Job</span><span class="sxs-lookup"><span data-stu-id="14b13-116">-Job</span></span>
<span data-ttu-id="14b13-117">Specifica il processo da interrompere.</span><span class="sxs-lookup"><span data-stu-id="14b13-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="14b13-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="14b13-118">-Profile</span></span>
<span data-ttu-id="14b13-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14b13-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14b13-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="14b13-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14b13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b13-121">CommonParameters</span></span>
<span data-ttu-id="14b13-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b13-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14b13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b13-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14b13-124">INPUTS</span></span>

## <span data-ttu-id="14b13-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14b13-125">OUTPUTS</span></span>

## <span data-ttu-id="14b13-126">Note</span><span class="sxs-lookup"><span data-stu-id="14b13-126">NOTES</span></span>

## <span data-ttu-id="14b13-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14b13-127">RELATED LINKS</span></span>

[<span data-ttu-id="14b13-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="14b13-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="14b13-129">Riavviare-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="14b13-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="14b13-130">Curriculum vitae-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="14b13-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


