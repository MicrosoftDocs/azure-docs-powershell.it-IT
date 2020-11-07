---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866714"
---
# <span data-ttu-id="865ab-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="865ab-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="865ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="865ab-102">SYNOPSIS</span></span>
<span data-ttu-id="865ab-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="865ab-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="865ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="865ab-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="865ab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="865ab-105">DESCRIPTION</span></span>
<span data-ttu-id="865ab-106">Il cmdlet **Remove-AzureRmVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="865ab-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="865ab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="865ab-107">EXAMPLES</span></span>

## <span data-ttu-id="865ab-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="865ab-108">PARAMETERS</span></span>

### <span data-ttu-id="865ab-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865ab-109">-DefaultProfile</span></span>
<span data-ttu-id="865ab-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="865ab-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865ab-111">-Force</span><span class="sxs-lookup"><span data-stu-id="865ab-111">-Force</span></span>
<span data-ttu-id="865ab-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="865ab-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="865ab-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="865ab-113">-Name</span></span>
<span data-ttu-id="865ab-114">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865ab-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="865ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="865ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="865ab-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="865ab-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="865ab-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="865ab-117">-VMName</span></span>
<span data-ttu-id="865ab-118">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="865ab-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="865ab-119">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="865ab-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="865ab-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="865ab-120">-Confirm</span></span>
<span data-ttu-id="865ab-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="865ab-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="865ab-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="865ab-122">-WhatIf</span></span>
<span data-ttu-id="865ab-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="865ab-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="865ab-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="865ab-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="865ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865ab-125">CommonParameters</span></span>
<span data-ttu-id="865ab-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="865ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865ab-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="865ab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865ab-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="865ab-128">INPUTS</span></span>

### <span data-ttu-id="865ab-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="865ab-129">None</span></span>
<span data-ttu-id="865ab-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="865ab-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="865ab-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="865ab-131">OUTPUTS</span></span>

### <span data-ttu-id="865ab-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="865ab-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="865ab-133">Note</span><span class="sxs-lookup"><span data-stu-id="865ab-133">NOTES</span></span>

## <span data-ttu-id="865ab-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="865ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="865ab-135">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="865ab-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="865ab-136">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="865ab-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="865ab-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="865ab-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
