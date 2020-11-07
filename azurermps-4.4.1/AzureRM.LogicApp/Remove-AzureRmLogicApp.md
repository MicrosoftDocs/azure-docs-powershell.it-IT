---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 6b76440b2d9e61075ac19e5a6fa0846a95a77669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687173"
---
# <span data-ttu-id="3634f-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3634f-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="3634f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3634f-102">SYNOPSIS</span></span>
<span data-ttu-id="3634f-103">Rimuove un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3634f-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3634f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3634f-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3634f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3634f-105">DESCRIPTION</span></span>
<span data-ttu-id="3634f-106">Il cmdlet **Remove-AzureRmLogicApp** rimuove un'app logica da un gruppo di risorse usando la caratteristica delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="3634f-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="3634f-107">Specifica il gruppo delle app e delle risorse logiche.</span><span class="sxs-lookup"><span data-stu-id="3634f-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="3634f-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="3634f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3634f-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="3634f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3634f-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3634f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3634f-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="3634f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3634f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3634f-112">EXAMPLES</span></span>

### <span data-ttu-id="3634f-113">Esempio 1: rimuovere un'app logica</span><span class="sxs-lookup"><span data-stu-id="3634f-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="3634f-114">Questo comando rimuove un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3634f-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="3634f-115">Il comando include il parametro *Force* , che impedisce al comando di richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3634f-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="3634f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3634f-116">PARAMETERS</span></span>

### <span data-ttu-id="3634f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3634f-117">-Force</span></span>
<span data-ttu-id="3634f-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3634f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3634f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3634f-119">-Name</span></span>
<span data-ttu-id="3634f-120">Specifica il nome dell'app logica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3634f-120">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3634f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3634f-121">-ResourceGroupName</span></span>
<span data-ttu-id="3634f-122">Specifica il nome del gruppo di risorse che contiene l'app logica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3634f-122">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3634f-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3634f-123">-Confirm</span></span>
<span data-ttu-id="3634f-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3634f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3634f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3634f-125">-WhatIf</span></span>
<span data-ttu-id="3634f-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3634f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3634f-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3634f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3634f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3634f-128">-DefaultProfile</span></span>
<span data-ttu-id="3634f-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3634f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3634f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3634f-130">CommonParameters</span></span>
<span data-ttu-id="3634f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3634f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3634f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3634f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3634f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3634f-133">INPUTS</span></span>

## <span data-ttu-id="3634f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3634f-134">OUTPUTS</span></span>

### <span data-ttu-id="3634f-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="3634f-135">System.Object</span></span>

## <span data-ttu-id="3634f-136">Note</span><span class="sxs-lookup"><span data-stu-id="3634f-136">NOTES</span></span>

## <span data-ttu-id="3634f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3634f-137">RELATED LINKS</span></span>

[<span data-ttu-id="3634f-138">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3634f-138">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="3634f-139">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3634f-139">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="3634f-140">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3634f-140">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="3634f-141">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3634f-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


