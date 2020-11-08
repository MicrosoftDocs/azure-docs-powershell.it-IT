---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023731"
---
# <span data-ttu-id="58680-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="58680-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="58680-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58680-102">SYNOPSIS</span></span>
<span data-ttu-id="58680-103">Avvia la creazione di un piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="58680-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="58680-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58680-104">SYNTAX</span></span>

### <span data-ttu-id="58680-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="58680-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="58680-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="58680-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="58680-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58680-107">DESCRIPTION</span></span>
<span data-ttu-id="58680-108">Il cmdlet **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** avvia la creazione di un piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="58680-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="58680-109">La creazione di un piano di migrazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="58680-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="58680-110">Per visualizzare lo stato del piano di migrazione, usare il cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .</span><span class="sxs-lookup"><span data-stu-id="58680-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="58680-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58680-111">EXAMPLES</span></span>

### <span data-ttu-id="58680-112">Esempio 1: avviare un piano di migrazione</span><span class="sxs-lookup"><span data-stu-id="58680-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="58680-113">Questo comando avvia la creazione di un piano di migrazione per il contenitore legacy denominato OneSDKAzureCloud.</span><span class="sxs-lookup"><span data-stu-id="58680-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="58680-114">Il comando restituisce un messaggio relativo allo stato del piano e per utilizzare il cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** per informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="58680-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="58680-115">Esempio 2: avviare il piano di migrazione per tutti i contenitori di volumi</span><span class="sxs-lookup"><span data-stu-id="58680-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="58680-116">Questo comando avvia la creazione di un piano di migrazione per tutti i contenitori del volume legacy nel file di configurazione importato.</span><span class="sxs-lookup"><span data-stu-id="58680-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="58680-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58680-117">PARAMETERS</span></span>

### <span data-ttu-id="58680-118">-Tutti</span><span class="sxs-lookup"><span data-stu-id="58680-118">-All</span></span>
<span data-ttu-id="58680-119">Indica che questo cmdlet avvia le stime del tempo di migrazione per tutti i contenitori del volume nel file di configurazione importato.</span><span class="sxs-lookup"><span data-stu-id="58680-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58680-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="58680-120">-LegacyConfigId</span></span>
<span data-ttu-id="58680-121">Specifica l'ID univoco della configurazione dell'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="58680-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="58680-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="58680-122">-LegacyContainerNames</span></span>
<span data-ttu-id="58680-123">Specifica una matrice di nomi di contenitori di volumi per cui creare un piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="58680-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58680-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="58680-124">-Profile</span></span>
<span data-ttu-id="58680-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58680-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58680-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="58680-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58680-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58680-127">CommonParameters</span></span>
<span data-ttu-id="58680-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58680-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58680-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58680-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58680-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58680-130">INPUTS</span></span>

### <span data-ttu-id="58680-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58680-131">None</span></span>

## <span data-ttu-id="58680-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58680-132">OUTPUTS</span></span>

### <span data-ttu-id="58680-133">Stringa</span><span class="sxs-lookup"><span data-stu-id="58680-133">String</span></span>
<span data-ttu-id="58680-134">Questo cmdlet restituisce lo stato del processo del piano di migrazione se è stato avviato correttamente nell'appliance.</span><span class="sxs-lookup"><span data-stu-id="58680-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="58680-135">Note</span><span class="sxs-lookup"><span data-stu-id="58680-135">NOTES</span></span>

## <span data-ttu-id="58680-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58680-136">RELATED LINKS</span></span>

[<span data-ttu-id="58680-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="58680-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


