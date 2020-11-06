---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514475"
---
# <span data-ttu-id="e55b8-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e55b8-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="e55b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e55b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e55b8-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e55b8-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e55b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e55b8-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e55b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e55b8-106">Il cmdlet **Remove-AzureRmVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e55b8-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="e55b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e55b8-107">EXAMPLES</span></span>

## <span data-ttu-id="e55b8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e55b8-108">PARAMETERS</span></span>

### <span data-ttu-id="e55b8-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e55b8-109">-Force</span></span>
<span data-ttu-id="e55b8-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e55b8-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e55b8-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e55b8-111">-Name</span></span>
<span data-ttu-id="e55b8-112">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e55b8-112">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e55b8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55b8-113">-ResourceGroupName</span></span>
<span data-ttu-id="e55b8-114">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e55b8-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e55b8-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="e55b8-115">-VMName</span></span>
<span data-ttu-id="e55b8-116">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e55b8-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e55b8-117">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e55b8-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e55b8-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e55b8-118">-Confirm</span></span>
<span data-ttu-id="e55b8-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e55b8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55b8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55b8-120">-WhatIf</span></span>
<span data-ttu-id="e55b8-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e55b8-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e55b8-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e55b8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55b8-123">CommonParameters</span></span>
<span data-ttu-id="e55b8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e55b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55b8-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e55b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55b8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e55b8-126">INPUTS</span></span>

### <span data-ttu-id="e55b8-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e55b8-127">None</span></span>
<span data-ttu-id="e55b8-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e55b8-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e55b8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e55b8-129">OUTPUTS</span></span>

## <span data-ttu-id="e55b8-130">Note</span><span class="sxs-lookup"><span data-stu-id="e55b8-130">NOTES</span></span>

## <span data-ttu-id="e55b8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e55b8-131">RELATED LINKS</span></span>

[<span data-ttu-id="e55b8-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e55b8-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="e55b8-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e55b8-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="e55b8-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="e55b8-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
