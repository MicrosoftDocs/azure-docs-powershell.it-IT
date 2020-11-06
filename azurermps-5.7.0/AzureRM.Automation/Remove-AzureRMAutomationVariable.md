---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515807"
---
# <span data-ttu-id="8f9cd-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f9cd-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="8f9cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9cd-103">Rimuove una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f9cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f9cd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f9cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f9cd-105">DESCRIPTION</span></span>
<span data-ttu-id="8f9cd-106">Il cmdlet **Remove-AzureRmAutomationVariable** consente di rimuovere una variabile da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="8f9cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f9cd-107">EXAMPLES</span></span>

### <span data-ttu-id="8f9cd-108">Esempio 1: rimuovere una variabile</span><span class="sxs-lookup"><span data-stu-id="8f9cd-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f9cd-109">Questo comando consente di rimuovere una variabile denominata StringVariable22 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="8f9cd-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="8f9cd-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8f9cd-111">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8f9cd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f9cd-112">PARAMETERS</span></span>

### <span data-ttu-id="8f9cd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f9cd-113">-AutomationAccountName</span></span>
<span data-ttu-id="8f9cd-114">Specifica il nome dell'account di automazione che contiene la variabile eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8f9cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9cd-115">-DefaultProfile</span></span>
<span data-ttu-id="8f9cd-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8f9cd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f9cd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f9cd-117">-Name</span></span>
<span data-ttu-id="8f9cd-118">Specifica il nome della variabile eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8f9cd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f9cd-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f9cd-120">Specifica il gruppo di risorse per cui questo cmdlet elimina una variabile.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="8f9cd-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f9cd-121">-Confirm</span></span>
<span data-ttu-id="8f9cd-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f9cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f9cd-123">-WhatIf</span></span>
<span data-ttu-id="8f9cd-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f9cd-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f9cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9cd-126">CommonParameters</span></span>
<span data-ttu-id="8f9cd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9cd-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f9cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9cd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f9cd-129">INPUTS</span></span>

### <span data-ttu-id="8f9cd-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8f9cd-130">None</span></span>
<span data-ttu-id="8f9cd-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f9cd-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f9cd-132">OUTPUTS</span></span>

### <span data-ttu-id="8f9cd-133">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="8f9cd-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="8f9cd-134">Note</span><span class="sxs-lookup"><span data-stu-id="8f9cd-134">NOTES</span></span>

## <span data-ttu-id="8f9cd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f9cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="8f9cd-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f9cd-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="8f9cd-137">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f9cd-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="8f9cd-138">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8f9cd-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


