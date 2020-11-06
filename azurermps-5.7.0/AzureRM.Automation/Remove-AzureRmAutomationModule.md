---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2ce97441769c15ed122dc7921554b4fa1c5a144f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522072"
---
# <span data-ttu-id="a4717-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a4717-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="a4717-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4717-102">SYNOPSIS</span></span>
<span data-ttu-id="a4717-103">Rimuove un modulo dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="a4717-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4717-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4717-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4717-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4717-105">DESCRIPTION</span></span>
<span data-ttu-id="a4717-106">Il cmdlet **Remove-AzureRmAutomationModule** rimuove un modulo da un account di automazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a4717-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="a4717-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4717-107">EXAMPLES</span></span>

### <span data-ttu-id="a4717-108">Esempio 1: rimuovere un modulo</span><span class="sxs-lookup"><span data-stu-id="a4717-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a4717-109">Questo comando rimuove un modulo denominato ContosoModule dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a4717-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a4717-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4717-110">PARAMETERS</span></span>

### <span data-ttu-id="a4717-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4717-111">-AutomationAccountName</span></span>
<span data-ttu-id="a4717-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove un modulo.</span><span class="sxs-lookup"><span data-stu-id="a4717-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4717-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4717-113">-DefaultProfile</span></span>
<span data-ttu-id="a4717-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4717-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4717-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a4717-115">-Force</span></span>
<span data-ttu-id="a4717-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a4717-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4717-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4717-117">-Name</span></span>
<span data-ttu-id="a4717-118">Specifica il nome del modulo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4717-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4717-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4717-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4717-120">Specifica il nome di un gruppo di risorse in cui questo cmdlet rimuove un modulo.</span><span class="sxs-lookup"><span data-stu-id="a4717-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4717-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4717-121">-Confirm</span></span>
<span data-ttu-id="a4717-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4717-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4717-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4717-123">-WhatIf</span></span>
<span data-ttu-id="a4717-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4717-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4717-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4717-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4717-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4717-126">CommonParameters</span></span>
<span data-ttu-id="a4717-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4717-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4717-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4717-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4717-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4717-129">INPUTS</span></span>

### <span data-ttu-id="a4717-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a4717-130">None</span></span>
<span data-ttu-id="a4717-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a4717-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4717-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4717-132">OUTPUTS</span></span>

## <span data-ttu-id="a4717-133">Note</span><span class="sxs-lookup"><span data-stu-id="a4717-133">NOTES</span></span>

## <span data-ttu-id="a4717-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4717-134">RELATED LINKS</span></span>

[<span data-ttu-id="a4717-135">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a4717-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="a4717-136">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a4717-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="a4717-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a4717-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


