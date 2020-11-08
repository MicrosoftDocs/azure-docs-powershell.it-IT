---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030012"
---
# <span data-ttu-id="76879-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="76879-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="76879-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76879-102">SYNOPSIS</span></span>
<span data-ttu-id="76879-103">Ottiene lo stato di migrazione dei contenitori del volume.</span><span class="sxs-lookup"><span data-stu-id="76879-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="76879-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76879-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="76879-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76879-105">DESCRIPTION</span></span>
<span data-ttu-id="76879-106">Il cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** ottiene lo stato di migrazione dei contenitori del volume.</span><span class="sxs-lookup"><span data-stu-id="76879-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="76879-107">Questo cmdlet restituisce le informazioni sullo stato che includono se la migrazione del contenitore di volumi è ancora in corso, completata o fallita.</span><span class="sxs-lookup"><span data-stu-id="76879-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="76879-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76879-108">EXAMPLES</span></span>

### <span data-ttu-id="76879-109">Esempio 1: ottenere lo stato per una migrazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="76879-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="76879-110">Questo comando ottiene lo stato di migrazione per il contenitore legacy denominato.</span><span class="sxs-lookup"><span data-stu-id="76879-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="76879-111">I risultati mostrano che la migrazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="76879-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="76879-112">Esempio 2: ottenere lo stato per una migrazione in corso</span><span class="sxs-lookup"><span data-stu-id="76879-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="76879-113">Questo comando ottiene lo stato di migrazione per il contenitore legacy denominato.</span><span class="sxs-lookup"><span data-stu-id="76879-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="76879-114">I risultati mostrano che la migrazione è in corso.</span><span class="sxs-lookup"><span data-stu-id="76879-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="76879-115">Esempio 3: ottenere lo stato per una migrazione completata</span><span class="sxs-lookup"><span data-stu-id="76879-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="76879-116">Questo comando ottiene lo stato di migrazione per il contenitore legacy denominato.</span><span class="sxs-lookup"><span data-stu-id="76879-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="76879-117">I risultati mostrano che la migrazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="76879-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="76879-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76879-118">PARAMETERS</span></span>

### <span data-ttu-id="76879-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="76879-119">-LegacyConfigId</span></span>
<span data-ttu-id="76879-120">Specifica l'ID univoco della configurazione dell'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="76879-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76879-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="76879-121">-LegacyContainerNames</span></span>
<span data-ttu-id="76879-122">Specifica una matrice di nomi di contenitori di volumi per cui si applica il piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="76879-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76879-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="76879-123">-Profile</span></span>
<span data-ttu-id="76879-124">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="76879-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="76879-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76879-125">CommonParameters</span></span>
<span data-ttu-id="76879-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76879-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76879-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76879-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76879-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76879-128">INPUTS</span></span>

## <span data-ttu-id="76879-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76879-129">OUTPUTS</span></span>

## <span data-ttu-id="76879-130">Note</span><span class="sxs-lookup"><span data-stu-id="76879-130">NOTES</span></span>

## <span data-ttu-id="76879-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76879-131">RELATED LINKS</span></span>

[<span data-ttu-id="76879-132">Conferma-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="76879-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="76879-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="76879-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


