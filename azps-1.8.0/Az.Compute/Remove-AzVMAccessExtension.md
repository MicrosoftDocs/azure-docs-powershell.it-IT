---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: a409d4f6d09279aed6a22b9212894a1aca9cae1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852001"
---
# <span data-ttu-id="7cf10-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7cf10-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="7cf10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cf10-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf10-103">Rimuove l'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7cf10-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="7cf10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cf10-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cf10-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf10-106">Il cmdlet **Remove-AzVMAccessExtension** rimuove l'estensione della macchina virtuale VMAccess (Virtual Machine Access) da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7cf10-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="7cf10-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cf10-107">EXAMPLES</span></span>

## <span data-ttu-id="7cf10-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cf10-108">PARAMETERS</span></span>

### <span data-ttu-id="7cf10-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf10-109">-DefaultProfile</span></span>
<span data-ttu-id="7cf10-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf10-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf10-111">-Force</span></span>
<span data-ttu-id="7cf10-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7cf10-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cf10-113">-Name</span></span>
<span data-ttu-id="7cf10-114">Specifica il nome dell'estensione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf10-115">-ResourceGroupName</span></span>
<span data-ttu-id="7cf10-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7cf10-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="7cf10-117">-VMName</span></span>
<span data-ttu-id="7cf10-118">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7cf10-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7cf10-119">Questo cmdlet consente di rimuovere VMAccess per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7cf10-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7cf10-120">-Confirm</span></span>
<span data-ttu-id="7cf10-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf10-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf10-122">-WhatIf</span></span>
<span data-ttu-id="7cf10-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cf10-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf10-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cf10-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cf10-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf10-125">CommonParameters</span></span>
<span data-ttu-id="7cf10-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf10-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf10-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf10-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf10-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cf10-128">INPUTS</span></span>

### <span data-ttu-id="7cf10-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7cf10-129">System.String</span></span>

## <span data-ttu-id="7cf10-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cf10-130">OUTPUTS</span></span>

### <span data-ttu-id="7cf10-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7cf10-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7cf10-132">Note</span><span class="sxs-lookup"><span data-stu-id="7cf10-132">NOTES</span></span>

## <span data-ttu-id="7cf10-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cf10-133">RELATED LINKS</span></span>

[<span data-ttu-id="7cf10-134">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7cf10-134">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="7cf10-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7cf10-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="7cf10-136">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7cf10-136">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
