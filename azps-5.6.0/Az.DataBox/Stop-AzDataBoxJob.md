---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 60fdd8223f073ffd6de76db659e6bd989f48fada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998673"
---
# <span data-ttu-id="e5057-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="e5057-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="e5057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5057-102">SYNOPSIS</span></span>
<span data-ttu-id="e5057-103">Annulla un processo della casella dati in corso se il processo è in stato di annullamento.</span><span class="sxs-lookup"><span data-stu-id="e5057-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="e5057-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5057-104">SYNTAX</span></span>

### <span data-ttu-id="e5057-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5057-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5057-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5057-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5057-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5057-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5057-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5057-108">DESCRIPTION</span></span>
<span data-ttu-id="e5057-109">Il cmdlet **Stop-AzDataBoxJob** viene usato per annullare un processo della casella di dati.</span><span class="sxs-lookup"><span data-stu-id="e5057-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="e5057-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5057-110">EXAMPLES</span></span>

### <span data-ttu-id="e5057-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5057-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="e5057-112">Annulla il processo specificato nella casella dati</span><span class="sxs-lookup"><span data-stu-id="e5057-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="e5057-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e5057-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="e5057-114">Annulla il processo specificato in modo forzato senza conferma</span><span class="sxs-lookup"><span data-stu-id="e5057-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="e5057-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e5057-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="e5057-116">Annulla il processo specificato nella casella dati</span><span class="sxs-lookup"><span data-stu-id="e5057-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="e5057-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5057-117">PARAMETERS</span></span>

### <span data-ttu-id="e5057-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5057-118">-DefaultProfile</span></span>
<span data-ttu-id="e5057-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5057-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5057-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e5057-120">-Force</span></span>
<span data-ttu-id="e5057-121">Forzare l'arresto senza conferma</span><span class="sxs-lookup"><span data-stu-id="e5057-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="e5057-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5057-122">-InputObject</span></span>
<span data-ttu-id="e5057-123">InputObject di tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="e5057-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e5057-124">-Name</span></span>
<span data-ttu-id="e5057-125">Nome processo casella di dati</span><span class="sxs-lookup"><span data-stu-id="e5057-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5057-126">-PassThru</span></span>
<span data-ttu-id="e5057-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="e5057-127">PassThru</span></span>

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

### <span data-ttu-id="e5057-128">-Motivo</span><span class="sxs-lookup"><span data-stu-id="e5057-128">-Reason</span></span>
<span data-ttu-id="e5057-129">Motivo dell'annullamento</span><span class="sxs-lookup"><span data-stu-id="e5057-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5057-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5057-131">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="e5057-131">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5057-132">-ResourceId</span></span>
<span data-ttu-id="e5057-133">ID risorsa casella dati</span><span class="sxs-lookup"><span data-stu-id="e5057-133">Databox Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5057-134">-Confirm</span></span>
<span data-ttu-id="e5057-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5057-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5057-136">-WhatIf</span></span>
<span data-ttu-id="e5057-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5057-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5057-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5057-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5057-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5057-139">CommonParameters</span></span>
<span data-ttu-id="e5057-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5057-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5057-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5057-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5057-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5057-142">INPUTS</span></span>

### <span data-ttu-id="e5057-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e5057-143">System.String</span></span>

## <span data-ttu-id="e5057-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5057-144">OUTPUTS</span></span>

### <span data-ttu-id="e5057-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5057-145">System.Void</span></span>

## <span data-ttu-id="e5057-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5057-146">NOTES</span></span>

## <span data-ttu-id="e5057-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5057-147">RELATED LINKS</span></span>
