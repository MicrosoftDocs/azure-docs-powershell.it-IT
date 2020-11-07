---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 302197adbbf6e90397a5bb6f3e96be6d6836b1bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675310"
---
# <span data-ttu-id="8cea4-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8cea4-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="8cea4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cea4-102">SYNOPSIS</span></span>
<span data-ttu-id="8cea4-103">Crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cea4-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="8cea4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cea4-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="8cea4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cea4-105">DESCRIPTION</span></span>
<span data-ttu-id="8cea4-106">Il cmdlet **New-AzVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cea4-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="8cea4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cea4-107">EXAMPLES</span></span>

### <span data-ttu-id="8cea4-108">Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico</span><span class="sxs-lookup"><span data-stu-id="8cea4-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="8cea4-109">Questo comando crea l'oggetto Configuration per la creazione di patch.</span><span class="sxs-lookup"><span data-stu-id="8cea4-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="8cea4-110">Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="8cea4-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="8cea4-111">Questa configurazione consente di applicare le patch che usano questi valori.</span><span class="sxs-lookup"><span data-stu-id="8cea4-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="8cea4-112">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="8cea4-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="8cea4-113">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="8cea4-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="8cea4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cea4-114">PARAMETERS</span></span>

### <span data-ttu-id="8cea4-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="8cea4-115">-DayOfWeek</span></span>
<span data-ttu-id="8cea4-116">Specifica il giorno della settimana in cui devono essere installati gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="8cea4-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="8cea4-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cea4-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cea4-118">Domenica</span><span class="sxs-lookup"><span data-stu-id="8cea4-118">Sunday</span></span>
- <span data-ttu-id="8cea4-119">Lunedì</span><span class="sxs-lookup"><span data-stu-id="8cea4-119">Monday</span></span>
- <span data-ttu-id="8cea4-120">Martedì</span><span class="sxs-lookup"><span data-stu-id="8cea4-120">Tuesday</span></span>
- <span data-ttu-id="8cea4-121">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="8cea4-121">Wednesday</span></span>
- <span data-ttu-id="8cea4-122">Giovedì</span><span class="sxs-lookup"><span data-stu-id="8cea4-122">Thursday</span></span>
- <span data-ttu-id="8cea4-123">Venerdì</span><span class="sxs-lookup"><span data-stu-id="8cea4-123">Friday</span></span>
- <span data-ttu-id="8cea4-124">Sabato</span><span class="sxs-lookup"><span data-stu-id="8cea4-124">Saturday</span></span>
- <span data-ttu-id="8cea4-125">Quotidiani</span><span class="sxs-lookup"><span data-stu-id="8cea4-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cea4-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="8cea4-126">-Enable</span></span>
<span data-ttu-id="8cea4-127">Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cea4-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="8cea4-128">Se si Abilita la patching automatizzato, il cmdlet inserisce Windows Update in modalità interattiva.</span><span class="sxs-lookup"><span data-stu-id="8cea4-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="8cea4-129">Se si disattiva l'aggiornamento automatico, le impostazioni di Windows Update non cambiano.</span><span class="sxs-lookup"><span data-stu-id="8cea4-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="8cea4-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="8cea4-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="8cea4-131">Specifica la durata, in minuti, della finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="8cea4-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="8cea4-132">La correzione automatica consente di evitare l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="8cea4-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="8cea4-133">Specificare un multiplo di 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="8cea4-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="8cea4-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="8cea4-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="8cea4-135">Specifica l'ora del giorno in cui viene avviata la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="8cea4-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="8cea4-136">Questa volta definisce gli aggiornamenti che iniziano a essere installati.</span><span class="sxs-lookup"><span data-stu-id="8cea4-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="8cea4-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="8cea4-137">-PatchCategory</span></span>
<span data-ttu-id="8cea4-138">Specifica se gli aggiornamenti importanti devono essere inclusi.</span><span class="sxs-lookup"><span data-stu-id="8cea4-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cea4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cea4-139">CommonParameters</span></span>
<span data-ttu-id="8cea4-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cea4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cea4-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cea4-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cea4-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cea4-142">INPUTS</span></span>

### <span data-ttu-id="8cea4-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8cea4-143">None</span></span>

## <span data-ttu-id="8cea4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cea4-144">OUTPUTS</span></span>

### <span data-ttu-id="8cea4-145">Microsoft. Azure. Commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8cea4-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="8cea4-146">Note</span><span class="sxs-lookup"><span data-stu-id="8cea4-146">NOTES</span></span>

## <span data-ttu-id="8cea4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cea4-147">RELATED LINKS</span></span>

[<span data-ttu-id="8cea4-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="8cea4-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="8cea4-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8cea4-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

