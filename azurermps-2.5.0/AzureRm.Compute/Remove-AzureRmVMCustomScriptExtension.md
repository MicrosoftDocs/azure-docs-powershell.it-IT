---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866710"
---
# <span data-ttu-id="c5e87-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c5e87-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="c5e87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5e87-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e87-103">Rimuove un'estensione di script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5e87-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5e87-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5e87-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e87-106">Il cmdlet **Remove-AzureRmVMCustomScriptExtension** rimuove un'estensione di una macchina virtuale script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5e87-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="c5e87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5e87-107">EXAMPLES</span></span>

## <span data-ttu-id="c5e87-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5e87-108">PARAMETERS</span></span>

### <span data-ttu-id="c5e87-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e87-109">-DefaultProfile</span></span>
<span data-ttu-id="c5e87-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e87-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5e87-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c5e87-111">-Force</span></span>
<span data-ttu-id="c5e87-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c5e87-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5e87-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5e87-113">-Name</span></span>
<span data-ttu-id="c5e87-114">Specifica il nome dell'estensione di script personalizzata rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e87-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c5e87-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e87-115">-ResourceGroupName</span></span>
<span data-ttu-id="c5e87-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5e87-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c5e87-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="c5e87-117">-VMName</span></span>
<span data-ttu-id="c5e87-118">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione di script personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c5e87-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="c5e87-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5e87-119">-Confirm</span></span>
<span data-ttu-id="c5e87-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e87-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e87-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e87-121">-WhatIf</span></span>
<span data-ttu-id="c5e87-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5e87-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c5e87-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5e87-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e87-124">CommonParameters</span></span>
<span data-ttu-id="c5e87-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e87-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e87-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5e87-127">INPUTS</span></span>

### <span data-ttu-id="c5e87-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5e87-128">None</span></span>
<span data-ttu-id="c5e87-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c5e87-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5e87-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5e87-130">OUTPUTS</span></span>

### <span data-ttu-id="c5e87-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c5e87-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c5e87-132">Note</span><span class="sxs-lookup"><span data-stu-id="c5e87-132">NOTES</span></span>

## <span data-ttu-id="c5e87-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5e87-133">RELATED LINKS</span></span>

[<span data-ttu-id="c5e87-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c5e87-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="c5e87-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c5e87-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
