---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 30aad11674cbdef747e444d18bce55ed223e3698
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010574"
---
# <span data-ttu-id="855c6-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="855c6-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="855c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="855c6-102">SYNOPSIS</span></span>
<span data-ttu-id="855c6-103">Imposta le macchine virtuali per i criteri lab di un lab nei laboratori DevTest.</span><span class="sxs-lookup"><span data-stu-id="855c6-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="855c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="855c6-104">SYNTAX</span></span>

### <span data-ttu-id="855c6-105">Abilita (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="855c6-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="855c6-106">Disabilita</span><span class="sxs-lookup"><span data-stu-id="855c6-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="855c6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="855c6-107">DESCRIPTION</span></span>
<span data-ttu-id="855c6-108">Il cmdlet **Set-AzDtlVMsPerLabPolicy** imposta le macchine virtuali per criterio lab di un lab, che imposta il numero totale di macchine virtuali consentite in un lab.</span><span class="sxs-lookup"><span data-stu-id="855c6-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="855c6-109">Il cmdlet usa il gruppo di risorse specificato e il nome del lab per impostare il criterio.</span><span class="sxs-lookup"><span data-stu-id="855c6-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="855c6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="855c6-110">EXAMPLES</span></span>

## <span data-ttu-id="855c6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="855c6-111">PARAMETERS</span></span>

### <span data-ttu-id="855c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="855c6-112">-DefaultProfile</span></span>
<span data-ttu-id="855c6-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="855c6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="855c6-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="855c6-114">-Disable</span></span>
<span data-ttu-id="855c6-115">Indica che questo cmdlet disabilita i criteri del lab.</span><span class="sxs-lookup"><span data-stu-id="855c6-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="855c6-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="855c6-116">-Enable</span></span>
<span data-ttu-id="855c6-117">Indica che questo cmdlet abilita i criteri del lab.</span><span class="sxs-lookup"><span data-stu-id="855c6-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="855c6-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="855c6-118">-LabName</span></span>
<span data-ttu-id="855c6-119">Specifica il nome del lab per cui questo cmdlet imposta le macchine virtuali per ogni criterio lab.</span><span class="sxs-lookup"><span data-stu-id="855c6-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="855c6-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="855c6-120">-MaxVMs</span></span>
<span data-ttu-id="855c6-121">Specifica il numero massimo di macchine virtuali che è possibile creare nel lab.</span><span class="sxs-lookup"><span data-stu-id="855c6-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="855c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="855c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="855c6-123">Specifica il nome del gruppo di risorse a cui appartiene il laboratorio.</span><span class="sxs-lookup"><span data-stu-id="855c6-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="855c6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="855c6-124">-Confirm</span></span>
<span data-ttu-id="855c6-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="855c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="855c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="855c6-126">-WhatIf</span></span>
<span data-ttu-id="855c6-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="855c6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="855c6-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="855c6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="855c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="855c6-129">CommonParameters</span></span>
<span data-ttu-id="855c6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="855c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="855c6-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="855c6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="855c6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="855c6-132">INPUTS</span></span>

### <span data-ttu-id="855c6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="855c6-133">System.String</span></span>

## <span data-ttu-id="855c6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="855c6-134">OUTPUTS</span></span>

### <span data-ttu-id="855c6-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="855c6-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="855c6-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="855c6-136">NOTES</span></span>

## <span data-ttu-id="855c6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="855c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="855c6-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="855c6-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


