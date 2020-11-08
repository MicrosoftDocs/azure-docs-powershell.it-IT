---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023693"
---
# <span data-ttu-id="fdf67-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fdf67-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="fdf67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdf67-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf67-103">Aggiunge un disco di dati a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdf67-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="fdf67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdf67-104">SYNTAX</span></span>

### <span data-ttu-id="fdf67-105">CreateNew (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdf67-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fdf67-106">Importazione</span><span class="sxs-lookup"><span data-stu-id="fdf67-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdf67-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="fdf67-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fdf67-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdf67-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf67-109">Il cmdlet **Add-AzureDataDisk** aggiunge un disco di dati nuovo o esistente a un oggetto macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf67-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="fdf67-110">Usa il parametro *CreateNew* per creare un nuovo disco dati con le dimensioni e l'etichetta specificate.</span><span class="sxs-lookup"><span data-stu-id="fdf67-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="fdf67-111">Usa il parametro *Import* per allegare un disco esistente dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="fdf67-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="fdf67-112">Usa il parametro *ImportFrom* per allegare un disco esistente da un BLOB in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fdf67-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="fdf67-113">Puoi specificare la modalità cache host del disco dati allegato.</span><span class="sxs-lookup"><span data-stu-id="fdf67-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="fdf67-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdf67-114">EXAMPLES</span></span>

### <span data-ttu-id="fdf67-115">Esempio 1: importare un disco di dati dal repository</span><span class="sxs-lookup"><span data-stu-id="fdf67-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="fdf67-116">Questo comando ottiene un oggetto macchina virtuale per la macchina virtuale denominata VirtualMachine07 nel servizio cloud di ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fdf67-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="fdf67-117">Il comando lo passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdf67-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fdf67-118">Questo comando allega un disco di dati esistente dal repository alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdf67-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="fdf67-119">Il disco dati ha un LUN pari a 0.</span><span class="sxs-lookup"><span data-stu-id="fdf67-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="fdf67-120">Il comando Aggiorna la macchina virtuale per riflettere le modifiche usando il cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fdf67-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="fdf67-121">Esempio 2: aggiungere un nuovo disco di dati</span><span class="sxs-lookup"><span data-stu-id="fdf67-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="fdf67-122">Questo comando ottiene un oggetto macchina virtuale per la macchina virtuale denominata VirtualMachine08.</span><span class="sxs-lookup"><span data-stu-id="fdf67-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="fdf67-123">Il comando lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="fdf67-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="fdf67-124">Questo comando allega un nuovo disco di dati denominato MyNewDisk. vhd.</span><span class="sxs-lookup"><span data-stu-id="fdf67-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="fdf67-125">Il cmdlet crea il disco nel contenitore VHD nell'account di archiviazione predefinito dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="fdf67-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="fdf67-126">Il comando Aggiorna la macchina virtuale per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="fdf67-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="fdf67-127">Esempio 3: aggiungere un disco dati da una posizione specificata</span><span class="sxs-lookup"><span data-stu-id="fdf67-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="fdf67-128">Questo comando ottiene un oggetto macchina virtuale per la macchina virtuale denominata database.</span><span class="sxs-lookup"><span data-stu-id="fdf67-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="fdf67-129">Il comando lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="fdf67-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="fdf67-130">Questo comando allega un disco di dati esistente denominato Disk14. vhd dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="fdf67-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="fdf67-131">Il comando Aggiorna la macchina virtuale per riflettere le modifiche.</span><span class="sxs-lookup"><span data-stu-id="fdf67-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="fdf67-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdf67-132">PARAMETERS</span></span>

### <span data-ttu-id="fdf67-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="fdf67-133">-CreateNew</span></span>
<span data-ttu-id="fdf67-134">Indica che questo cmdlet crea un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fdf67-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="fdf67-135">-DiskLabel</span></span>
<span data-ttu-id="fdf67-136">Specifica l'etichetta del disco per un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fdf67-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-137">-Diskname</span><span class="sxs-lookup"><span data-stu-id="fdf67-137">-DiskName</span></span>
<span data-ttu-id="fdf67-138">Specifica il nome di un disco di dati nel repository del disco.</span><span class="sxs-lookup"><span data-stu-id="fdf67-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fdf67-139">-DiskSizeInGB</span></span>
<span data-ttu-id="fdf67-140">Specifica la dimensione del disco logico, in gigabyte, per un nuovo disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fdf67-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="fdf67-141">-HostCaching</span></span>
<span data-ttu-id="fdf67-142">Specifica le impostazioni di memorizzazione nella cache del livello host del disco.</span><span class="sxs-lookup"><span data-stu-id="fdf67-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="fdf67-143">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="fdf67-143">Valid values are:</span></span> 

