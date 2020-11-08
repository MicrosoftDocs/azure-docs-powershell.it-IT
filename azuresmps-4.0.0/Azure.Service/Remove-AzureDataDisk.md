---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029628"
---
# <span data-ttu-id="ade52-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="ade52-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="ade52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ade52-102">SYNOPSIS</span></span>
<span data-ttu-id="ade52-103">Rimuove un disco di dati da una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ade52-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="ade52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ade52-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ade52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ade52-105">DESCRIPTION</span></span>
<span data-ttu-id="ade52-106">Il cmdlet **Remove-AzureDataDisk** rimuove un disco di dati da una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ade52-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="ade52-107">Per impostazione predefinita, questo cmdlet non rimuove il BLOB del disco dati dall'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ade52-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="ade52-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ade52-108">EXAMPLES</span></span>

### <span data-ttu-id="ade52-109">Esempio 1: rimuovere un disco di dati</span><span class="sxs-lookup"><span data-stu-id="ade52-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="ade52-110">Questo comando ottiene la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ade52-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ade52-111">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ade52-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ade52-112">Il cmdlet corrente rimuove il disco di dati con il LUN 0.</span><span class="sxs-lookup"><span data-stu-id="ade52-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="ade52-113">Esempio 2: rimuovere un disco di dati e il file del disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="ade52-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="ade52-114">Questo comando consente di ottenere la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="ade52-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="ade52-115">Il comando passa la macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="ade52-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="ade52-116">Il cmdlet corrente rimuove il disco di dati con il LUN 0.</span><span class="sxs-lookup"><span data-stu-id="ade52-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="ade52-117">Il comando include il parametro *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="ade52-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="ade52-118">Elimina pertanto anche il disco rigido virtuale sottostante.</span><span class="sxs-lookup"><span data-stu-id="ade52-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="ade52-119">Il comando Aggiorna la macchina virtuale per riflettere le modifiche usando il cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ade52-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="ade52-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ade52-120">PARAMETERS</span></span>

### <span data-ttu-id="ade52-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="ade52-121">-DeleteVHD</span></span>
<span data-ttu-id="ade52-122">Indica che questo cmdlet rimuove il disco di dati e il disco rigido virtuale (VHD) dallo spazio di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="ade52-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade52-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ade52-123">-InformationAction</span></span>
<span data-ttu-id="ade52-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ade52-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ade52-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ade52-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ade52-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="ade52-126">Continue</span></span>
- <span data-ttu-id="ade52-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="ade52-127">Ignore</span></span>
- <span data-ttu-id="ade52-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ade52-128">Inquire</span></span>
- <span data-ttu-id="ade52-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ade52-129">SilentlyContinue</span></span>
- <span data-ttu-id="ade52-130">Stop</span><span class="sxs-lookup"><span data-stu-id="ade52-130">Stop</span></span>
- <span data-ttu-id="ade52-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ade52-131">Suspend</span></span>

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

### <span data-ttu-id="ade52-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ade52-132">-InformationVariable</span></span>
<span data-ttu-id="ade52-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ade52-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ade52-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="ade52-134">-LUN</span></span>
<span data-ttu-id="ade52-135">Specifica il numero di unità logica (LUN) per l'unità dati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ade52-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="ade52-136">I valori validi sono: da 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="ade52-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade52-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="ade52-137">-Profile</span></span>
<span data-ttu-id="ade52-138">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade52-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ade52-139">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ade52-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ade52-140">-VM</span><span class="sxs-lookup"><span data-stu-id="ade52-140">-VM</span></span>
<span data-ttu-id="ade52-141">Specifica l'oggetto macchina virtuale associato al disco di dati.</span><span class="sxs-lookup"><span data-stu-id="ade52-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="ade52-142">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ade52-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="ade52-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade52-143">CommonParameters</span></span>
<span data-ttu-id="ade52-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade52-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade52-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade52-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade52-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ade52-146">INPUTS</span></span>

## <span data-ttu-id="ade52-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ade52-147">OUTPUTS</span></span>

## <span data-ttu-id="ade52-148">Note</span><span class="sxs-lookup"><span data-stu-id="ade52-148">NOTES</span></span>

## <span data-ttu-id="ade52-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ade52-149">RELATED LINKS</span></span>

[<span data-ttu-id="ade52-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="ade52-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="ade52-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="ade52-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="ade52-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade52-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ade52-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="ade52-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="ade52-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ade52-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


