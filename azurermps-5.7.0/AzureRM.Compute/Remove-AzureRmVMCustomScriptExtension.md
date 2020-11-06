---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514467"
---
# <span data-ttu-id="88717-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="88717-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="88717-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88717-102">SYNOPSIS</span></span>
<span data-ttu-id="88717-103">Rimuove un'estensione di script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88717-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88717-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88717-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88717-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88717-105">DESCRIPTION</span></span>
<span data-ttu-id="88717-106">Il cmdlet **Remove-AzureRmVMCustomScriptExtension** rimuove un'estensione di una macchina virtuale script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88717-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="88717-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88717-107">EXAMPLES</span></span>

## <span data-ttu-id="88717-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88717-108">PARAMETERS</span></span>

### <span data-ttu-id="88717-109">-Force</span><span class="sxs-lookup"><span data-stu-id="88717-109">-Force</span></span>
<span data-ttu-id="88717-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="88717-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88717-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="88717-111">-Name</span></span>
<span data-ttu-id="88717-112">Specifica il nome dell'estensione di script personalizzata rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88717-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88717-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88717-113">-ResourceGroupName</span></span>
<span data-ttu-id="88717-114">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88717-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="88717-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="88717-115">-VMName</span></span>
<span data-ttu-id="88717-116">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="88717-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="88717-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88717-117">-Confirm</span></span>
<span data-ttu-id="88717-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88717-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88717-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88717-119">-WhatIf</span></span>
<span data-ttu-id="88717-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88717-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="88717-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88717-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88717-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88717-122">CommonParameters</span></span>
<span data-ttu-id="88717-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88717-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88717-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88717-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88717-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88717-125">INPUTS</span></span>

### <span data-ttu-id="88717-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="88717-126">None</span></span>
<span data-ttu-id="88717-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="88717-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88717-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88717-128">OUTPUTS</span></span>

## <span data-ttu-id="88717-129">Note</span><span class="sxs-lookup"><span data-stu-id="88717-129">NOTES</span></span>

## <span data-ttu-id="88717-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88717-130">RELATED LINKS</span></span>

[<span data-ttu-id="88717-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="88717-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="88717-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="88717-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
