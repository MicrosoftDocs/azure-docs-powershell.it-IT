---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: 1ec020aa93b1a7e6964e8f85eb8a02c6a9f895cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835347"
---
# <span data-ttu-id="cbf7e-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cbf7e-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="cbf7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf7e-103">Esegue un'app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="cbf7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbf7e-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbf7e-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf7e-106">Il cmdlet **Start-AzLogicApp** esegue un'app logica usando la funzionalità delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="cbf7e-107">Specificare un nome, un gruppo di risorse e un trigger.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="cbf7e-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cbf7e-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cbf7e-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cbf7e-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cbf7e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbf7e-112">EXAMPLES</span></span>

### <span data-ttu-id="cbf7e-113">Esempio 1: eseguire un'app logica</span><span class="sxs-lookup"><span data-stu-id="cbf7e-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="cbf7e-114">Questo comando esegue l'app logica nel gruppo risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="cbf7e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbf7e-115">PARAMETERS</span></span>

### <span data-ttu-id="cbf7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf7e-116">-DefaultProfile</span></span>
<span data-ttu-id="cbf7e-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cbf7e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbf7e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbf7e-118">-Name</span></span>
<span data-ttu-id="cbf7e-119">Specifica il nome dell'app logica avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cbf7e-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="cbf7e-120">-Parameters</span></span>
<span data-ttu-id="cbf7e-121">Specifica un oggetto raccolta Parameters dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="cbf7e-122">Specificare una tabella hash, una \< stringa di dizionario \> o una stringa di dizionario \< , WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="cbf7e-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="cbf7e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf7e-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbf7e-124">Specifica il nome del gruppo di risorse che contiene l'app logica avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cbf7e-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="cbf7e-125">-TriggerName</span></span>
<span data-ttu-id="cbf7e-126">Specifica il nome del trigger dell'app logica avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cbf7e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cbf7e-127">-Confirm</span></span>
<span data-ttu-id="cbf7e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbf7e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf7e-129">-WhatIf</span></span>
<span data-ttu-id="cbf7e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf7e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbf7e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf7e-132">CommonParameters</span></span>
<span data-ttu-id="cbf7e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf7e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf7e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf7e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf7e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbf7e-135">INPUTS</span></span>

### <span data-ttu-id="cbf7e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf7e-136">System.String</span></span>

## <span data-ttu-id="cbf7e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbf7e-137">OUTPUTS</span></span>

### <span data-ttu-id="cbf7e-138">System. void</span><span class="sxs-lookup"><span data-stu-id="cbf7e-138">System.Void</span></span>

## <span data-ttu-id="cbf7e-139">Note</span><span class="sxs-lookup"><span data-stu-id="cbf7e-139">NOTES</span></span>

## <span data-ttu-id="cbf7e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbf7e-140">RELATED LINKS</span></span>

[<span data-ttu-id="cbf7e-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cbf7e-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="cbf7e-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="cbf7e-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="cbf7e-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cbf7e-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="cbf7e-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cbf7e-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="cbf7e-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="cbf7e-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="cbf7e-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="cbf7e-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


