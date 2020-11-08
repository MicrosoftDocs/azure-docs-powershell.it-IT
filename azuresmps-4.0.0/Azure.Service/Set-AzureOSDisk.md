---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023786"
---
# <span data-ttu-id="37270-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="37270-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="37270-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37270-102">SYNOPSIS</span></span>
<span data-ttu-id="37270-103">Modifica la modalità cache ospitante di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="37270-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="37270-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37270-104">SYNTAX</span></span>

### <span data-ttu-id="37270-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="37270-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="37270-106">Ridimensionare</span><span class="sxs-lookup"><span data-stu-id="37270-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="37270-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37270-107">DESCRIPTION</span></span>
<span data-ttu-id="37270-108">Il cmdlet **set-AzureOSDisk** modifica la modalità cache host del disco del sistema operativo di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="37270-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="37270-109">Le modalità cache host supportate sono ReadOnly e ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="37270-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="37270-110">Se si esegue questo cmdlet in una macchina virtuale in esecuzione, la macchina virtuale viene riavviata.</span><span class="sxs-lookup"><span data-stu-id="37270-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="37270-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37270-111">EXAMPLES</span></span>

### <span data-ttu-id="37270-112">Esempio 1: impostare la modalità cache host su ReadOnly tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="37270-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="37270-113">Questo comando ottiene la macchina virtuale denominata VirtualMachine02 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="37270-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="37270-114">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="37270-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37270-115">Il cmdlet Current imposta la modalità cache host del disco del sistema operativo della macchina virtuale in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="37270-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="37270-116">Esempio 2: impostare la modalità cache host su ReadWrite</span><span class="sxs-lookup"><span data-stu-id="37270-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="37270-117">Il primo comando consente di ottenere la macchina virtuale denominata VirtualMachine02 nel servizio denominato ContosoService e quindi di archiviarla nella variabile.</span><span class="sxs-lookup"><span data-stu-id="37270-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="37270-118">Il secondo comando imposta la modalità cache host del disco del sistema operativo della macchina virtuale che deve essere ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="37270-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="37270-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37270-119">PARAMETERS</span></span>

### <span data-ttu-id="37270-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="37270-120">-HostCaching</span></span>
<span data-ttu-id="37270-121">Specifica l'attributo della cache host per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="37270-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="37270-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="37270-122">Valid values are:</span></span> 

- <span data-ttu-id="37270-123">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="37270-123">ReadOnly</span></span> 
- <span data-ttu-id="37270-124">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="37270-124">ReadWrite</span></span>

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37270-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="37270-125">-InformationAction</span></span>
<span data-ttu-id="37270-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="37270-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="37270-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37270-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37270-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="37270-128">Continue</span></span>
- <span data-ttu-id="37270-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="37270-129">Ignore</span></span>
- <span data-ttu-id="37270-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="37270-130">Inquire</span></span>
- <span data-ttu-id="37270-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="37270-131">SilentlyContinue</span></span>
- <span data-ttu-id="37270-132">Stop</span><span class="sxs-lookup"><span data-stu-id="37270-132">Stop</span></span>
- <span data-ttu-id="37270-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="37270-133">Suspend</span></span>

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

### <span data-ttu-id="37270-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="37270-134">-InformationVariable</span></span>
<span data-ttu-id="37270-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="37270-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="37270-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="37270-136">-Profile</span></span>
<span data-ttu-id="37270-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37270-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37270-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="37270-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37270-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="37270-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="37270-140">Specifica una nuova dimensione, in gigabyte, per il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="37270-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="37270-141">Le dimensioni devono essere superiori alle dimensioni correnti.</span><span class="sxs-lookup"><span data-stu-id="37270-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37270-142">-VM</span><span class="sxs-lookup"><span data-stu-id="37270-142">-VM</span></span>
<span data-ttu-id="37270-143">Specifica la macchina virtuale per cui questo cmdlet modifica il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="37270-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="37270-144">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="37270-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="37270-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37270-145">CommonParameters</span></span>
<span data-ttu-id="37270-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37270-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37270-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37270-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37270-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37270-148">INPUTS</span></span>

## <span data-ttu-id="37270-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37270-149">OUTPUTS</span></span>

## <span data-ttu-id="37270-150">Note</span><span class="sxs-lookup"><span data-stu-id="37270-150">NOTES</span></span>

## <span data-ttu-id="37270-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37270-151">RELATED LINKS</span></span>

[<span data-ttu-id="37270-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="37270-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="37270-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="37270-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="37270-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="37270-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="37270-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="37270-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="37270-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="37270-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="37270-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="37270-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


