---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023474"
---
# <span data-ttu-id="49547-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49547-101">Remove-AzureVM</span></span>

## <span data-ttu-id="49547-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49547-102">SYNOPSIS</span></span>
<span data-ttu-id="49547-103">Rimuove una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="49547-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="49547-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49547-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49547-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49547-105">DESCRIPTION</span></span>
<span data-ttu-id="49547-106">Il cmdlet **Remove-AzureVM** Elimina una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="49547-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="49547-107">Questo processo non elimina i file con estensione vhd sottostanti dei dischi installati nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49547-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="49547-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49547-108">EXAMPLES</span></span>

### <span data-ttu-id="49547-109">Esempio 1: rimuovere una macchina virtuale da un servizio</span><span class="sxs-lookup"><span data-stu-id="49547-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="49547-110">Questo comando rimuove la macchina virtuale denominata VirtualMachine03 eseguita nel servizio ContosoService03.</span><span class="sxs-lookup"><span data-stu-id="49547-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="49547-111">Esempio 2: rimuovere una macchina virtuale ed eliminare i file con estensione VHD</span><span class="sxs-lookup"><span data-stu-id="49547-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="49547-112">Questo comando rimuove la macchina virtuale VirtualMachine04 eseguita nel servizio ContosoService03 e specifica di rimuovere i file con estensione VHD tramite il parametro *DeleteVHD* .</span><span class="sxs-lookup"><span data-stu-id="49547-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="49547-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49547-113">PARAMETERS</span></span>

### <span data-ttu-id="49547-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="49547-114">-DeleteVHD</span></span>
<span data-ttu-id="49547-115">Specifica se questo cmdlet rimuove la macchina virtuale e i BLOB del disco sottostante.</span><span class="sxs-lookup"><span data-stu-id="49547-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49547-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="49547-116">-InformationAction</span></span>
<span data-ttu-id="49547-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="49547-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="49547-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="49547-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49547-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="49547-119">Continue</span></span>
- <span data-ttu-id="49547-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="49547-120">Ignore</span></span>
- <span data-ttu-id="49547-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="49547-121">Inquire</span></span>
- <span data-ttu-id="49547-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="49547-122">SilentlyContinue</span></span>
- <span data-ttu-id="49547-123">Stop</span><span class="sxs-lookup"><span data-stu-id="49547-123">Stop</span></span>
- <span data-ttu-id="49547-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="49547-124">Suspend</span></span>

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

### <span data-ttu-id="49547-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="49547-125">-InformationVariable</span></span>
<span data-ttu-id="49547-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="49547-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="49547-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="49547-127">-Name</span></span>
<span data-ttu-id="49547-128">Specifica il nome della macchina virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="49547-128">Specifies the name of the virtual machine being removed.</span></span>

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

### <span data-ttu-id="49547-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="49547-129">-Profile</span></span>
<span data-ttu-id="49547-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49547-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49547-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="49547-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49547-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49547-132">-ServiceName</span></span>
<span data-ttu-id="49547-133">Specifica il nome del servizio Azure da cui viene rimossa la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49547-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="49547-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49547-134">-Confirm</span></span>
<span data-ttu-id="49547-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49547-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49547-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49547-136">-WhatIf</span></span>
<span data-ttu-id="49547-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49547-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49547-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49547-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49547-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49547-139">CommonParameters</span></span>
<span data-ttu-id="49547-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49547-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49547-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49547-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49547-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49547-142">INPUTS</span></span>

## <span data-ttu-id="49547-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49547-143">OUTPUTS</span></span>

## <span data-ttu-id="49547-144">Note</span><span class="sxs-lookup"><span data-stu-id="49547-144">NOTES</span></span>

## <span data-ttu-id="49547-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49547-145">RELATED LINKS</span></span>

[<span data-ttu-id="49547-146">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49547-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="49547-147">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="49547-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="49547-148">Riavviare-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49547-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="49547-149">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49547-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="49547-150">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49547-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="49547-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="49547-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


