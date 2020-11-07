---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863609"
---
# <span data-ttu-id="e6cb8-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e6cb8-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e6cb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cb8-103">Crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e6cb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6cb8-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6cb8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cb8-106">Il cmdlet **New-AzVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e6cb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cb8-108">Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico</span><span class="sxs-lookup"><span data-stu-id="e6cb8-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="e6cb8-109">Questo comando crea l'oggetto Configuration per la creazione di patch.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="e6cb8-110">Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="e6cb8-111">Questa configurazione consente di applicare le patch che usano questi valori.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="e6cb8-112">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e6cb8-113">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="e6cb8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6cb8-114">PARAMETERS</span></span>

### <span data-ttu-id="e6cb8-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e6cb8-115">-DayOfWeek</span></span>
<span data-ttu-id="e6cb8-116">Specifica il giorno della settimana in cui devono essere installati gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="e6cb8-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6cb8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6cb8-118">Domenica</span><span class="sxs-lookup"><span data-stu-id="e6cb8-118">Sunday</span></span>
- <span data-ttu-id="e6cb8-119">Lunedì</span><span class="sxs-lookup"><span data-stu-id="e6cb8-119">Monday</span></span>
- <span data-ttu-id="e6cb8-120">Martedì</span><span class="sxs-lookup"><span data-stu-id="e6cb8-120">Tuesday</span></span>
- <span data-ttu-id="e6cb8-121">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="e6cb8-121">Wednesday</span></span>
- <span data-ttu-id="e6cb8-122">Giovedì</span><span class="sxs-lookup"><span data-stu-id="e6cb8-122">Thursday</span></span>
- <span data-ttu-id="e6cb8-123">Venerdì</span><span class="sxs-lookup"><span data-stu-id="e6cb8-123">Friday</span></span>
- <span data-ttu-id="e6cb8-124">Sabato</span><span class="sxs-lookup"><span data-stu-id="e6cb8-124">Saturday</span></span>
- <span data-ttu-id="e6cb8-125">Quotidiani</span><span class="sxs-lookup"><span data-stu-id="e6cb8-125">Everyday</span></span>

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

### <span data-ttu-id="e6cb8-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="e6cb8-126">-Enable</span></span>
<span data-ttu-id="e6cb8-127">Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e6cb8-128">Se si Abilita la patching automatizzato, il cmdlet inserisce Windows Update in modalità interattiva.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="e6cb8-129">Se si disattiva l'aggiornamento automatico, le impostazioni di Windows Update non cambiano.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="e6cb8-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e6cb8-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e6cb8-131">Specifica la durata, in minuti, della finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="e6cb8-132">La correzione automatica consente di evitare l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="e6cb8-133">Specificare un multiplo di 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="e6cb8-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e6cb8-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e6cb8-135">Specifica l'ora del giorno in cui viene avviata la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e6cb8-136">Questa volta definisce gli aggiornamenti che iniziano a essere installati.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="e6cb8-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e6cb8-137">-PatchCategory</span></span>
<span data-ttu-id="e6cb8-138">Specifica se gli aggiornamenti importanti devono essere inclusi.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="e6cb8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cb8-139">CommonParameters</span></span>
<span data-ttu-id="e6cb8-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cb8-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cb8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cb8-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6cb8-142">INPUTS</span></span>

### <span data-ttu-id="e6cb8-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6cb8-143">None</span></span>
<span data-ttu-id="e6cb8-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6cb8-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6cb8-145">OUTPUTS</span></span>

### <span data-ttu-id="e6cb8-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e6cb8-146">AutoPatchingSettings</span></span>
<span data-ttu-id="e6cb8-147">Questo cmdlet restituisce l'oggetto contenente le impostazioni per l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="e6cb8-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="e6cb8-148">Note</span><span class="sxs-lookup"><span data-stu-id="e6cb8-148">NOTES</span></span>

## <span data-ttu-id="e6cb8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6cb8-149">RELATED LINKS</span></span>

[<span data-ttu-id="e6cb8-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e6cb8-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e6cb8-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e6cb8-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


