---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: e1b400f2fe3ff973c586fbde9f4003732ad8c6cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863518"
---
# <span data-ttu-id="d0aad-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d0aad-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="d0aad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0aad-102">SYNOPSIS</span></span>
<span data-ttu-id="d0aad-103">Rimuove un'estensione da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d0aad-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="d0aad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0aad-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0aad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0aad-105">DESCRIPTION</span></span>
<span data-ttu-id="d0aad-106">Il cmdlet **Remove-AzVMExtension** consente di rimuovere un'estensione dalle estensioni della macchina virtuale di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d0aad-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="d0aad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0aad-107">EXAMPLES</span></span>

### <span data-ttu-id="d0aad-108">Esempio 1: rimuovere un'estensione da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="d0aad-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="d0aad-109">Questo comando rimuove l'estensione denominata ContosoTest dalla macchina virtuale denominata VirtualMachine22 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d0aad-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="d0aad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0aad-110">PARAMETERS</span></span>

### <span data-ttu-id="d0aad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0aad-111">-DefaultProfile</span></span>
<span data-ttu-id="d0aad-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0aad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0aad-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d0aad-113">-Force</span></span>
<span data-ttu-id="d0aad-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d0aad-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0aad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0aad-115">-Name</span></span>
<span data-ttu-id="d0aad-116">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0aad-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0aad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0aad-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0aad-118">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d0aad-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d0aad-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="d0aad-119">-VMName</span></span>
<span data-ttu-id="d0aad-120">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione.</span><span class="sxs-lookup"><span data-stu-id="d0aad-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="d0aad-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0aad-121">-Confirm</span></span>
<span data-ttu-id="d0aad-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0aad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0aad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0aad-123">-WhatIf</span></span>
<span data-ttu-id="d0aad-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0aad-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d0aad-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0aad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0aad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0aad-126">CommonParameters</span></span>
<span data-ttu-id="d0aad-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0aad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0aad-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0aad-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0aad-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0aad-129">INPUTS</span></span>

### <span data-ttu-id="d0aad-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0aad-130">None</span></span>
<span data-ttu-id="d0aad-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d0aad-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0aad-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0aad-132">OUTPUTS</span></span>

### <span data-ttu-id="d0aad-133">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d0aad-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d0aad-134">Note</span><span class="sxs-lookup"><span data-stu-id="d0aad-134">NOTES</span></span>

## <span data-ttu-id="d0aad-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0aad-135">RELATED LINKS</span></span>

[<span data-ttu-id="d0aad-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d0aad-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="d0aad-137">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d0aad-137">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


