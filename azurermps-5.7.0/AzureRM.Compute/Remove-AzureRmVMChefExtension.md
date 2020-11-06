---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514472"
---
# <span data-ttu-id="414e0-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="414e0-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="414e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="414e0-102">SYNOPSIS</span></span>
<span data-ttu-id="414e0-103">Rimuove l'estensione dello chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="414e0-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="414e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="414e0-104">SYNTAX</span></span>

### <span data-ttu-id="414e0-105">Linux</span><span class="sxs-lookup"><span data-stu-id="414e0-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="414e0-106">Windows</span><span class="sxs-lookup"><span data-stu-id="414e0-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="414e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="414e0-107">DESCRIPTION</span></span>
<span data-ttu-id="414e0-108">Il cmdlet **Remove-AzureVMChefExtension** rimuove l'estensione chef da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="414e0-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="414e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="414e0-109">EXAMPLES</span></span>

### <span data-ttu-id="414e0-110">Esempio 1: rimuovere un'estensione dello chef da una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="414e0-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="414e0-111">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="414e0-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="414e0-112">Esempio 2: rimuovere un'estensione dello chef da una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="414e0-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="414e0-113">Questo comando consente di rimuovere un'estensione di chef da una macchina virtuale basata su Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="414e0-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="414e0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="414e0-114">PARAMETERS</span></span>

### <span data-ttu-id="414e0-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="414e0-115">-Linux</span></span>
<span data-ttu-id="414e0-116">Indica che questo cmdlet è destinato a una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="414e0-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414e0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="414e0-117">-Name</span></span>
<span data-ttu-id="414e0-118">Specifica il nome dell'estensione dello chef rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="414e0-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414e0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="414e0-119">-ResourceGroupName</span></span>
<span data-ttu-id="414e0-120">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="414e0-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="414e0-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="414e0-121">-VMName</span></span>
<span data-ttu-id="414e0-122">Specifica il nome di una macchina virtuale per cui questo cmdlet rimuove l'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="414e0-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414e0-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="414e0-123">-Windows</span></span>
<span data-ttu-id="414e0-124">Indica che questo cmdlet è destinato a una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="414e0-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414e0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="414e0-125">-Confirm</span></span>
<span data-ttu-id="414e0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="414e0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="414e0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414e0-127">-WhatIf</span></span>
<span data-ttu-id="414e0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="414e0-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="414e0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="414e0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="414e0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="414e0-130">CommonParameters</span></span>
<span data-ttu-id="414e0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="414e0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="414e0-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="414e0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="414e0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="414e0-133">INPUTS</span></span>

### <span data-ttu-id="414e0-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="414e0-134">None</span></span>
<span data-ttu-id="414e0-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="414e0-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="414e0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="414e0-136">OUTPUTS</span></span>

## <span data-ttu-id="414e0-137">Note</span><span class="sxs-lookup"><span data-stu-id="414e0-137">NOTES</span></span>

## <span data-ttu-id="414e0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="414e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="414e0-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="414e0-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="414e0-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="414e0-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
