---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 3650e04b8c6d254b396072c55d39cde38a1328f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518059"
---
# <span data-ttu-id="8e8d9-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8e8d9-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="8e8d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8d9-103">Rimuove un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e8d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e8d9-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8d9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e8d9-105">DESCRIPTION</span></span>
<span data-ttu-id="8e8d9-106">Il cmdlet **Remove-AzureRmLogicApp** rimuove un'app logica da un gruppo di risorse usando la caratteristica delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="8e8d9-107">Specifica il gruppo delle app e delle risorse logiche.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="8e8d9-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8e8d9-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8e8d9-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8e8d9-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8e8d9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e8d9-112">EXAMPLES</span></span>

### <span data-ttu-id="8e8d9-113">Esempio 1: rimuovere un'app logica</span><span class="sxs-lookup"><span data-stu-id="8e8d9-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="8e8d9-114">Questo comando rimuove un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="8e8d9-115">Il comando include il parametro *Force* , che impedisce al comando di richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="8e8d9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e8d9-116">PARAMETERS</span></span>

### <span data-ttu-id="8e8d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8d9-117">-DefaultProfile</span></span>
<span data-ttu-id="8e8d9-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8e8d9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8d9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e8d9-119">-Force</span></span>
<span data-ttu-id="8e8d9-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8d9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e8d9-121">-Name</span></span>
<span data-ttu-id="8e8d9-122">Specifica il nome dell'app logica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e8d9-124">Specifica il nome del gruppo di risorse che contiene l'app logica rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e8d9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e8d9-125">-Confirm</span></span>
<span data-ttu-id="8e8d9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8d9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8d9-127">-WhatIf</span></span>
<span data-ttu-id="8e8d9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e8d9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e8d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8d9-130">CommonParameters</span></span>
<span data-ttu-id="8e8d9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8d9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e8d9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8d9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e8d9-133">INPUTS</span></span>

### <span data-ttu-id="8e8d9-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8e8d9-134">None</span></span>
<span data-ttu-id="8e8d9-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8e8d9-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e8d9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e8d9-136">OUTPUTS</span></span>

### <span data-ttu-id="8e8d9-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="8e8d9-137">System.Object</span></span>

## <span data-ttu-id="8e8d9-138">Note</span><span class="sxs-lookup"><span data-stu-id="8e8d9-138">NOTES</span></span>

## <span data-ttu-id="8e8d9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e8d9-139">RELATED LINKS</span></span>

[<span data-ttu-id="8e8d9-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8e8d9-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="8e8d9-141">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8e8d9-141">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="8e8d9-142">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8e8d9-142">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="8e8d9-143">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8e8d9-143">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


