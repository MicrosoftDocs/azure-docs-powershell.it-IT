---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177543"
---
# <span data-ttu-id="70aa9-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="70aa9-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="70aa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="70aa9-103">Rimuove un gestore delle estensioni DSC da una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70aa9-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="70aa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70aa9-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70aa9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70aa9-105">DESCRIPTION</span></span>
<span data-ttu-id="70aa9-106">Il cmdlet **Remove-AzVMDscExtension** rimuove un gestore delle estensioni DSC (Desired State Configuration) da una macchina virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70aa9-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="70aa9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70aa9-107">EXAMPLES</span></span>

### <span data-ttu-id="70aa9-108">Esempio 1: Rimuovere un'estensione DSC</span><span class="sxs-lookup"><span data-stu-id="70aa9-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="70aa9-109">Questo comando rimuove l'estensione DSC nella macchina virtuale denominata VM07.</span><span class="sxs-lookup"><span data-stu-id="70aa9-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="70aa9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70aa9-110">PARAMETERS</span></span>

### <span data-ttu-id="70aa9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70aa9-111">-DefaultProfile</span></span>
<span data-ttu-id="70aa9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70aa9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70aa9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="70aa9-113">-Name</span></span>
<span data-ttu-id="70aa9-114">Specifica il nome dell'estensione DSC rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70aa9-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="70aa9-115">Il cmdlet Set-AzVMDscExtension imposta questo nome su Microsoft.Powershell.DSC, ovvero il valore predefinito usato da **Remove-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="70aa9-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aa9-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="70aa9-116">-NoWait</span></span>
<span data-ttu-id="70aa9-117">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="70aa9-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="70aa9-118">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="70aa9-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="70aa9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70aa9-119">-ResourceGroupName</span></span>
<span data-ttu-id="70aa9-120">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="70aa9-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="70aa9-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="70aa9-121">-VMName</span></span>
<span data-ttu-id="70aa9-122">Specifica il nome di una macchina virtuale da cui questo cmdlet rimuove l'estensione DSC.</span><span class="sxs-lookup"><span data-stu-id="70aa9-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aa9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70aa9-123">-Confirm</span></span>
<span data-ttu-id="70aa9-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70aa9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70aa9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70aa9-125">-WhatIf</span></span>
<span data-ttu-id="70aa9-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70aa9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70aa9-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70aa9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70aa9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70aa9-128">CommonParameters</span></span>
<span data-ttu-id="70aa9-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70aa9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70aa9-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70aa9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70aa9-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="70aa9-131">INPUTS</span></span>

### <span data-ttu-id="70aa9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="70aa9-132">System.String</span></span>

## <span data-ttu-id="70aa9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70aa9-133">OUTPUTS</span></span>

### <span data-ttu-id="70aa9-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="70aa9-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="70aa9-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="70aa9-135">NOTES</span></span>

## <span data-ttu-id="70aa9-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70aa9-136">RELATED LINKS</span></span>

[<span data-ttu-id="70aa9-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="70aa9-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="70aa9-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="70aa9-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


