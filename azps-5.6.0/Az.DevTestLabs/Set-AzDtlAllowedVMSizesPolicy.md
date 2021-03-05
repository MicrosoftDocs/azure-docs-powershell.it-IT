---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 04538710a078c72c7b91725823601a55c21ef846
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994348"
---
# <span data-ttu-id="738aa-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="738aa-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="738aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="738aa-102">SYNOPSIS</span></span>
<span data-ttu-id="738aa-103">Imposta i criteri consentiti per le dimensioni delle macchine virtuali di un lab nei laboratori DevTest.</span><span class="sxs-lookup"><span data-stu-id="738aa-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="738aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="738aa-104">SYNTAX</span></span>

### <span data-ttu-id="738aa-105">Abilita (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="738aa-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="738aa-106">Disabilita</span><span class="sxs-lookup"><span data-stu-id="738aa-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="738aa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="738aa-107">DESCRIPTION</span></span>
<span data-ttu-id="738aa-108">Il cmdlet **Set-AzDtlAllowedVMSizesPolicy** imposta il criterio per le dimensioni delle macchine virtuali consentite, che specifica un elenco delle dimensioni di macchine virtuali consentite in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="738aa-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="738aa-109">Il cmdlet usa il gruppo di risorse specificato e il nome del lab per impostare il criterio.</span><span class="sxs-lookup"><span data-stu-id="738aa-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="738aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="738aa-110">EXAMPLES</span></span>

## <span data-ttu-id="738aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="738aa-111">PARAMETERS</span></span>

### <span data-ttu-id="738aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738aa-112">-DefaultProfile</span></span>
<span data-ttu-id="738aa-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="738aa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="738aa-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="738aa-114">-Disable</span></span>
<span data-ttu-id="738aa-115">Indica che questo cmdlet disabilita il criterio.</span><span class="sxs-lookup"><span data-stu-id="738aa-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="738aa-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="738aa-116">-Enable</span></span>
<span data-ttu-id="738aa-117">Indica che questo cmdlet abilita il criterio.</span><span class="sxs-lookup"><span data-stu-id="738aa-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="738aa-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="738aa-118">-LabName</span></span>
<span data-ttu-id="738aa-119">Specifica il nome del lab per cui questo cmdlet imposta i criteri per le dimensioni delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="738aa-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="738aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="738aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="738aa-121">Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.</span><span class="sxs-lookup"><span data-stu-id="738aa-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="738aa-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="738aa-122">-VmSizes</span></span>
<span data-ttu-id="738aa-123">Specifica, come matrice di stringhe, l'elenco delle dimensioni delle macchine virtuali consentite nel lab.</span><span class="sxs-lookup"><span data-stu-id="738aa-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="738aa-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="738aa-124">-Confirm</span></span>
<span data-ttu-id="738aa-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="738aa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="738aa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="738aa-126">-WhatIf</span></span>
<span data-ttu-id="738aa-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="738aa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="738aa-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="738aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="738aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738aa-129">CommonParameters</span></span>
<span data-ttu-id="738aa-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="738aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738aa-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="738aa-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738aa-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="738aa-132">INPUTS</span></span>

### <span data-ttu-id="738aa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="738aa-133">System.String</span></span>

## <span data-ttu-id="738aa-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="738aa-134">OUTPUTS</span></span>

### <span data-ttu-id="738aa-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="738aa-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="738aa-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="738aa-136">NOTES</span></span>

## <span data-ttu-id="738aa-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="738aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="738aa-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="738aa-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


