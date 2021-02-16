---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398258"
---
# <span data-ttu-id="79642-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="79642-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="79642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79642-102">SYNOPSIS</span></span>
<span data-ttu-id="79642-103">Crea un oggetto configurazione per la distribuzione automatica di patch in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="79642-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="79642-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79642-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="79642-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79642-105">DESCRIPTION</span></span>
<span data-ttu-id="79642-106">Il cmdlet **New-AzVMSqlServerAutoPatchingConfig** crea un oggetto di configurazione per l'applicazione automatica delle patch in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="79642-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="79642-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79642-107">EXAMPLES</span></span>

### <span data-ttu-id="79642-108">Esempio 1: Creare un oggetto di configurazione per configurare la distribuzione automatica di patch</span><span class="sxs-lookup"><span data-stu-id="79642-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="79642-109">Questo comando crea un oggetto configurazione per la distribuzione delle patch.</span><span class="sxs-lookup"><span data-stu-id="79642-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="79642-110">Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="79642-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="79642-111">Questa configurazione abilita la distribuzione di patch che usa questi valori.</span><span class="sxs-lookup"><span data-stu-id="79642-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="79642-112">Il comando archivia il risultato nella $AutoBackupConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="79642-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="79642-113">È possibile specificare questo elemento di configurazione per altri cmdlet, ad esempio Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79642-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="79642-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79642-114">PARAMETERS</span></span>

### <span data-ttu-id="79642-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="79642-115">-DayOfWeek</span></span>
<span data-ttu-id="79642-116">Specifica il giorno della settimana in cui installare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="79642-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="79642-117">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="79642-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79642-118">Domenica</span><span class="sxs-lookup"><span data-stu-id="79642-118">Sunday</span></span>
- <span data-ttu-id="79642-119">Lunedì</span><span class="sxs-lookup"><span data-stu-id="79642-119">Monday</span></span>
- <span data-ttu-id="79642-120">Martedì</span><span class="sxs-lookup"><span data-stu-id="79642-120">Tuesday</span></span>
- <span data-ttu-id="79642-121">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="79642-121">Wednesday</span></span>
- <span data-ttu-id="79642-122">Giovedì</span><span class="sxs-lookup"><span data-stu-id="79642-122">Thursday</span></span>
- <span data-ttu-id="79642-123">Venerdì</span><span class="sxs-lookup"><span data-stu-id="79642-123">Friday</span></span>
- <span data-ttu-id="79642-124">Sabato</span><span class="sxs-lookup"><span data-stu-id="79642-124">Saturday</span></span>
- <span data-ttu-id="79642-125">Ogni giorno</span><span class="sxs-lookup"><span data-stu-id="79642-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79642-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="79642-126">-Enable</span></span>
<span data-ttu-id="79642-127">Indica che è abilitata la distribuzione automatica di patch per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="79642-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="79642-128">Se si abilita la distribuzione automatica di patch, il cmdlet attiva la modalità interattiva di Windows Update.</span><span class="sxs-lookup"><span data-stu-id="79642-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="79642-129">Se si disabilita la distribuzione automatica di patch, le impostazioni di Windows Update non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="79642-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="79642-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="79642-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="79642-131">Specifica la durata in minuti della finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="79642-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="79642-132">La distribuzione automatizzata delle patch evita di eseguire un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno di tale finestra.</span><span class="sxs-lookup"><span data-stu-id="79642-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="79642-133">Specificare un multiplo di 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="79642-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79642-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="79642-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="79642-135">Specifica l'ora del giorno in cui inizia la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="79642-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="79642-136">Questa volta definisce l'inizio dell'installazione degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="79642-136">This time defines when updates start to install.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79642-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="79642-137">-PatchCategory</span></span>
<span data-ttu-id="79642-138">Specifica se includere gli aggiornamenti importanti.</span><span class="sxs-lookup"><span data-stu-id="79642-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79642-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79642-139">CommonParameters</span></span>
<span data-ttu-id="79642-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79642-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79642-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79642-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79642-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="79642-142">INPUTS</span></span>

### <span data-ttu-id="79642-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79642-143">None</span></span>
<span data-ttu-id="79642-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="79642-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79642-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79642-145">OUTPUTS</span></span>

### <span data-ttu-id="79642-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="79642-146">AutoPatchingSettings</span></span>
<span data-ttu-id="79642-147">Questo cmdlet restituisce l'oggetto che contiene le impostazioni per la distribuzione automatica di patch.</span><span class="sxs-lookup"><span data-stu-id="79642-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="79642-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="79642-148">NOTES</span></span>

## <span data-ttu-id="79642-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79642-149">RELATED LINKS</span></span>

[<span data-ttu-id="79642-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="79642-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="79642-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="79642-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


