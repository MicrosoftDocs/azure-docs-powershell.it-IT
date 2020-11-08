---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 7031aaa5a0e5655f933beadbb51569aba0adbef1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020345"
---
# <span data-ttu-id="d7de1-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d7de1-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="d7de1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7de1-102">SYNOPSIS</span></span>
<span data-ttu-id="d7de1-103">Imposta i criteri di avvio automatico di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d7de1-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d7de1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7de1-104">SYNTAX</span></span>

### <span data-ttu-id="d7de1-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7de1-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7de1-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="d7de1-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7de1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7de1-107">DESCRIPTION</span></span>
<span data-ttu-id="d7de1-108">Il cmdlet **set-AzDtlAutoStartPolicy** imposta i criteri di avvio automatico di un Lab, che consente di pianificare le macchine virtuali di Lab per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="d7de1-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="d7de1-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="d7de1-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="d7de1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7de1-110">EXAMPLES</span></span>

## <span data-ttu-id="d7de1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7de1-111">PARAMETERS</span></span>

### <span data-ttu-id="d7de1-112">Giorni</span><span class="sxs-lookup"><span data-stu-id="d7de1-112">-Days</span></span>
<span data-ttu-id="d7de1-113">Specifica, in forma di matrice, i giorni della settimana per il momento in cui le macchine virtuali del lab devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="d7de1-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7de1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7de1-114">-DefaultProfile</span></span>
<span data-ttu-id="d7de1-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d7de1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7de1-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="d7de1-116">-Disable</span></span>
<span data-ttu-id="d7de1-117">Indica che questo cmdlet Disabilita i criteri per le macchine virtuali in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="d7de1-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="d7de1-118">-Enable</span><span class="sxs-lookup"><span data-stu-id="d7de1-118">-Enable</span></span>
<span data-ttu-id="d7de1-119">Indica che questo cmdlet Abilita i criteri per le macchine virtuali in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="d7de1-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="d7de1-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="d7de1-120">-LabName</span></span>
<span data-ttu-id="d7de1-121">Specifica il nome del Lab per il quale questo cmdlet imposta i criteri per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="d7de1-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="d7de1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7de1-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7de1-123">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="d7de1-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d7de1-124">-Ora</span><span class="sxs-lookup"><span data-stu-id="d7de1-124">-Time</span></span>
<span data-ttu-id="d7de1-125">Specifica il momento in cui le macchine virtuali del lab devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="d7de1-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7de1-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7de1-126">-Confirm</span></span>
<span data-ttu-id="d7de1-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7de1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7de1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7de1-128">-WhatIf</span></span>
<span data-ttu-id="d7de1-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7de1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7de1-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7de1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7de1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7de1-131">CommonParameters</span></span>
<span data-ttu-id="d7de1-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7de1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7de1-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7de1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7de1-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7de1-134">INPUTS</span></span>

### <span data-ttu-id="d7de1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d7de1-135">System.String</span></span>

## <span data-ttu-id="d7de1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7de1-136">OUTPUTS</span></span>

### <span data-ttu-id="d7de1-137">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="d7de1-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="d7de1-138">Note</span><span class="sxs-lookup"><span data-stu-id="d7de1-138">NOTES</span></span>

## <span data-ttu-id="d7de1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7de1-139">RELATED LINKS</span></span>

[<span data-ttu-id="d7de1-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d7de1-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)


