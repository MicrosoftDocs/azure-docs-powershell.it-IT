---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863541"
---
# <span data-ttu-id="af714-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="af714-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="af714-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af714-102">SYNOPSIS</span></span>
<span data-ttu-id="af714-103">Rimuove un'estensione di script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="af714-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="af714-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af714-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af714-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af714-105">DESCRIPTION</span></span>
<span data-ttu-id="af714-106">Il cmdlet **Remove-AzVMCustomScriptExtension** rimuove un'estensione di una macchina virtuale script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="af714-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="af714-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af714-107">EXAMPLES</span></span>

## <span data-ttu-id="af714-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af714-108">PARAMETERS</span></span>

### <span data-ttu-id="af714-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af714-109">-DefaultProfile</span></span>
<span data-ttu-id="af714-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af714-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af714-111">-Force</span><span class="sxs-lookup"><span data-stu-id="af714-111">-Force</span></span>
<span data-ttu-id="af714-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="af714-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af714-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="af714-113">-Name</span></span>
<span data-ttu-id="af714-114">Specifica il nome dell'estensione di script personalizzata rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af714-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="af714-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af714-115">-ResourceGroupName</span></span>
<span data-ttu-id="af714-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="af714-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="af714-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="af714-117">-VMName</span></span>
<span data-ttu-id="af714-118">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="af714-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="af714-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af714-119">-Confirm</span></span>
<span data-ttu-id="af714-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af714-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af714-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af714-121">-WhatIf</span></span>
<span data-ttu-id="af714-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af714-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="af714-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af714-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af714-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af714-124">CommonParameters</span></span>
<span data-ttu-id="af714-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af714-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af714-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af714-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af714-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af714-127">INPUTS</span></span>

### <span data-ttu-id="af714-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="af714-128">None</span></span>
<span data-ttu-id="af714-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="af714-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af714-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af714-130">OUTPUTS</span></span>

### <span data-ttu-id="af714-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af714-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="af714-132">Note</span><span class="sxs-lookup"><span data-stu-id="af714-132">NOTES</span></span>

## <span data-ttu-id="af714-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af714-133">RELATED LINKS</span></span>

[<span data-ttu-id="af714-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="af714-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="af714-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="af714-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
