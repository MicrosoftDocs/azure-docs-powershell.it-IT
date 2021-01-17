---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351136"
---
# <span data-ttu-id="69054-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69054-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="69054-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69054-102">SYNOPSIS</span></span>
<span data-ttu-id="69054-103">Rimuove un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="69054-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="69054-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69054-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69054-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69054-105">DESCRIPTION</span></span>
<span data-ttu-id="69054-106">Il cmdlet **Remove-AzLogicApp** rimuove un'app logica da un gruppo di risorse usando la caratteristica delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="69054-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="69054-107">Specifica il gruppo delle app e delle risorse logiche.</span><span class="sxs-lookup"><span data-stu-id="69054-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="69054-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="69054-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="69054-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="69054-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="69054-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="69054-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="69054-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="69054-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="69054-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69054-112">EXAMPLES</span></span>

### <span data-ttu-id="69054-113">Esempio 1: rimuovere un'app logica</span><span class="sxs-lookup"><span data-stu-id="69054-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="69054-114">Questo comando rimuove un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="69054-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="69054-115">Il comando include il parametro *Force* , che impedisce al comando di richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="69054-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="69054-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69054-116">PARAMETERS</span></span>

### <span data-ttu-id="69054-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69054-117">-DefaultProfile</span></span>
<span data-ttu-id="69054-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="69054-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69054-119">-Force</span><span class="sxs-lookup"><span data-stu-id="69054-119">-Force</span></span>
<span data-ttu-id="69054-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="69054-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69054-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="69054-121">-Name</span></span>
<span data-ttu-id="69054-122">Specifica il nome dell'app logica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69054-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="69054-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69054-123">-ResourceGroupName</span></span>
<span data-ttu-id="69054-124">Specifica il nome del gruppo di risorse che contiene l'app logica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69054-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="69054-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69054-125">-Confirm</span></span>
<span data-ttu-id="69054-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69054-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69054-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69054-127">-WhatIf</span></span>
<span data-ttu-id="69054-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69054-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69054-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69054-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69054-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69054-130">CommonParameters</span></span>
<span data-ttu-id="69054-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69054-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69054-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69054-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69054-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69054-133">INPUTS</span></span>

### <span data-ttu-id="69054-134">System. String</span><span class="sxs-lookup"><span data-stu-id="69054-134">System.String</span></span>

## <span data-ttu-id="69054-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69054-135">OUTPUTS</span></span>

### <span data-ttu-id="69054-136">System. void</span><span class="sxs-lookup"><span data-stu-id="69054-136">System.Void</span></span>

## <span data-ttu-id="69054-137">Note</span><span class="sxs-lookup"><span data-stu-id="69054-137">NOTES</span></span>

## <span data-ttu-id="69054-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69054-138">RELATED LINKS</span></span>

[<span data-ttu-id="69054-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69054-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="69054-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69054-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="69054-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69054-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="69054-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69054-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


