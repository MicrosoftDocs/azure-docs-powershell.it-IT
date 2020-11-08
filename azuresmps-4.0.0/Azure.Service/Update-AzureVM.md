---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029475"
---
# <span data-ttu-id="2dda4-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-101">Update-AzureVM</span></span>

## <span data-ttu-id="2dda4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dda4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dda4-103">Modifica la configurazione di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda4-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="2dda4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dda4-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2dda4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dda4-105">DESCRIPTION</span></span>
<span data-ttu-id="2dda4-106">Il cmdlet **Update-AzureVM** accetta le informazioni sull'aggiornamento per la macchina virtuale specificata e avvia l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2dda4-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="2dda4-107">È possibile aggiungere o rimuovere dischi di dati, modificare la modalità cache di dischi di dati o sistemi operativi, modificare gli endpoint di rete o modificare le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2dda4-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="2dda4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dda4-108">EXAMPLES</span></span>

### <span data-ttu-id="2dda4-109">Esempio 1: aggiornare le dimensioni di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2dda4-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="2dda4-110">Questo comando modifica le dimensioni della macchina virtuale denominata VirtualMachine04, in corso nel servizio denominato ContosoService03, su media.</span><span class="sxs-lookup"><span data-stu-id="2dda4-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="2dda4-111">Esempio 2: aggiungere un disco di dati a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2dda4-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="2dda4-112">Questo comando aggiunge un nuovo disco dati alla macchina virtuale denominata VirtualMachine05, in corso nel servizio denominato ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="2dda4-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="2dda4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dda4-113">PARAMETERS</span></span>

### <span data-ttu-id="2dda4-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2dda4-114">-InformationAction</span></span>
<span data-ttu-id="2dda4-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="2dda4-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2dda4-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2dda4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dda4-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="2dda4-117">Continue</span></span>
- <span data-ttu-id="2dda4-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="2dda4-118">Ignore</span></span>
- <span data-ttu-id="2dda4-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="2dda4-119">Inquire</span></span>
- <span data-ttu-id="2dda4-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2dda4-120">SilentlyContinue</span></span>
- <span data-ttu-id="2dda4-121">Stop</span><span class="sxs-lookup"><span data-stu-id="2dda4-121">Stop</span></span>
- <span data-ttu-id="2dda4-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="2dda4-122">Suspend</span></span>

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

### <span data-ttu-id="2dda4-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2dda4-123">-InformationVariable</span></span>
<span data-ttu-id="2dda4-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="2dda4-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2dda4-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dda4-125">-Name</span></span>
<span data-ttu-id="2dda4-126">Specifica il nome della macchina virtuale da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2dda4-126">Specifies the name of the virtual machine to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="2dda4-127">-Profile</span></span>
<span data-ttu-id="2dda4-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dda4-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2dda4-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2dda4-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2dda4-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2dda4-130">-ServiceName</span></span>
<span data-ttu-id="2dda4-131">Specifica il nome del servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="2dda4-131">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-132">-VM</span><span class="sxs-lookup"><span data-stu-id="2dda4-132">-VM</span></span>
<span data-ttu-id="2dda4-133">Specifica l'oggetto macchina virtuale che include le impostazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="2dda4-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dda4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dda4-134">CommonParameters</span></span>
<span data-ttu-id="2dda4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dda4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dda4-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dda4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dda4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dda4-137">INPUTS</span></span>

## <span data-ttu-id="2dda4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dda4-138">OUTPUTS</span></span>

## <span data-ttu-id="2dda4-139">Note</span><span class="sxs-lookup"><span data-stu-id="2dda4-139">NOTES</span></span>

## <span data-ttu-id="2dda4-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dda4-140">RELATED LINKS</span></span>

[<span data-ttu-id="2dda4-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="2dda4-142">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="2dda4-143">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="2dda4-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="2dda4-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="2dda4-145">Riavviare-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="2dda4-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="2dda4-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="2dda4-147">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="2dda4-148">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2dda4-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


