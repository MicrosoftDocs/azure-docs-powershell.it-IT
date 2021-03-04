---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: c109839692ea20f1fbbcced50df9c4167322b1b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952461"
---
# <span data-ttu-id="a0f81-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f81-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="a0f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f81-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f81-103">Esegue un'app per la logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a0f81-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="a0f81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0f81-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f81-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a0f81-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f81-106">Il cmdlet **Start-AzLogicApp** esegue un'app di logica usando la funzionalità App logica.</span><span class="sxs-lookup"><span data-stu-id="a0f81-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="a0f81-107">Specificare un nome, un gruppo di risorse e un trigger.</span><span class="sxs-lookup"><span data-stu-id="a0f81-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="a0f81-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="a0f81-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a0f81-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="a0f81-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a0f81-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0f81-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a0f81-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="a0f81-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a0f81-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0f81-112">EXAMPLES</span></span>

### <span data-ttu-id="a0f81-113">Esempio 1: Eseguire un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="a0f81-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="a0f81-114">Questo comando esegue l'app per la logica nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a0f81-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a0f81-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0f81-115">PARAMETERS</span></span>

### <span data-ttu-id="a0f81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f81-116">-DefaultProfile</span></span>
<span data-ttu-id="a0f81-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a0f81-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0f81-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a0f81-118">-Name</span></span>
<span data-ttu-id="a0f81-119">Specifica il nome dell'app per la logica avviata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f81-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f81-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="a0f81-120">-Parameters</span></span>
<span data-ttu-id="a0f81-121">Specifica un oggetto raccolta di parametri dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="a0f81-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="a0f81-122">Specificare una tabella hash, \<string\> un dizionario o un \<string, WorkflowParameter\> dizionario.</span><span class="sxs-lookup"><span data-stu-id="a0f81-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f81-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0f81-124">Specifica il nome del gruppo di risorse che contiene l'app per la logica avviata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f81-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f81-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a0f81-125">-TriggerName</span></span>
<span data-ttu-id="a0f81-126">Specifica il nome del trigger dell'app per la logica che viene avviato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f81-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f81-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0f81-127">-Confirm</span></span>
<span data-ttu-id="a0f81-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f81-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f81-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f81-129">-WhatIf</span></span>
<span data-ttu-id="a0f81-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0f81-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f81-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0f81-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f81-132">CommonParameters</span></span>
<span data-ttu-id="a0f81-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f81-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f81-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f81-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="a0f81-135">INPUTS</span></span>

### <span data-ttu-id="a0f81-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a0f81-136">System.String</span></span>

## <span data-ttu-id="a0f81-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0f81-137">OUTPUTS</span></span>

### <span data-ttu-id="a0f81-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="a0f81-138">System.Void</span></span>

## <span data-ttu-id="a0f81-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a0f81-139">NOTES</span></span>

## <span data-ttu-id="a0f81-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0f81-140">RELATED LINKS</span></span>

[<span data-ttu-id="a0f81-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f81-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="a0f81-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a0f81-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="a0f81-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f81-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="a0f81-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f81-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="a0f81-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0f81-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="a0f81-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a0f81-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


