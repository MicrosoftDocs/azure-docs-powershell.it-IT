---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193498"
---
# <span data-ttu-id="2ffcc-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="2ffcc-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="2ffcc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ffcc-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffcc-103">Imposta i criteri delle macchine virtuali per Lab di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="2ffcc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ffcc-104">SYNTAX</span></span>

### <span data-ttu-id="2ffcc-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ffcc-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ffcc-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="2ffcc-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ffcc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ffcc-107">DESCRIPTION</span></span>
<span data-ttu-id="2ffcc-108">Il cmdlet **set-AzDtlVMsPerLabPolicy** imposta le macchine virtuali per i criteri Lab di un Lab, che imposta il numero totale di macchine virtuali consentite in un Lab.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="2ffcc-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="2ffcc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ffcc-110">EXAMPLES</span></span>

## <span data-ttu-id="2ffcc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ffcc-111">PARAMETERS</span></span>

### <span data-ttu-id="2ffcc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffcc-112">-DefaultProfile</span></span>
<span data-ttu-id="2ffcc-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ffcc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ffcc-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="2ffcc-114">-Disable</span></span>
<span data-ttu-id="2ffcc-115">Indica che questo cmdlet Disabilita i criteri del Lab.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="2ffcc-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="2ffcc-116">-Enable</span></span>
<span data-ttu-id="2ffcc-117">Indica che questo cmdlet Abilita i criteri del Lab.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="2ffcc-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="2ffcc-118">-LabName</span></span>
<span data-ttu-id="2ffcc-119">Specifica il nome del Lab per il quale questo cmdlet imposta le macchine virtuali per ogni criterio Lab.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="2ffcc-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="2ffcc-120">-MaxVMs</span></span>
<span data-ttu-id="2ffcc-121">Specifica il numero massimo di macchine virtuali che possono essere create in Lab.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="2ffcc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ffcc-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ffcc-123">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2ffcc-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ffcc-124">-Confirm</span></span>
<span data-ttu-id="2ffcc-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ffcc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ffcc-126">-WhatIf</span></span>
<span data-ttu-id="2ffcc-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ffcc-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ffcc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffcc-129">CommonParameters</span></span>
<span data-ttu-id="2ffcc-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffcc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffcc-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ffcc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffcc-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ffcc-132">INPUTS</span></span>

### <span data-ttu-id="2ffcc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2ffcc-133">System.String</span></span>

## <span data-ttu-id="2ffcc-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ffcc-134">OUTPUTS</span></span>

### <span data-ttu-id="2ffcc-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="2ffcc-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="2ffcc-136">Note</span><span class="sxs-lookup"><span data-stu-id="2ffcc-136">NOTES</span></span>

## <span data-ttu-id="2ffcc-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ffcc-137">RELATED LINKS</span></span>

[<span data-ttu-id="2ffcc-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="2ffcc-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)

