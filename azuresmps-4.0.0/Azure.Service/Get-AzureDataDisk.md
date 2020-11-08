---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023609"
---
# <span data-ttu-id="60d0a-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="60d0a-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="60d0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="60d0a-103">Ottiene i dischi di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="60d0a-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="60d0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60d0a-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="60d0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="60d0a-106">Il cmdlet **Get-AzureDataDisk** ottiene un oggetto che rappresenta i dischi di dati in una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="60d0a-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="60d0a-107">Per ottenere un oggetto disco dati specifico, specificare il numero di unità logica (LUN) del disco.</span><span class="sxs-lookup"><span data-stu-id="60d0a-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="60d0a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60d0a-108">EXAMPLES</span></span>

### <span data-ttu-id="60d0a-109">Esempio 1: ottenere tutti i dischi di dati per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="60d0a-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="60d0a-110">Questo comando ottiene la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="60d0a-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="60d0a-111">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="60d0a-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="60d0a-112">Il cmdlet corrente recupera tutti i dischi di dati per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="60d0a-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="60d0a-113">Esempio 2: ottenere uno specifico disco dati per un vituralvirtual machinevirtual</span><span class="sxs-lookup"><span data-stu-id="60d0a-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="60d0a-114">Questo comando consente di ottenere la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="60d0a-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="60d0a-115">Il comando passa la macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="60d0a-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="60d0a-116">Il cmdlet corrente ottiene il disco di dati con il LUN 2.</span><span class="sxs-lookup"><span data-stu-id="60d0a-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="60d0a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60d0a-117">PARAMETERS</span></span>

### <span data-ttu-id="60d0a-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="60d0a-118">-InformationAction</span></span>
<span data-ttu-id="60d0a-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="60d0a-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="60d0a-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60d0a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60d0a-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="60d0a-121">Continue</span></span>
- <span data-ttu-id="60d0a-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="60d0a-122">Ignore</span></span>
- <span data-ttu-id="60d0a-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="60d0a-123">Inquire</span></span>
- <span data-ttu-id="60d0a-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="60d0a-124">SilentlyContinue</span></span>
- <span data-ttu-id="60d0a-125">Stop</span><span class="sxs-lookup"><span data-stu-id="60d0a-125">Stop</span></span>
- <span data-ttu-id="60d0a-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="60d0a-126">Suspend</span></span>

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

### <span data-ttu-id="60d0a-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="60d0a-127">-InformationVariable</span></span>
<span data-ttu-id="60d0a-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="60d0a-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="60d0a-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="60d0a-129">-Lun</span></span>
<span data-ttu-id="60d0a-130">Specifica il LUN per l'unità dati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="60d0a-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="60d0a-131">I valori validi sono: da 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="60d0a-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d0a-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="60d0a-132">-Profile</span></span>
<span data-ttu-id="60d0a-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60d0a-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="60d0a-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="60d0a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60d0a-135">-VM</span><span class="sxs-lookup"><span data-stu-id="60d0a-135">-VM</span></span>
<span data-ttu-id="60d0a-136">Specifica l'oggetto macchina virtuale per cui questo cmdlet recupera i dischi dati.</span><span class="sxs-lookup"><span data-stu-id="60d0a-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="60d0a-137">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="60d0a-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="60d0a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d0a-138">CommonParameters</span></span>
<span data-ttu-id="60d0a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d0a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d0a-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d0a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d0a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60d0a-141">INPUTS</span></span>

## <span data-ttu-id="60d0a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60d0a-142">OUTPUTS</span></span>

## <span data-ttu-id="60d0a-143">Note</span><span class="sxs-lookup"><span data-stu-id="60d0a-143">NOTES</span></span>

## <span data-ttu-id="60d0a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60d0a-144">RELATED LINKS</span></span>

[<span data-ttu-id="60d0a-145">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="60d0a-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="60d0a-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="60d0a-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="60d0a-147">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="60d0a-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="60d0a-148">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="60d0a-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


