---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487743"
---
# <span data-ttu-id="47d5e-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="47d5e-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="47d5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="47d5e-103">Annulla un processo di databox in corso se il processo è in stato cancellable.</span><span class="sxs-lookup"><span data-stu-id="47d5e-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="47d5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47d5e-104">SYNTAX</span></span>

### <span data-ttu-id="47d5e-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47d5e-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d5e-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d5e-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47d5e-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47d5e-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47d5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47d5e-108">DESCRIPTION</span></span>
<span data-ttu-id="47d5e-109">Il cmdlet **Stop-AzDataBoxJob** viene usato per annullare un processo di databox.</span><span class="sxs-lookup"><span data-stu-id="47d5e-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="47d5e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47d5e-110">EXAMPLES</span></span>

### <span data-ttu-id="47d5e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47d5e-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="47d5e-112">Annulla il processo di databox specificato</span><span class="sxs-lookup"><span data-stu-id="47d5e-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="47d5e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="47d5e-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="47d5e-114">Annulla il processo di databox specificato con forza senza conferma</span><span class="sxs-lookup"><span data-stu-id="47d5e-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="47d5e-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="47d5e-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="47d5e-116">Annulla il processo di databox specificato</span><span class="sxs-lookup"><span data-stu-id="47d5e-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="47d5e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47d5e-117">PARAMETERS</span></span>

### <span data-ttu-id="47d5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d5e-118">-DefaultProfile</span></span>
<span data-ttu-id="47d5e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47d5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47d5e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="47d5e-120">-Force</span></span>
<span data-ttu-id="47d5e-121">Arresto forzata senza conferma</span><span class="sxs-lookup"><span data-stu-id="47d5e-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="47d5e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47d5e-122">-InputObject</span></span>
<span data-ttu-id="47d5e-123">InputObject di tipo PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="47d5e-123">InputObject of type PSDataBoxJob</span></span>

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

### <span data-ttu-id="47d5e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="47d5e-124">-Name</span></span>
<span data-ttu-id="47d5e-125">Nome processo databox</span><span class="sxs-lookup"><span data-stu-id="47d5e-125">Databox Job Name</span></span>

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

### <span data-ttu-id="47d5e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47d5e-126">-PassThru</span></span>
<span data-ttu-id="47d5e-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="47d5e-127">PassThru</span></span>

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

### <span data-ttu-id="47d5e-128">-Motivo</span><span class="sxs-lookup"><span data-stu-id="47d5e-128">-Reason</span></span>
<span data-ttu-id="47d5e-129">Motivo dell'annullamento</span><span class="sxs-lookup"><span data-stu-id="47d5e-129">Reason For Cancellation</span></span>

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

### <span data-ttu-id="47d5e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d5e-130">-ResourceGroupName</span></span>
<span data-ttu-id="47d5e-131">Nome gruppo risorse processo databox</span><span class="sxs-lookup"><span data-stu-id="47d5e-131">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="47d5e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47d5e-132">-ResourceId</span></span>
<span data-ttu-id="47d5e-133">ID risorsa databox</span><span class="sxs-lookup"><span data-stu-id="47d5e-133">Databox Resource Id</span></span>

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

### <span data-ttu-id="47d5e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47d5e-134">-Confirm</span></span>
<span data-ttu-id="47d5e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47d5e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d5e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d5e-136">-WhatIf</span></span>
<span data-ttu-id="47d5e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47d5e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47d5e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47d5e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d5e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d5e-139">CommonParameters</span></span>
<span data-ttu-id="47d5e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d5e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d5e-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47d5e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d5e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47d5e-142">INPUTS</span></span>

### <span data-ttu-id="47d5e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="47d5e-143">System.String</span></span>

## <span data-ttu-id="47d5e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47d5e-144">OUTPUTS</span></span>

### <span data-ttu-id="47d5e-145">System. void</span><span class="sxs-lookup"><span data-stu-id="47d5e-145">System.Void</span></span>

## <span data-ttu-id="47d5e-146">Note</span><span class="sxs-lookup"><span data-stu-id="47d5e-146">NOTES</span></span>

## <span data-ttu-id="47d5e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47d5e-147">RELATED LINKS</span></span>
