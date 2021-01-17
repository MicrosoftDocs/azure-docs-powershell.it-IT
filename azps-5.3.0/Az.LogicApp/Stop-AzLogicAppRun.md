---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386133"
---
# <span data-ttu-id="80381-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="80381-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="80381-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80381-102">SYNOPSIS</span></span>
<span data-ttu-id="80381-103">Annulla un'esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="80381-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="80381-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80381-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80381-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80381-105">DESCRIPTION</span></span>
<span data-ttu-id="80381-106">Il cmdlet **Stop-AzLogicAppRun** Annulla un'esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="80381-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="80381-107">Specifica l'app logica, il gruppo di risorse ed Esegui.</span><span class="sxs-lookup"><span data-stu-id="80381-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="80381-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="80381-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="80381-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="80381-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="80381-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="80381-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="80381-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="80381-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="80381-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80381-112">EXAMPLES</span></span>

### <span data-ttu-id="80381-113">Esempio 1: annullare un'esecuzione di un'app logica</span><span class="sxs-lookup"><span data-stu-id="80381-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="80381-114">Questo comando Annulla un'esecuzione dell'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="80381-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="80381-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80381-115">PARAMETERS</span></span>

### <span data-ttu-id="80381-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80381-116">-DefaultProfile</span></span>
<span data-ttu-id="80381-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="80381-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80381-118">-Force</span><span class="sxs-lookup"><span data-stu-id="80381-118">-Force</span></span>
<span data-ttu-id="80381-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="80381-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80381-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="80381-120">-Name</span></span>
<span data-ttu-id="80381-121">Specifica il nome di un'app logica per cui questo cmdlet Annulla un'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="80381-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="80381-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80381-122">-ResourceGroupName</span></span>
<span data-ttu-id="80381-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet Annulla un'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="80381-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="80381-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="80381-124">-RunName</span></span>
<span data-ttu-id="80381-125">Specifica il nome di un'app logica eseguita dall'annullamento di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80381-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="80381-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80381-126">-Confirm</span></span>
<span data-ttu-id="80381-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80381-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80381-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80381-128">-WhatIf</span></span>
<span data-ttu-id="80381-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80381-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80381-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80381-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80381-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80381-131">CommonParameters</span></span>
<span data-ttu-id="80381-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80381-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80381-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80381-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80381-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80381-134">INPUTS</span></span>

### <span data-ttu-id="80381-135">System. String</span><span class="sxs-lookup"><span data-stu-id="80381-135">System.String</span></span>

## <span data-ttu-id="80381-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80381-136">OUTPUTS</span></span>

### <span data-ttu-id="80381-137">System. void</span><span class="sxs-lookup"><span data-stu-id="80381-137">System.Void</span></span>

## <span data-ttu-id="80381-138">Note</span><span class="sxs-lookup"><span data-stu-id="80381-138">NOTES</span></span>

## <span data-ttu-id="80381-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80381-139">RELATED LINKS</span></span>

[<span data-ttu-id="80381-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="80381-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


