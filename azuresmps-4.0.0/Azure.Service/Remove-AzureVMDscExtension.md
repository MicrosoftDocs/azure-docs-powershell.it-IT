---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029909"
---
# <span data-ttu-id="8ae1a-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ae1a-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="8ae1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ae1a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae1a-103">Rimuove un'estensione di Azure DSC da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="8ae1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ae1a-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ae1a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ae1a-105">DESCRIPTION</span></span>
<span data-ttu-id="8ae1a-106">Il cmdlet **Remove-AzureVMDscExtension** rimuove un'estensione di Azure DSC da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="8ae1a-107">L'output di questo cmdlet deve essere inviato tramite pipe al cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8ae1a-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="8ae1a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ae1a-108">EXAMPLES</span></span>

### <span data-ttu-id="8ae1a-109">Esempio 1: rimuovere un'estensione DSC da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8ae1a-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="8ae1a-110">Questo comando rimuove un'estensione di Azure DSC da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="8ae1a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ae1a-111">PARAMETERS</span></span>

### <span data-ttu-id="8ae1a-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8ae1a-112">-InformationAction</span></span>
<span data-ttu-id="8ae1a-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8ae1a-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ae1a-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ae1a-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="8ae1a-115">Continue</span></span>
- <span data-ttu-id="8ae1a-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="8ae1a-116">Ignore</span></span>
- <span data-ttu-id="8ae1a-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8ae1a-117">Inquire</span></span>
- <span data-ttu-id="8ae1a-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8ae1a-118">SilentlyContinue</span></span>
- <span data-ttu-id="8ae1a-119">Stop</span><span class="sxs-lookup"><span data-stu-id="8ae1a-119">Stop</span></span>
- <span data-ttu-id="8ae1a-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8ae1a-120">Suspend</span></span>

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

### <span data-ttu-id="8ae1a-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8ae1a-121">-InformationVariable</span></span>
<span data-ttu-id="8ae1a-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8ae1a-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="8ae1a-123">-Profile</span></span>
<span data-ttu-id="8ae1a-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ae1a-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ae1a-126">-VM</span><span class="sxs-lookup"><span data-stu-id="8ae1a-126">-VM</span></span>
<span data-ttu-id="8ae1a-127">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8ae1a-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ae1a-128">-Confirm</span></span>
<span data-ttu-id="8ae1a-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae1a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae1a-130">-WhatIf</span></span>
<span data-ttu-id="8ae1a-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae1a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae1a-133">CommonParameters</span></span>
<span data-ttu-id="8ae1a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae1a-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae1a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae1a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ae1a-136">INPUTS</span></span>

## <span data-ttu-id="8ae1a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ae1a-137">OUTPUTS</span></span>

## <span data-ttu-id="8ae1a-138">Note</span><span class="sxs-lookup"><span data-stu-id="8ae1a-138">NOTES</span></span>

## <span data-ttu-id="8ae1a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ae1a-139">RELATED LINKS</span></span>

[<span data-ttu-id="8ae1a-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ae1a-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="8ae1a-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ae1a-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="8ae1a-142">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8ae1a-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


