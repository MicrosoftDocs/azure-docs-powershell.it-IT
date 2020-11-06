---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521743"
---
# <span data-ttu-id="20f14-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="20f14-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="20f14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20f14-102">SYNOPSIS</span></span>
<span data-ttu-id="20f14-103">Crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="20f14-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20f14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20f14-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="20f14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20f14-105">DESCRIPTION</span></span>
<span data-ttu-id="20f14-106">Il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="20f14-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="20f14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20f14-107">EXAMPLES</span></span>

### <span data-ttu-id="20f14-108">Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico</span><span class="sxs-lookup"><span data-stu-id="20f14-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="20f14-109">Questo comando crea l'oggetto Configuration per la creazione di patch.</span><span class="sxs-lookup"><span data-stu-id="20f14-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="20f14-110">Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="20f14-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="20f14-111">Questa configurazione consente di applicare le patch che usano questi valori.</span><span class="sxs-lookup"><span data-stu-id="20f14-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="20f14-112">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="20f14-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="20f14-113">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="20f14-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="20f14-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20f14-114">PARAMETERS</span></span>

### <span data-ttu-id="20f14-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="20f14-115">-Enable</span></span>
<span data-ttu-id="20f14-116">Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="20f14-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="20f14-117">Se si Abilita la patching automatizzato, il cmdlet inserisce Windows Update in modalità interattiva.</span><span class="sxs-lookup"><span data-stu-id="20f14-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="20f14-118">Se si disattiva l'aggiornamento automatico, le impostazioni di Windows Update non cambiano.</span><span class="sxs-lookup"><span data-stu-id="20f14-118">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f14-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="20f14-119">-DayOfWeek</span></span>
<span data-ttu-id="20f14-120">Specifica il giorno della settimana in cui devono essere installati gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="20f14-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="20f14-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="20f14-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20f14-122">Domenica</span><span class="sxs-lookup"><span data-stu-id="20f14-122">Sunday</span></span>
- <span data-ttu-id="20f14-123">Lunedì</span><span class="sxs-lookup"><span data-stu-id="20f14-123">Monday</span></span>
- <span data-ttu-id="20f14-124">Martedì</span><span class="sxs-lookup"><span data-stu-id="20f14-124">Tuesday</span></span>
- <span data-ttu-id="20f14-125">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="20f14-125">Wednesday</span></span>
- <span data-ttu-id="20f14-126">Giovedì</span><span class="sxs-lookup"><span data-stu-id="20f14-126">Thursday</span></span>
- <span data-ttu-id="20f14-127">Venerdì</span><span class="sxs-lookup"><span data-stu-id="20f14-127">Friday</span></span>
- <span data-ttu-id="20f14-128">Sabato</span><span class="sxs-lookup"><span data-stu-id="20f14-128">Saturday</span></span>
- <span data-ttu-id="20f14-129">Quotidiani</span><span class="sxs-lookup"><span data-stu-id="20f14-129">Everyday</span></span>

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

### <span data-ttu-id="20f14-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="20f14-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="20f14-131">Specifica l'ora del giorno in cui viene avviata la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="20f14-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="20f14-132">Questa volta definisce gli aggiornamenti che iniziano a essere installati.</span><span class="sxs-lookup"><span data-stu-id="20f14-132">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f14-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="20f14-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="20f14-134">Specifica la durata, in minuti, della finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="20f14-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="20f14-135">La correzione automatica consente di evitare l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="20f14-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="20f14-136">Specificare un multiplo di 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="20f14-136">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f14-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="20f14-137">-PatchCategory</span></span>
<span data-ttu-id="20f14-138">Specifica se gli aggiornamenti importanti devono essere inclusi.</span><span class="sxs-lookup"><span data-stu-id="20f14-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="20f14-139">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20f14-139">-InformationAction</span></span>
<span data-ttu-id="20f14-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="20f14-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f14-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20f14-141">-InformationVariable</span></span>
<span data-ttu-id="20f14-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="20f14-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f14-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f14-143">CommonParameters</span></span>
<span data-ttu-id="20f14-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f14-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f14-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f14-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f14-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20f14-146">INPUTS</span></span>

## <span data-ttu-id="20f14-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20f14-147">OUTPUTS</span></span>

### <span data-ttu-id="20f14-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="20f14-148">AutoPatchingSettings</span></span>
<span data-ttu-id="20f14-149">Questo cmdlet restituisce l'oggetto contenente le impostazioni per l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="20f14-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="20f14-150">Note</span><span class="sxs-lookup"><span data-stu-id="20f14-150">NOTES</span></span>

## <span data-ttu-id="20f14-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20f14-151">RELATED LINKS</span></span>

[<span data-ttu-id="20f14-152">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="20f14-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="20f14-153">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="20f14-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


