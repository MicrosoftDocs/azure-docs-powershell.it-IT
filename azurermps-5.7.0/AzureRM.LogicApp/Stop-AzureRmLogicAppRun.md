---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/stop-azurermlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: 1d23c4f92a73a2ec6471169a05c1048d96abcaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515664"
---
# <span data-ttu-id="22d37-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="22d37-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="22d37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22d37-102">SYNOPSIS</span></span>
<span data-ttu-id="22d37-103">Annulla un'esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="22d37-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22d37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22d37-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d37-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22d37-105">DESCRIPTION</span></span>
<span data-ttu-id="22d37-106">Il cmdlet **Stop-AzureRmLogicAppRun** Annulla un'esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="22d37-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="22d37-107">Specifica l'app logica, il gruppo di risorse ed Esegui.</span><span class="sxs-lookup"><span data-stu-id="22d37-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="22d37-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="22d37-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="22d37-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="22d37-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="22d37-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="22d37-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="22d37-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="22d37-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="22d37-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22d37-112">EXAMPLES</span></span>

### <span data-ttu-id="22d37-113">Esempio 1: annullare un'esecuzione di un'app logica</span><span class="sxs-lookup"><span data-stu-id="22d37-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="22d37-114">Questo comando Annulla un'esecuzione dell'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="22d37-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="22d37-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22d37-115">PARAMETERS</span></span>

### <span data-ttu-id="22d37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d37-116">-DefaultProfile</span></span>
<span data-ttu-id="22d37-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="22d37-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22d37-118">-Force</span><span class="sxs-lookup"><span data-stu-id="22d37-118">-Force</span></span>
<span data-ttu-id="22d37-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="22d37-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22d37-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="22d37-120">-Name</span></span>
<span data-ttu-id="22d37-121">Specifica il nome di un'app logica per cui questo cmdlet Annulla un'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="22d37-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d37-122">-ResourceGroupName</span></span>
<span data-ttu-id="22d37-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet Annulla un'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="22d37-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="22d37-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="22d37-124">-RunName</span></span>
<span data-ttu-id="22d37-125">Specifica il nome di un'app logica eseguita dall'annullamento di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22d37-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="22d37-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22d37-126">-Confirm</span></span>
<span data-ttu-id="22d37-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22d37-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d37-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d37-128">-WhatIf</span></span>
<span data-ttu-id="22d37-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22d37-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d37-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22d37-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d37-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d37-131">CommonParameters</span></span>
<span data-ttu-id="22d37-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d37-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d37-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d37-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d37-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22d37-134">INPUTS</span></span>

### <span data-ttu-id="22d37-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22d37-135">None</span></span>
<span data-ttu-id="22d37-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="22d37-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22d37-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22d37-137">OUTPUTS</span></span>

### <span data-ttu-id="22d37-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="22d37-138">System.Object</span></span>

## <span data-ttu-id="22d37-139">Note</span><span class="sxs-lookup"><span data-stu-id="22d37-139">NOTES</span></span>

## <span data-ttu-id="22d37-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22d37-140">RELATED LINKS</span></span>

[<span data-ttu-id="22d37-141">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="22d37-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


