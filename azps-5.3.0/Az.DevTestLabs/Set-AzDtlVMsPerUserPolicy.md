---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475337"
---
# <span data-ttu-id="56bfc-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="56bfc-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="56bfc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="56bfc-103">Imposta i criteri per gli utenti delle macchine virtuali di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="56bfc-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="56bfc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56bfc-104">SYNTAX</span></span>

### <span data-ttu-id="56bfc-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56bfc-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56bfc-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="56bfc-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56bfc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56bfc-107">DESCRIPTION</span></span>
<span data-ttu-id="56bfc-108">Il cmdlet **set-AzDtlVMsPerUserPolicy** imposta i criteri per gli utenti delle macchine virtuali di un Lab, che imposta il numero massimo di macchine virtuali consentite per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="56bfc-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="56bfc-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="56bfc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="56bfc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56bfc-110">EXAMPLES</span></span>

## <span data-ttu-id="56bfc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56bfc-111">PARAMETERS</span></span>

### <span data-ttu-id="56bfc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bfc-112">-DefaultProfile</span></span>
<span data-ttu-id="56bfc-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56bfc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56bfc-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="56bfc-114">-Disable</span></span>
<span data-ttu-id="56bfc-115">Indica che questo cmdlet disabilita il criterio per il Lab.</span><span class="sxs-lookup"><span data-stu-id="56bfc-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="56bfc-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="56bfc-116">-Enable</span></span>
<span data-ttu-id="56bfc-117">Indica che questo cmdlet Abilita i criteri per Lab.</span><span class="sxs-lookup"><span data-stu-id="56bfc-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="56bfc-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="56bfc-118">-LabName</span></span>
<span data-ttu-id="56bfc-119">Specifica il nome del Lab per il quale questo cmdlet imposta le macchine virtuali per ogni criterio utente.</span><span class="sxs-lookup"><span data-stu-id="56bfc-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="56bfc-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="56bfc-120">-MaxVMs</span></span>
<span data-ttu-id="56bfc-121">Specifica il numero massimo di macchine virtuali che possono essere create in Lab.</span><span class="sxs-lookup"><span data-stu-id="56bfc-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="56bfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="56bfc-123">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="56bfc-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="56bfc-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56bfc-124">-Confirm</span></span>
<span data-ttu-id="56bfc-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56bfc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56bfc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56bfc-126">-WhatIf</span></span>
<span data-ttu-id="56bfc-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56bfc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56bfc-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56bfc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56bfc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bfc-129">CommonParameters</span></span>
<span data-ttu-id="56bfc-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bfc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bfc-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56bfc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bfc-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56bfc-132">INPUTS</span></span>

### <span data-ttu-id="56bfc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="56bfc-133">System.String</span></span>

## <span data-ttu-id="56bfc-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56bfc-134">OUTPUTS</span></span>

### <span data-ttu-id="56bfc-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="56bfc-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="56bfc-136">Note</span><span class="sxs-lookup"><span data-stu-id="56bfc-136">NOTES</span></span>

## <span data-ttu-id="56bfc-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56bfc-137">RELATED LINKS</span></span>

[<span data-ttu-id="56bfc-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="56bfc-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


