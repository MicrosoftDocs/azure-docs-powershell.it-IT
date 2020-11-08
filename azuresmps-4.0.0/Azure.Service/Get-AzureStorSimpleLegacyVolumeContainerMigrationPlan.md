---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023514"
---
# <span data-ttu-id="9c5b8-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="9c5b8-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="9c5b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5b8-103">Ottiene i piani di migrazione per i contenitori legacy.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="9c5b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c5b8-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c5b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c5b8-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5b8-106">Il cmdlet **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** ottiene i piani di migrazione per i contenitori legacy.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="9c5b8-107">Specificare un piano di migrazione per l'ID configurazione legacy.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="9c5b8-108">Se la creazione del piano di migrazione è ancora in corso, questo cmdlet ottiene lo stato del piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="9c5b8-109">Se il piano di migrazione è stato completato, questo cmdlet restituisce il piano di migrazione effettivo per il set di contenitori legacy.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="9c5b8-110">Se non specifichi il parametro *LegacyConfigId* , questo cmdlet restituisce un elenco di ID di configurazione.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="9c5b8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c5b8-111">EXAMPLES</span></span>

### <span data-ttu-id="9c5b8-112">Esempio 1: ottenere lo stato di un piano</span><span class="sxs-lookup"><span data-stu-id="9c5b8-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="9c5b8-113">Questo comando ottiene lo stato del piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="9c5b8-114">Lo stato include la larghezza di banda assunta, il tempo stimato e le informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="9c5b8-115">Esempio 2: ottenere gli ID dei piani esistenti</span><span class="sxs-lookup"><span data-stu-id="9c5b8-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="9c5b8-116">Questo comando consente di ottenere tutti gli ID di configurazione dei piani di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="9c5b8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c5b8-117">PARAMETERS</span></span>

### <span data-ttu-id="9c5b8-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="9c5b8-118">-LegacyConfigId</span></span>
<span data-ttu-id="9c5b8-119">Specifica l'ID univoco della configurazione dell'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="9c5b8-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="9c5b8-120">-LegacyContainerNames</span></span>
<span data-ttu-id="9c5b8-121">Specifica una matrice di nomi di contenitori di volumi per cui questo cmdlet ottiene un piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="9c5b8-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="9c5b8-122">-Profile</span></span>
<span data-ttu-id="9c5b8-123">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9c5b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5b8-124">CommonParameters</span></span>
<span data-ttu-id="9c5b8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5b8-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5b8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5b8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c5b8-127">INPUTS</span></span>

### <span data-ttu-id="9c5b8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9c5b8-128">None</span></span>

## <span data-ttu-id="9c5b8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c5b8-129">OUTPUTS</span></span>

### <span data-ttu-id="9c5b8-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="9c5b8-130">MigrationPlanMsg</span></span>
<span data-ttu-id="9c5b8-131">Questo cmdlet restituisce un oggetto **MigrationPlanMsg** che contiene lo stato del processo del piano di migrazione, la larghezza di banda assunta in megabit al secondo e il tempo stimato in minuti.</span><span class="sxs-lookup"><span data-stu-id="9c5b8-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="9c5b8-132">Note</span><span class="sxs-lookup"><span data-stu-id="9c5b8-132">NOTES</span></span>

## <span data-ttu-id="9c5b8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c5b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c5b8-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="9c5b8-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


