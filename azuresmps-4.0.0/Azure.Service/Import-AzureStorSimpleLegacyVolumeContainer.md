---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029720"
---
# <span data-ttu-id="741c7-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="741c7-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="741c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="741c7-102">SYNOPSIS</span></span>
<span data-ttu-id="741c7-103">Avvia la migrazione dei contenitori di volumi.</span><span class="sxs-lookup"><span data-stu-id="741c7-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="741c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="741c7-104">SYNTAX</span></span>

### <span data-ttu-id="741c7-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="741c7-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="741c7-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="741c7-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="741c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="741c7-107">DESCRIPTION</span></span>
<span data-ttu-id="741c7-108">Il cmdlet **Import-AzureStorSimpleLegacyVolumeContainer** avvia la migrazione dei contenitori di volumi da un dispositivo legacy all'accessorio di destinazione.</span><span class="sxs-lookup"><span data-stu-id="741c7-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="741c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="741c7-109">EXAMPLES</span></span>

### <span data-ttu-id="741c7-110">Esempio 1: importare un contenitore di volumi legacy</span><span class="sxs-lookup"><span data-stu-id="741c7-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="741c7-111">Questo comando importa un contenitore di volumi legacy per il contenitore denominato.</span><span class="sxs-lookup"><span data-stu-id="741c7-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="741c7-112">Il cmdlet avvia l'importazione e quindi restituisce un messaggio.</span><span class="sxs-lookup"><span data-stu-id="741c7-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="741c7-113">Esempio 2: importare tutti i contenitori del volume legacy</span><span class="sxs-lookup"><span data-stu-id="741c7-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="741c7-114">Questo comando importa tutti i contenitori del volume legacy dal file di configurazione importato.</span><span class="sxs-lookup"><span data-stu-id="741c7-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="741c7-115">Il cmdlet avvia l'importazione e quindi restituisce un messaggio.</span><span class="sxs-lookup"><span data-stu-id="741c7-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="741c7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="741c7-116">PARAMETERS</span></span>

### <span data-ttu-id="741c7-117">-Tutti</span><span class="sxs-lookup"><span data-stu-id="741c7-117">-All</span></span>
<span data-ttu-id="741c7-118">Indica che questo cmdlet importa tutti i contenitori del volume nel file di configurazione importato nel dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="741c7-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="741c7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="741c7-119">-Force</span></span>
<span data-ttu-id="741c7-120">Indica che questo cmdlet importa il contenitore di volumi in un dispositivo diverso, anche se il contenitore del volume è stato importato in un dispositivo diverso.</span><span class="sxs-lookup"><span data-stu-id="741c7-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741c7-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="741c7-121">-LegacyConfigId</span></span>
<span data-ttu-id="741c7-122">Specifica l'ID univoco della configurazione dell'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="741c7-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="741c7-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="741c7-123">-LegacyContainerNames</span></span>
<span data-ttu-id="741c7-124">Specifica una matrice di nomi di contenitori di volumi per cui si applica il piano di migrazione.</span><span class="sxs-lookup"><span data-stu-id="741c7-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="741c7-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="741c7-125">-Profile</span></span>
<span data-ttu-id="741c7-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="741c7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="741c7-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="741c7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="741c7-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="741c7-128">-SkipACRs</span></span>
<span data-ttu-id="741c7-129">Indica che il processo di importazione ignora i record di controllo di accesso per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="741c7-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741c7-130">CommonParameters</span></span>
<span data-ttu-id="741c7-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741c7-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="741c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741c7-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="741c7-133">INPUTS</span></span>

## <span data-ttu-id="741c7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="741c7-134">OUTPUTS</span></span>

### <span data-ttu-id="741c7-135">Stringa</span><span class="sxs-lookup"><span data-stu-id="741c7-135">String</span></span>
<span data-ttu-id="741c7-136">Questo comando restituisce lo stato del processo di migrazione del contenitore del volume di importazione se è stato avviato correttamente nell'appliance.</span><span class="sxs-lookup"><span data-stu-id="741c7-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="741c7-137">Note</span><span class="sxs-lookup"><span data-stu-id="741c7-137">NOTES</span></span>

## <span data-ttu-id="741c7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="741c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="741c7-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="741c7-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="741c7-140">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="741c7-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


