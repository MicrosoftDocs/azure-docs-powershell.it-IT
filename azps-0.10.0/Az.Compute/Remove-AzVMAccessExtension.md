---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863554"
---
# <span data-ttu-id="3eabe-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3eabe-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="3eabe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eabe-102">SYNOPSIS</span></span>
<span data-ttu-id="3eabe-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3eabe-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="3eabe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eabe-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eabe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eabe-105">DESCRIPTION</span></span>
<span data-ttu-id="3eabe-106">Il cmdlet **Remove-AzVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3eabe-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="3eabe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eabe-107">EXAMPLES</span></span>

## <span data-ttu-id="3eabe-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eabe-108">PARAMETERS</span></span>

### <span data-ttu-id="3eabe-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eabe-109">-DefaultProfile</span></span>
<span data-ttu-id="3eabe-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3eabe-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eabe-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3eabe-111">-Force</span></span>
<span data-ttu-id="3eabe-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3eabe-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3eabe-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eabe-113">-Name</span></span>
<span data-ttu-id="3eabe-114">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eabe-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3eabe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eabe-115">-ResourceGroupName</span></span>
<span data-ttu-id="3eabe-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3eabe-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3eabe-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="3eabe-117">-VMName</span></span>
<span data-ttu-id="3eabe-118">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3eabe-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3eabe-119">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3eabe-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3eabe-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3eabe-120">-Confirm</span></span>
<span data-ttu-id="3eabe-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eabe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eabe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eabe-122">-WhatIf</span></span>
<span data-ttu-id="3eabe-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eabe-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3eabe-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eabe-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eabe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eabe-125">CommonParameters</span></span>
<span data-ttu-id="3eabe-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eabe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eabe-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eabe-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eabe-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eabe-128">INPUTS</span></span>

### <span data-ttu-id="3eabe-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3eabe-129">None</span></span>
<span data-ttu-id="3eabe-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3eabe-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3eabe-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eabe-131">OUTPUTS</span></span>

### <span data-ttu-id="3eabe-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3eabe-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3eabe-133">Note</span><span class="sxs-lookup"><span data-stu-id="3eabe-133">NOTES</span></span>

## <span data-ttu-id="3eabe-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eabe-134">RELATED LINKS</span></span>

[<span data-ttu-id="3eabe-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3eabe-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="3eabe-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3eabe-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="3eabe-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="3eabe-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
