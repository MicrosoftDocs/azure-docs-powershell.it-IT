---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191583"
---
# <span data-ttu-id="83b43-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="83b43-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="83b43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b43-102">SYNOPSIS</span></span>
<span data-ttu-id="83b43-103">Imposta i criteri di dimensioni della macchina virtuale consentiti di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="83b43-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="83b43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b43-104">SYNTAX</span></span>

### <span data-ttu-id="83b43-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83b43-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83b43-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="83b43-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83b43-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b43-107">DESCRIPTION</span></span>
<span data-ttu-id="83b43-108">Il cmdlet **set-AzDtlAllowedVMSizesPolicy** imposta i criteri per le dimensioni della macchina virtuale consentiti, che specifica un elenco delle dimensioni della macchina virtuale consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="83b43-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="83b43-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="83b43-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="83b43-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b43-110">EXAMPLES</span></span>

## <span data-ttu-id="83b43-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b43-111">PARAMETERS</span></span>

### <span data-ttu-id="83b43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b43-112">-DefaultProfile</span></span>
<span data-ttu-id="83b43-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="83b43-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83b43-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="83b43-114">-Disable</span></span>
<span data-ttu-id="83b43-115">Indica che questo cmdlet disabilita il criterio.</span><span class="sxs-lookup"><span data-stu-id="83b43-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="83b43-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="83b43-116">-Enable</span></span>
<span data-ttu-id="83b43-117">Indica che questo cmdlet Abilita i criteri.</span><span class="sxs-lookup"><span data-stu-id="83b43-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="83b43-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="83b43-118">-LabName</span></span>
<span data-ttu-id="83b43-119">Specifica il nome del Lab per il quale questo cmdlet imposta i criteri di dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="83b43-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="83b43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b43-120">-ResourceGroupName</span></span>
<span data-ttu-id="83b43-121">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="83b43-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="83b43-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="83b43-122">-VmSizes</span></span>
<span data-ttu-id="83b43-123">Specifica come matrice di stringhe l'elenco delle dimensioni della macchina virtuale consentite in Lab.</span><span class="sxs-lookup"><span data-stu-id="83b43-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="83b43-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83b43-124">-Confirm</span></span>
<span data-ttu-id="83b43-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b43-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b43-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b43-126">-WhatIf</span></span>
<span data-ttu-id="83b43-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b43-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b43-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b43-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b43-129">CommonParameters</span></span>
<span data-ttu-id="83b43-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b43-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b43-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b43-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b43-132">INPUTS</span></span>

### <span data-ttu-id="83b43-133">System. String</span><span class="sxs-lookup"><span data-stu-id="83b43-133">System.String</span></span>

## <span data-ttu-id="83b43-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b43-134">OUTPUTS</span></span>

### <span data-ttu-id="83b43-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="83b43-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="83b43-136">Note</span><span class="sxs-lookup"><span data-stu-id="83b43-136">NOTES</span></span>

## <span data-ttu-id="83b43-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b43-137">RELATED LINKS</span></span>

[<span data-ttu-id="83b43-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="83b43-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)

