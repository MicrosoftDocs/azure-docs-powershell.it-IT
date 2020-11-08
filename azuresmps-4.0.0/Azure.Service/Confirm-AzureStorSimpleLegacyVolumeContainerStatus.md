---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023658"
---
# <span data-ttu-id="ddf23-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="ddf23-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="ddf23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddf23-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf23-103">Avvia il commit o il rollback dei contenitori del volume di cui viene eseguita la migrazione.</span><span class="sxs-lookup"><span data-stu-id="ddf23-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="ddf23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddf23-104">SYNTAX</span></span>

### <span data-ttu-id="ddf23-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="ddf23-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ddf23-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="ddf23-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ddf23-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddf23-107">DESCRIPTION</span></span>
<span data-ttu-id="ddf23-108">Il cmdlet **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** avvia il commit o il rollback dei contenitori del volume di cui viene eseguita la migrazione come parte di una migrazione legacy.</span><span class="sxs-lookup"><span data-stu-id="ddf23-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="ddf23-109">Il rollback ripristina l'accessorio nella proprietà originale.</span><span class="sxs-lookup"><span data-stu-id="ddf23-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="ddf23-110">Il commit assegna la proprietà all'appliance di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ddf23-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="ddf23-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddf23-111">EXAMPLES</span></span>

### <span data-ttu-id="ddf23-112">Esempio 1: avviare un'operazione di commit in un contenitore di volumi specifico</span><span class="sxs-lookup"><span data-stu-id="ddf23-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="ddf23-113">Questo comando avvia un'operazione di commit nel contenitore di volumi specificato per l'ID di configurazione legacy specificato.</span><span class="sxs-lookup"><span data-stu-id="ddf23-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="ddf23-114">Per visualizzare lo stato dell'operazione, usare il cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** .</span><span class="sxs-lookup"><span data-stu-id="ddf23-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="ddf23-115">Esempio 2: avviare un'operazione di rollback in un contenitore di volumi specifico</span><span class="sxs-lookup"><span data-stu-id="ddf23-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="ddf23-116">Questo comando avvia un'operazione di rollback nel contenitore di volumi specificato per l'ID configurazione legacy specificato.</span><span class="sxs-lookup"><span data-stu-id="ddf23-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="ddf23-117">Esempio 3: avviare un'operazione di commit in tutti i contenitori di volumi</span><span class="sxs-lookup"><span data-stu-id="ddf23-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="ddf23-118">Questo comando avvia un'operazione di commit in tutti i contenitori di volumi per l'ID di configurazione legacy specificato.</span><span class="sxs-lookup"><span data-stu-id="ddf23-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="ddf23-119">Esempio 4: avviare un'operazione di rollback in tutti i contenitori di volumi</span><span class="sxs-lookup"><span data-stu-id="ddf23-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="ddf23-120">Questo comando avvia un'operazione di rollback in tutti i contenitori di volumi per l'ID configurazione legacy specificato.</span><span class="sxs-lookup"><span data-stu-id="ddf23-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="ddf23-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddf23-121">PARAMETERS</span></span>

### <span data-ttu-id="ddf23-122">-Tutti</span><span class="sxs-lookup"><span data-stu-id="ddf23-122">-All</span></span>
<span data-ttu-id="ddf23-123">Indica che questo cmdlet avvia un'operazione di rollback o di commit in tutti i contenitori del volume nel file di configurazione importato.</span><span class="sxs-lookup"><span data-stu-id="ddf23-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="ddf23-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="ddf23-124">-LegacyConfigId</span></span>
<span data-ttu-id="ddf23-125">Specifica l'ID univoco della configurazione dell'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="ddf23-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="ddf23-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="ddf23-126">-LegacyContainerNames</span></span>
<span data-ttu-id="ddf23-127">Specifica una matrice di nomi di contenitori di volumi per cui si applica il piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="ddf23-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="ddf23-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="ddf23-128">-MigrationOperation</span></span>
<span data-ttu-id="ddf23-129">Specifica se questo cmdlet esegue un commit o un rollback.</span><span class="sxs-lookup"><span data-stu-id="ddf23-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="ddf23-130">I valori validi sono: commit e rollback.</span><span class="sxs-lookup"><span data-stu-id="ddf23-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="ddf23-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="ddf23-131">-Profile</span></span>
<span data-ttu-id="ddf23-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddf23-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ddf23-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ddf23-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ddf23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf23-134">CommonParameters</span></span>
<span data-ttu-id="ddf23-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf23-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf23-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf23-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddf23-137">INPUTS</span></span>

## <span data-ttu-id="ddf23-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddf23-138">OUTPUTS</span></span>

## <span data-ttu-id="ddf23-139">Note</span><span class="sxs-lookup"><span data-stu-id="ddf23-139">NOTES</span></span>

## <span data-ttu-id="ddf23-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddf23-140">RELATED LINKS</span></span>

[<span data-ttu-id="ddf23-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="ddf23-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="ddf23-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="ddf23-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="ddf23-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="ddf23-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


