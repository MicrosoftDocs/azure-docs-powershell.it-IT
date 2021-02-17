---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188518"
---
# <span data-ttu-id="cdfef-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cdfef-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="cdfef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdfef-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfef-103">Imposta i criteri consentiti per le dimensioni delle macchine virtuali di un lab nei laboratori DevTest.</span><span class="sxs-lookup"><span data-stu-id="cdfef-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="cdfef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdfef-104">SYNTAX</span></span>

### <span data-ttu-id="cdfef-105">Abilita (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdfef-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdfef-106">Disabilita</span><span class="sxs-lookup"><span data-stu-id="cdfef-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdfef-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cdfef-107">DESCRIPTION</span></span>
<span data-ttu-id="cdfef-108">Il cmdlet **Set-AzDtlAllowedVMSizesPolicy** imposta il criterio per le dimensioni delle macchine virtuali consentite, che specifica un elenco delle dimensioni di macchine virtuali consentite in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="cdfef-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="cdfef-109">Il cmdlet usa il gruppo di risorse specificato e il nome del lab per impostare il criterio.</span><span class="sxs-lookup"><span data-stu-id="cdfef-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="cdfef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdfef-110">EXAMPLES</span></span>

## <span data-ttu-id="cdfef-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdfef-111">PARAMETERS</span></span>

### <span data-ttu-id="cdfef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfef-112">-DefaultProfile</span></span>
<span data-ttu-id="cdfef-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="cdfef-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdfef-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="cdfef-114">-Disable</span></span>
<span data-ttu-id="cdfef-115">Indica che questo cmdlet disabilita il criterio.</span><span class="sxs-lookup"><span data-stu-id="cdfef-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdfef-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="cdfef-116">-Enable</span></span>
<span data-ttu-id="cdfef-117">Indica che questo cmdlet abilita il criterio.</span><span class="sxs-lookup"><span data-stu-id="cdfef-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdfef-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="cdfef-118">-LabName</span></span>
<span data-ttu-id="cdfef-119">Specifica il nome del lab per cui questo cmdlet imposta i criteri per le dimensioni delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="cdfef-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="cdfef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfef-120">-ResourceGroupName</span></span>
<span data-ttu-id="cdfef-121">Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.</span><span class="sxs-lookup"><span data-stu-id="cdfef-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="cdfef-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="cdfef-122">-VmSizes</span></span>
<span data-ttu-id="cdfef-123">Specifica, come matrice di stringhe, l'elenco delle dimensioni delle macchine virtuali consentite nel lab.</span><span class="sxs-lookup"><span data-stu-id="cdfef-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdfef-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdfef-124">-Confirm</span></span>
<span data-ttu-id="cdfef-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdfef-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdfef-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdfef-126">-WhatIf</span></span>
<span data-ttu-id="cdfef-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdfef-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdfef-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdfef-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdfef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfef-129">CommonParameters</span></span>
<span data-ttu-id="cdfef-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfef-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfef-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfef-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="cdfef-132">INPUTS</span></span>

### <span data-ttu-id="cdfef-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cdfef-133">System.String</span></span>

## <span data-ttu-id="cdfef-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdfef-134">OUTPUTS</span></span>

### <span data-ttu-id="cdfef-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cdfef-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="cdfef-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="cdfef-136">NOTES</span></span>

## <span data-ttu-id="cdfef-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdfef-137">RELATED LINKS</span></span>

[<span data-ttu-id="cdfef-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="cdfef-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


