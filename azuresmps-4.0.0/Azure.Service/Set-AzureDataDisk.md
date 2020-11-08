---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029528"
---
# <span data-ttu-id="1f227-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f227-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="1f227-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f227-102">SYNOPSIS</span></span>
<span data-ttu-id="1f227-103">Modifica la memorizzazione nella cache dell'host di un disco di dati esistente in una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f227-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="1f227-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f227-104">SYNTAX</span></span>

### <span data-ttu-id="1f227-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="1f227-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1f227-106">Ridimensionare</span><span class="sxs-lookup"><span data-stu-id="1f227-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f227-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f227-107">DESCRIPTION</span></span>
<span data-ttu-id="1f227-108">Il cmdlet **set-AzureDataDisk** modifica gli attributi della cache di un disco di dati esistente in una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f227-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="1f227-109">Specificare il disco di dati da aggiornare per il numero di unità logica (LUN).</span><span class="sxs-lookup"><span data-stu-id="1f227-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="1f227-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f227-110">EXAMPLES</span></span>

### <span data-ttu-id="1f227-111">Esempio 1: modificare la memorizzazione nella cache dell'host per un disco di dati</span><span class="sxs-lookup"><span data-stu-id="1f227-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="1f227-112">Questo comando ottiene le macchine virtuali eseguite nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1f227-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="1f227-113">Il comando li passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f227-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1f227-114">Questo cmdlet imposta il disco di dati su LUN 2 della macchina virtuale denominato VirtualMachine07 per usare la memorizzazione nella cache dell'host ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="1f227-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="1f227-115">Il comando Aggiorna la macchina virtuale per riflettere le modifiche usando il cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1f227-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="1f227-116">Esempio 2: modificare la memorizzazione nella cache dell'host per tutti i dischi di dati in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="1f227-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="1f227-117">Questo comando ottiene un oggetto per la macchina virtuale denominato VirtualMachine07 nel servizio cloud di ContosoService.</span><span class="sxs-lookup"><span data-stu-id="1f227-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="1f227-118">Il comando lo passa al cmdlet **Get-AzureDataDisk** , che recupera i dischi di dati per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f227-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="1f227-119">Il cmdlet corrente imposta quindi la modalità di memorizzazione nella cache host di ogni disco di dati in ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="1f227-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="1f227-120">Il comando Aggiorna la macchina virtuale per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1f227-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="1f227-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f227-121">PARAMETERS</span></span>

### <span data-ttu-id="1f227-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="1f227-122">-DiskName</span></span>
<span data-ttu-id="1f227-123">Specifica il nome della configurazione del disco dati che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="1f227-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f227-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="1f227-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="1f227-125">La memorizzazione nella cache del disco non è supportata per i dischi 4 TiB e più grandi.</span><span class="sxs-lookup"><span data-stu-id="1f227-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="1f227-126">Se alla VM sono allegati più dischi, ogni disco di dimensioni inferiori a 4 TiB supporterà la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="1f227-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="1f227-127">La modifica dell'impostazione della cache di un disco di Azure si disconnette e riattacca il disco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f227-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="1f227-128">Se si tratta del disco del sistema operativo, la VM viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="1f227-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="1f227-129">Arrestare tutte le applicazioni o i servizi che potrebbero essere interessati da questa interruzione prima di modificare l'impostazione della cache del disco.</span><span class="sxs-lookup"><span data-stu-id="1f227-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="1f227-130">Non seguire tali raccomandazioni può determinare il danneggiamento dei dati.</span><span class="sxs-lookup"><span data-stu-id="1f227-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="1f227-131">Specifica le impostazioni di memorizzazione nella cache del livello host del disco.</span><span class="sxs-lookup"><span data-stu-id="1f227-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="1f227-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1f227-132">Valid values are:</span></span>

- <span data-ttu-id="1f227-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f227-133">None</span></span>
- <span data-ttu-id="1f227-134">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1f227-134">ReadOnly</span></span>
- <span data-ttu-id="1f227-135">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f227-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f227-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1f227-136">-InformationAction</span></span>
<span data-ttu-id="1f227-137">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="1f227-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1f227-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f227-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f227-139">Continuare</span><span class="sxs-lookup"><span data-stu-id="1f227-139">Continue</span></span>
- <span data-ttu-id="1f227-140">Ignora</span><span class="sxs-lookup"><span data-stu-id="1f227-140">Ignore</span></span>
- <span data-ttu-id="1f227-141">Informarsi</span><span class="sxs-lookup"><span data-stu-id="1f227-141">Inquire</span></span>
- <span data-ttu-id="1f227-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1f227-142">SilentlyContinue</span></span>
- <span data-ttu-id="1f227-143">Stop</span><span class="sxs-lookup"><span data-stu-id="1f227-143">Stop</span></span>
- <span data-ttu-id="1f227-144">Sospensione</span><span class="sxs-lookup"><span data-stu-id="1f227-144">Suspend</span></span>

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

### <span data-ttu-id="1f227-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1f227-145">-InformationVariable</span></span>
<span data-ttu-id="1f227-146">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="1f227-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1f227-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="1f227-147">-LUN</span></span>
<span data-ttu-id="1f227-148">Specifica il LUN per l'unità dati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f227-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="1f227-149">I valori validi sono: da 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="1f227-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f227-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="1f227-150">-Profile</span></span>
<span data-ttu-id="1f227-151">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f227-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f227-152">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1f227-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f227-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1f227-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="1f227-154">Specifica le nuove dimensioni, in gigabyte, per il disco dati.</span><span class="sxs-lookup"><span data-stu-id="1f227-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="1f227-155">La nuova dimensione deve essere superiore alle dimensioni correnti.</span><span class="sxs-lookup"><span data-stu-id="1f227-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f227-156">-VM</span><span class="sxs-lookup"><span data-stu-id="1f227-156">-VM</span></span>
<span data-ttu-id="1f227-157">Specifica l'oggetto macchina virtuale associato al disco di dati.</span><span class="sxs-lookup"><span data-stu-id="1f227-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="1f227-158">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="1f227-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f227-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f227-159">CommonParameters</span></span>
<span data-ttu-id="1f227-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f227-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f227-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f227-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f227-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f227-162">INPUTS</span></span>

## <span data-ttu-id="1f227-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f227-163">OUTPUTS</span></span>

## <span data-ttu-id="1f227-164">Note</span><span class="sxs-lookup"><span data-stu-id="1f227-164">NOTES</span></span>

## <span data-ttu-id="1f227-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f227-165">RELATED LINKS</span></span>

[<span data-ttu-id="1f227-166">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f227-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="1f227-167">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1f227-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1f227-168">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f227-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="1f227-169">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="1f227-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="1f227-170">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1f227-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


