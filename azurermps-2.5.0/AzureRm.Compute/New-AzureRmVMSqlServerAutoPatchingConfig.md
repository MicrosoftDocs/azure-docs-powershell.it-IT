---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
ms.openlocfilehash: 1204a8b14cdbb45f46edd2a1ca2e4c12c27845a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866750"
---
# <span data-ttu-id="02962-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="02962-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="02962-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02962-102">SYNOPSIS</span></span>
<span data-ttu-id="02962-103">Crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="02962-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02962-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02962-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="02962-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02962-105">DESCRIPTION</span></span>
<span data-ttu-id="02962-106">Il cmdlet **New-AzureRmVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="02962-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="02962-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02962-107">EXAMPLES</span></span>

### <span data-ttu-id="02962-108">Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico</span><span class="sxs-lookup"><span data-stu-id="02962-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="02962-109">Questo comando crea l'oggetto Configuration per la creazione di patch.</span><span class="sxs-lookup"><span data-stu-id="02962-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="02962-110">Il comando specifica il giorno della settimana e definisce la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="02962-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="02962-111">Questa configurazione consente di applicare le patch che usano questi valori.</span><span class="sxs-lookup"><span data-stu-id="02962-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="02962-112">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="02962-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="02962-113">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="02962-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="02962-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02962-114">PARAMETERS</span></span>

### <span data-ttu-id="02962-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="02962-115">-DayOfWeek</span></span>
<span data-ttu-id="02962-116">Specifica il giorno della settimana in cui devono essere installati gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="02962-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="02962-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="02962-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02962-118">Domenica</span><span class="sxs-lookup"><span data-stu-id="02962-118">Sunday</span></span>
- <span data-ttu-id="02962-119">Lunedì</span><span class="sxs-lookup"><span data-stu-id="02962-119">Monday</span></span>
- <span data-ttu-id="02962-120">Martedì</span><span class="sxs-lookup"><span data-stu-id="02962-120">Tuesday</span></span>
- <span data-ttu-id="02962-121">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="02962-121">Wednesday</span></span>
- <span data-ttu-id="02962-122">Giovedì</span><span class="sxs-lookup"><span data-stu-id="02962-122">Thursday</span></span>
- <span data-ttu-id="02962-123">Venerdì</span><span class="sxs-lookup"><span data-stu-id="02962-123">Friday</span></span>
- <span data-ttu-id="02962-124">Sabato</span><span class="sxs-lookup"><span data-stu-id="02962-124">Saturday</span></span>
- <span data-ttu-id="02962-125">Quotidiani</span><span class="sxs-lookup"><span data-stu-id="02962-125">Everyday</span></span>

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

### <span data-ttu-id="02962-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="02962-126">-Enable</span></span>
<span data-ttu-id="02962-127">Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="02962-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="02962-128">Se si Abilita la patching automatizzato, il cmdlet inserisce Windows Update in modalità interattiva.</span><span class="sxs-lookup"><span data-stu-id="02962-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="02962-129">Se si disattiva l'aggiornamento automatico, le impostazioni di Windows Update non cambiano.</span><span class="sxs-lookup"><span data-stu-id="02962-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="02962-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="02962-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="02962-131">Specifica la durata, in minuti, della finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="02962-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="02962-132">La correzione automatica consente di evitare l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="02962-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="02962-133">Specificare un multiplo di 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="02962-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="02962-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="02962-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="02962-135">Specifica l'ora del giorno in cui viene avviata la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="02962-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="02962-136">Questa volta definisce gli aggiornamenti che iniziano a essere installati.</span><span class="sxs-lookup"><span data-stu-id="02962-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="02962-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="02962-137">-PatchCategory</span></span>
<span data-ttu-id="02962-138">Specifica se gli aggiornamenti importanti devono essere inclusi.</span><span class="sxs-lookup"><span data-stu-id="02962-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="02962-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02962-139">CommonParameters</span></span>
<span data-ttu-id="02962-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02962-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02962-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02962-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02962-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02962-142">INPUTS</span></span>

### <span data-ttu-id="02962-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="02962-143">None</span></span>
<span data-ttu-id="02962-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="02962-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02962-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02962-145">OUTPUTS</span></span>

### <span data-ttu-id="02962-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="02962-146">AutoPatchingSettings</span></span>
<span data-ttu-id="02962-147">Questo cmdlet restituisce l'oggetto contenente le impostazioni per l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="02962-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="02962-148">Note</span><span class="sxs-lookup"><span data-stu-id="02962-148">NOTES</span></span>

## <span data-ttu-id="02962-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02962-149">RELATED LINKS</span></span>



[<span data-ttu-id="02962-150">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="02962-150">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


