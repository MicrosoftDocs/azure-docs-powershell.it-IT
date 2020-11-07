---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: 316df4d265b32fc87388b701f096df61df246d85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687823"
---
# <span data-ttu-id="0f222-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0f222-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="0f222-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f222-102">SYNOPSIS</span></span>
<span data-ttu-id="0f222-103">Esegue un'app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f222-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f222-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f222-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f222-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f222-105">DESCRIPTION</span></span>
<span data-ttu-id="0f222-106">Il cmdlet **Start-AzureRmLogicApp** esegue un'app logica usando la funzionalità delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="0f222-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="0f222-107">Specificare un nome, un gruppo di risorse e un trigger.</span><span class="sxs-lookup"><span data-stu-id="0f222-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="0f222-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="0f222-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0f222-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="0f222-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0f222-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="0f222-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0f222-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="0f222-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0f222-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f222-112">EXAMPLES</span></span>

### <span data-ttu-id="0f222-113">Esempio 1: eseguire un'app logica</span><span class="sxs-lookup"><span data-stu-id="0f222-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="0f222-114">Questo comando esegue l'app logica nel gruppo risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0f222-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0f222-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f222-115">PARAMETERS</span></span>

### <span data-ttu-id="0f222-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f222-116">-DefaultProfile</span></span>
<span data-ttu-id="0f222-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f222-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f222-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f222-118">-Name</span></span>
<span data-ttu-id="0f222-119">Specifica il nome dell'app logica avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f222-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0f222-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="0f222-120">-Parameters</span></span>
<span data-ttu-id="0f222-121">Specifica un oggetto raccolta Parameters dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="0f222-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="0f222-122">Specificare una tabella hash, un dizionario \<string\> o un dizionario \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="0f222-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="0f222-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f222-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f222-124">Specifica il nome del gruppo di risorse che contiene l'app logica avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f222-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0f222-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="0f222-125">-TriggerName</span></span>
<span data-ttu-id="0f222-126">Specifica il nome del trigger dell'app logica avviata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f222-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0f222-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f222-127">-Confirm</span></span>
<span data-ttu-id="0f222-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f222-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f222-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f222-129">-WhatIf</span></span>
<span data-ttu-id="0f222-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f222-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f222-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f222-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f222-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f222-132">CommonParameters</span></span>
<span data-ttu-id="0f222-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f222-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f222-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f222-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f222-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f222-135">INPUTS</span></span>

### <span data-ttu-id="0f222-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0f222-136">System.String</span></span>

## <span data-ttu-id="0f222-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f222-137">OUTPUTS</span></span>

### <span data-ttu-id="0f222-138">System. void</span><span class="sxs-lookup"><span data-stu-id="0f222-138">System.Void</span></span>

## <span data-ttu-id="0f222-139">Note</span><span class="sxs-lookup"><span data-stu-id="0f222-139">NOTES</span></span>

## <span data-ttu-id="0f222-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f222-140">RELATED LINKS</span></span>

[<span data-ttu-id="0f222-141">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0f222-141">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="0f222-142">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0f222-142">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="0f222-143">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0f222-143">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="0f222-144">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0f222-144">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="0f222-145">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0f222-145">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="0f222-146">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="0f222-146">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


