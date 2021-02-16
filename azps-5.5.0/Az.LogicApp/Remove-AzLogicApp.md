---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180358"
---
# <span data-ttu-id="424d3-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="424d3-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="424d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424d3-102">SYNOPSIS</span></span>
<span data-ttu-id="424d3-103">Rimuove un'app per la logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="424d3-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="424d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="424d3-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="424d3-105">DESCRIPTION</span></span>
<span data-ttu-id="424d3-106">Il cmdlet **Remove-AzLogicApp** rimuove un'app per la logica da un gruppo di risorse usando la caratteristica App per la logica.</span><span class="sxs-lookup"><span data-stu-id="424d3-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="424d3-107">Specificare l'app logica e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="424d3-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="424d3-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="424d3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="424d3-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="424d3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="424d3-110">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="424d3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="424d3-111">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="424d3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="424d3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="424d3-112">EXAMPLES</span></span>

### <span data-ttu-id="424d3-113">Esempio 1: Rimuovere un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="424d3-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="424d3-114">Questo comando rimuove un'app per la logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="424d3-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="424d3-115">Il comando include il *parametro Force,* che impedisce al comando di richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="424d3-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="424d3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="424d3-116">PARAMETERS</span></span>

### <span data-ttu-id="424d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424d3-117">-DefaultProfile</span></span>
<span data-ttu-id="424d3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="424d3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="424d3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="424d3-119">-Force</span></span>
<span data-ttu-id="424d3-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="424d3-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="424d3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="424d3-121">-Name</span></span>
<span data-ttu-id="424d3-122">Specifica il nome dell'app per la logica rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424d3-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="424d3-124">Specifica il nome del gruppo di risorse che contiene l'app logica rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424d3-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="424d3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="424d3-125">-Confirm</span></span>
<span data-ttu-id="424d3-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="424d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424d3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424d3-127">-WhatIf</span></span>
<span data-ttu-id="424d3-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="424d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424d3-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="424d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424d3-130">CommonParameters</span></span>
<span data-ttu-id="424d3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="424d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424d3-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424d3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424d3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="424d3-133">INPUTS</span></span>

### <span data-ttu-id="424d3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="424d3-134">System.String</span></span>

## <span data-ttu-id="424d3-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="424d3-135">OUTPUTS</span></span>

### <span data-ttu-id="424d3-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="424d3-136">System.Void</span></span>

## <span data-ttu-id="424d3-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="424d3-137">NOTES</span></span>

## <span data-ttu-id="424d3-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="424d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="424d3-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="424d3-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="424d3-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="424d3-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="424d3-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="424d3-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="424d3-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="424d3-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


