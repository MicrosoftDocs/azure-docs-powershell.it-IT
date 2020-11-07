---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: a1efa9159bbe318a1de0360a3f70f197660db535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687197"
---
# <span data-ttu-id="fa4e8-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="fa4e8-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="fa4e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4e8-103">Imposta i criteri di avvio automatico di un Lab in DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa4e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa4e8-104">SYNTAX</span></span>

### <span data-ttu-id="fa4e8-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa4e8-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa4e8-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="fa4e8-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa4e8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa4e8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa4e8-108">Il cmdlet **set-AzureRmDtlAutoStartPolicy** imposta i criteri di avvio automatico di un Lab, che consente di pianificare le macchine virtuali di Lab per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="fa4e8-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="fa4e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa4e8-110">EXAMPLES</span></span>

## <span data-ttu-id="fa4e8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa4e8-111">PARAMETERS</span></span>

### <span data-ttu-id="fa4e8-112">Giorni</span><span class="sxs-lookup"><span data-stu-id="fa4e8-112">-Days</span></span>
<span data-ttu-id="fa4e8-113">Specifica, in forma di matrice, i giorni della settimana per il momento in cui le macchine virtuali del lab devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="fa4e8-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="fa4e8-114">-Disable</span></span>
<span data-ttu-id="fa4e8-115">Indica che questo cmdlet Disabilita i criteri per le macchine virtuali in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-115">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="fa4e8-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="fa4e8-116">-Enable</span></span>
<span data-ttu-id="fa4e8-117">Indica che questo cmdlet Abilita i criteri per le macchine virtuali in laboratorio.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-117">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="fa4e8-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="fa4e8-118">-LabName</span></span>
<span data-ttu-id="fa4e8-119">Specifica il nome del Lab per il quale questo cmdlet imposta i criteri per l'avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-119">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="fa4e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa4e8-121">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="fa4e8-122">-Ora</span><span class="sxs-lookup"><span data-stu-id="fa4e8-122">-Time</span></span>
<span data-ttu-id="fa4e8-123">Specifica il momento in cui le macchine virtuali del lab devono essere avviate.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-123">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="fa4e8-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa4e8-124">-Confirm</span></span>
<span data-ttu-id="fa4e8-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4e8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4e8-126">-WhatIf</span></span>
<span data-ttu-id="fa4e8-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa4e8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4e8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4e8-129">-DefaultProfile</span></span>
<span data-ttu-id="fa4e8-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4e8-131">CommonParameters</span></span>
<span data-ttu-id="fa4e8-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4e8-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa4e8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4e8-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa4e8-134">INPUTS</span></span>

## <span data-ttu-id="fa4e8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa4e8-135">OUTPUTS</span></span>

### <span data-ttu-id="fa4e8-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="fa4e8-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="fa4e8-137">Questo cmdlet restituisce la programmazione che specifica quando deve essere avviata la macchina virtuale del Lab.</span><span class="sxs-lookup"><span data-stu-id="fa4e8-137">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="fa4e8-138">Note</span><span class="sxs-lookup"><span data-stu-id="fa4e8-138">NOTES</span></span>

## <span data-ttu-id="fa4e8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa4e8-139">RELATED LINKS</span></span>

[<span data-ttu-id="fa4e8-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="fa4e8-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


