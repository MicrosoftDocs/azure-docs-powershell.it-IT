---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029653"
---
# <span data-ttu-id="d35e6-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d35e6-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="d35e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d35e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d35e6-103">Crea un oggetto Configuration per l'aggiornamento automatico della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d35e6-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="d35e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d35e6-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d35e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d35e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d35e6-106">Il cmdlet **New-AzureVMSqlServerAutoPatchingConfig** crea un oggetto Configuration per l'aggiornamento automatico della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d35e6-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="d35e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d35e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d35e6-108">Esempio 1: creare un oggetto di configurazione per configurare l'aggiornamento automatico</span><span class="sxs-lookup"><span data-stu-id="d35e6-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="d35e6-109">Questo comando crea un oggetto Configuration che può essere usato per configurare l'aggiornamento automatico tramite set-AzureVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="d35e6-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="d35e6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d35e6-110">PARAMETERS</span></span>

### <span data-ttu-id="d35e6-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d35e6-111">-DayOfWeek</span></span>
<span data-ttu-id="d35e6-112">Specifica il giorno della settimana in cui devono essere installati gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="d35e6-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="d35e6-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d35e6-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d35e6-114">Domenica</span><span class="sxs-lookup"><span data-stu-id="d35e6-114">Sunday</span></span>
- <span data-ttu-id="d35e6-115">Lunedì</span><span class="sxs-lookup"><span data-stu-id="d35e6-115">Monday</span></span>
- <span data-ttu-id="d35e6-116">Martedì</span><span class="sxs-lookup"><span data-stu-id="d35e6-116">Tuesday</span></span>
- <span data-ttu-id="d35e6-117">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="d35e6-117">Wednesday</span></span>
- <span data-ttu-id="d35e6-118">Giovedì</span><span class="sxs-lookup"><span data-stu-id="d35e6-118">Thursday</span></span>
- <span data-ttu-id="d35e6-119">Venerdì</span><span class="sxs-lookup"><span data-stu-id="d35e6-119">Friday</span></span>
- <span data-ttu-id="d35e6-120">Sabato</span><span class="sxs-lookup"><span data-stu-id="d35e6-120">Saturday</span></span>
- <span data-ttu-id="d35e6-121">Quotidiani</span><span class="sxs-lookup"><span data-stu-id="d35e6-121">Everyday</span></span>

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

### <span data-ttu-id="d35e6-122">-Enable</span><span class="sxs-lookup"><span data-stu-id="d35e6-122">-Enable</span></span>
<span data-ttu-id="d35e6-123">Indica che è abilitata l'attivazione automatica delle patch per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d35e6-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="d35e6-124">Se si Abilita l'applicazione di patch automatica, il cmdlet verrà inserito in modalità interattiva in Windows Update.</span><span class="sxs-lookup"><span data-stu-id="d35e6-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="d35e6-125">Se si disattiva la correzione automatica, le impostazioni di Windows Update non verranno modificate.</span><span class="sxs-lookup"><span data-stu-id="d35e6-125">If you disable automated patching, Windows Update settings will not change.</span></span>

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

### <span data-ttu-id="d35e6-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d35e6-126">-InformationAction</span></span>
<span data-ttu-id="d35e6-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d35e6-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d35e6-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d35e6-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d35e6-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="d35e6-129">Continue</span></span>
- <span data-ttu-id="d35e6-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="d35e6-130">Ignore</span></span>
- <span data-ttu-id="d35e6-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d35e6-131">Inquire</span></span>
- <span data-ttu-id="d35e6-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d35e6-132">SilentlyContinue</span></span>
- <span data-ttu-id="d35e6-133">Stop</span><span class="sxs-lookup"><span data-stu-id="d35e6-133">Stop</span></span>
- <span data-ttu-id="d35e6-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d35e6-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35e6-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d35e6-135">-InformationVariable</span></span>
<span data-ttu-id="d35e6-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d35e6-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35e6-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="d35e6-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="d35e6-138">Specifica la durata della finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d35e6-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="d35e6-139">La patching automatizzato eviterà l'esecuzione di un'azione che può influire sulla disponibilità di una macchina virtuale all'esterno della finestra.</span><span class="sxs-lookup"><span data-stu-id="d35e6-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="d35e6-140">Sono consentiti solo 30 minuti di incrementi.</span><span class="sxs-lookup"><span data-stu-id="d35e6-140">Only 30 minutes increments are allowed.</span></span>

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

### <span data-ttu-id="d35e6-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="d35e6-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="d35e6-142">Specifica l'ora del giorno in cui viene avviata la finestra di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d35e6-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="d35e6-143">Questa volta definisce quando si avvia l'installazione degli aggiornamenti e viene arrotondato all'ora.</span><span class="sxs-lookup"><span data-stu-id="d35e6-143">This time defines when updates start installing and is rounded to the hour.</span></span>

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

### <span data-ttu-id="d35e6-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="d35e6-144">-PatchCategory</span></span>
<span data-ttu-id="d35e6-145">Specifica se gli aggiornamenti importanti devono essere inclusi.</span><span class="sxs-lookup"><span data-stu-id="d35e6-145">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="d35e6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35e6-146">CommonParameters</span></span>
<span data-ttu-id="d35e6-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d35e6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35e6-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d35e6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35e6-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d35e6-149">INPUTS</span></span>

## <span data-ttu-id="d35e6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d35e6-150">OUTPUTS</span></span>

### <span data-ttu-id="d35e6-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d35e6-151">AutoPatchingSettings</span></span>
<span data-ttu-id="d35e6-152">Questo cmdlet restituisce l'oggetto contenente le impostazioni per l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="d35e6-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="d35e6-153">Note</span><span class="sxs-lookup"><span data-stu-id="d35e6-153">NOTES</span></span>

## <span data-ttu-id="d35e6-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d35e6-154">RELATED LINKS</span></span>

[<span data-ttu-id="d35e6-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d35e6-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="d35e6-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d35e6-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="d35e6-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d35e6-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