- <span data-ttu-id="fdf67-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fdf67-144">None</span></span> 
- <span data-ttu-id="fdf67-145">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="fdf67-145">ReadOnly</span></span> 
- <span data-ttu-id="fdf67-146">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fdf67-146">ReadWrite</span></span>

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

### <span data-ttu-id="fdf67-147">-Import</span><span class="sxs-lookup"><span data-stu-id="fdf67-147">-Import</span></span>
<span data-ttu-id="fdf67-148">Indica che questo cmdlet importa un disco di dati esistente dal repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="fdf67-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="fdf67-149">-ImportFrom</span></span>
<span data-ttu-id="fdf67-150">Indica che questo cmdlet importa un disco di dati esistente da un BLOB in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fdf67-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fdf67-151">-InformationAction</span></span>
<span data-ttu-id="fdf67-152">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="fdf67-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fdf67-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fdf67-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fdf67-154">Continuare</span><span class="sxs-lookup"><span data-stu-id="fdf67-154">Continue</span></span>
- <span data-ttu-id="fdf67-155">Ignora</span><span class="sxs-lookup"><span data-stu-id="fdf67-155">Ignore</span></span>
- <span data-ttu-id="fdf67-156">Informarsi</span><span class="sxs-lookup"><span data-stu-id="fdf67-156">Inquire</span></span>
- <span data-ttu-id="fdf67-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fdf67-157">SilentlyContinue</span></span>
- <span data-ttu-id="fdf67-158">Stop</span><span class="sxs-lookup"><span data-stu-id="fdf67-158">Stop</span></span>
- <span data-ttu-id="fdf67-159">Sospensione</span><span class="sxs-lookup"><span data-stu-id="fdf67-159">Suspend</span></span>

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

### <span data-ttu-id="fdf67-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fdf67-160">-InformationVariable</span></span>
<span data-ttu-id="fdf67-161">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="fdf67-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fdf67-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="fdf67-162">-LUN</span></span>
<span data-ttu-id="fdf67-163">Specifica il numero di unità logica (LUN) per l'unità dati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdf67-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="fdf67-164">I valori validi sono: da 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="fdf67-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="fdf67-165">Ogni disco di dati deve avere un LUN univoco.</span><span class="sxs-lookup"><span data-stu-id="fdf67-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="fdf67-166">-MediaLocation</span></span>
<span data-ttu-id="fdf67-167">Specifica la posizione del BLOB in un account di archiviazione di Azure in cui questo cmdlet archivia il disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fdf67-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="fdf67-168">Se non si specifica una posizione, il cmdlet archivia il disco dati nel contenitore VHD nell'account di archiviazione predefinito per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="fdf67-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="fdf67-169">Se un contenitore VHD non esiste, il cmdlet crea un contenitore VHD.</span><span class="sxs-lookup"><span data-stu-id="fdf67-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf67-170">-Profile</span><span class="sxs-lookup"><span data-stu-id="fdf67-170">-Profile</span></span>
<span data-ttu-id="fdf67-171">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf67-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fdf67-172">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fdf67-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fdf67-173">-VM</span><span class="sxs-lookup"><span data-stu-id="fdf67-173">-VM</span></span>
<span data-ttu-id="fdf67-174">Specifica l'oggetto macchina virtuale a cui questo cmdlet allega un disco di dati.</span><span class="sxs-lookup"><span data-stu-id="fdf67-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="fdf67-175">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="fdf67-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="fdf67-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf67-176">CommonParameters</span></span>
<span data-ttu-id="fdf67-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf67-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf67-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf67-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf67-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdf67-179">INPUTS</span></span>

## <span data-ttu-id="fdf67-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdf67-180">OUTPUTS</span></span>

## <span data-ttu-id="fdf67-181">Note</span><span class="sxs-lookup"><span data-stu-id="fdf67-181">NOTES</span></span>

## <span data-ttu-id="fdf67-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdf67-182">RELATED LINKS</span></span>

[<span data-ttu-id="fdf67-183">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fdf67-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="fdf67-184">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fdf67-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="fdf67-185">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fdf67-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="fdf67-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fdf67-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="fdf67-187">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fdf67-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


