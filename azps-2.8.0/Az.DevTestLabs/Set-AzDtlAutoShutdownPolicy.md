---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4b15f20f9399df277fc2d2a76f7e51c2a7d57d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674561"
---
# <span data-ttu-id="c4242-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c4242-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="c4242-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4242-102">SYNOPSIS</span></span>
<span data-ttu-id="c4242-103">Imposta il criterio di arresto automatico di un Lab DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="c4242-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="c4242-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4242-104">SYNTAX</span></span>

### <span data-ttu-id="c4242-105">Enable (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4242-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4242-106">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="c4242-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4242-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4242-107">DESCRIPTION</span></span>
<span data-ttu-id="c4242-108">Il cmdlet **set-AzDtlAutoShutdownPolicy** imposta i criteri di arresto automatico di un Lab, che arresta automaticamente tutte le macchine virtuali nel Lab in un determinato momento della giornata.</span><span class="sxs-lookup"><span data-stu-id="c4242-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="c4242-109">Il cmdlet usa il gruppo di risorse specificato e il nome del Lab per impostare i criteri.</span><span class="sxs-lookup"><span data-stu-id="c4242-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="c4242-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4242-110">EXAMPLES</span></span>

## <span data-ttu-id="c4242-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4242-111">PARAMETERS</span></span>

### <span data-ttu-id="c4242-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4242-112">-DefaultProfile</span></span>
<span data-ttu-id="c4242-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c4242-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4242-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="c4242-114">-Disable</span></span>
<span data-ttu-id="c4242-115">Indica che il cmdlet disabilita il criterio in Lab.</span><span class="sxs-lookup"><span data-stu-id="c4242-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="c4242-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="c4242-116">-Enable</span></span>
<span data-ttu-id="c4242-117">Indica che il cmdlet Abilita i criteri in Lab.</span><span class="sxs-lookup"><span data-stu-id="c4242-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="c4242-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="c4242-118">-LabName</span></span>
<span data-ttu-id="c4242-119">Specifica il nome del Lab per il quale questo cmdlet imposta il criterio di arresto automatico.</span><span class="sxs-lookup"><span data-stu-id="c4242-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="c4242-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4242-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4242-121">Specifica il nome del gruppo di risorse a cui appartiene il Lab.</span><span class="sxs-lookup"><span data-stu-id="c4242-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c4242-122">-Ora</span><span class="sxs-lookup"><span data-stu-id="c4242-122">-Time</span></span>
<span data-ttu-id="c4242-123">Specifica il tempo, come oggetto **DateTime** , per il momento in cui le macchine virtuali in laboratorio devono essere arrestate.</span><span class="sxs-lookup"><span data-stu-id="c4242-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="c4242-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4242-124">-Confirm</span></span>
<span data-ttu-id="c4242-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4242-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4242-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4242-126">-WhatIf</span></span>
<span data-ttu-id="c4242-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4242-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4242-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4242-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4242-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4242-129">CommonParameters</span></span>
<span data-ttu-id="c4242-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4242-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4242-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4242-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4242-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4242-132">INPUTS</span></span>

### <span data-ttu-id="c4242-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c4242-133">System.String</span></span>

## <span data-ttu-id="c4242-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4242-134">OUTPUTS</span></span>

### <span data-ttu-id="c4242-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="c4242-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="c4242-136">Note</span><span class="sxs-lookup"><span data-stu-id="c4242-136">NOTES</span></span>

## <span data-ttu-id="c4242-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4242-137">RELATED LINKS</span></span>

[<span data-ttu-id="c4242-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c4242-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


