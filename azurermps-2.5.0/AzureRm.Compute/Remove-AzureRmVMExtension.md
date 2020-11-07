---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: 835413728b22dd8bbb80d472eed71e0f4185db89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866555"
---
# <span data-ttu-id="f4f6e-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f4f6e-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="f4f6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f6e-103">Rimuove un'estensione da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4f6e-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4f6e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f6e-106">Il cmdlet **Remove-AzureRmVMExtension** consente di rimuovere un'estensione dalle estensioni della macchina virtuale di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="f4f6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4f6e-107">EXAMPLES</span></span>

### <span data-ttu-id="f4f6e-108">Esempio 1: rimuovere un'estensione da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f4f6e-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="f4f6e-109">Questo comando rimuove l'estensione denominata ContosoTest dalla macchina virtuale denominata VirtualMachine22 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="f4f6e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4f6e-110">PARAMETERS</span></span>

### <span data-ttu-id="f4f6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f6e-111">-DefaultProfile</span></span>
<span data-ttu-id="f4f6e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4f6e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f4f6e-113">-Force</span></span>
<span data-ttu-id="f4f6e-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4f6e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4f6e-115">-Name</span></span>
<span data-ttu-id="f4f6e-116">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f4f6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4f6e-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f4f6e-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="f4f6e-119">-VMName</span></span>
<span data-ttu-id="f4f6e-120">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="f4f6e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4f6e-121">-Confirm</span></span>
<span data-ttu-id="f4f6e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f6e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f6e-123">-WhatIf</span></span>
<span data-ttu-id="f4f6e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f4f6e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f6e-126">CommonParameters</span></span>
<span data-ttu-id="f4f6e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f6e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f6e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f6e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4f6e-129">INPUTS</span></span>

### <span data-ttu-id="f4f6e-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4f6e-130">None</span></span>
<span data-ttu-id="f4f6e-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f4f6e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4f6e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4f6e-132">OUTPUTS</span></span>

### <span data-ttu-id="f4f6e-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f4f6e-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f4f6e-134">Note</span><span class="sxs-lookup"><span data-stu-id="f4f6e-134">NOTES</span></span>

## <span data-ttu-id="f4f6e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4f6e-135">RELATED LINKS</span></span>

[<span data-ttu-id="f4f6e-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f4f6e-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="f4f6e-137">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f4f6e-137">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


