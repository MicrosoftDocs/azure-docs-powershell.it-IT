---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 54bbda0226cf2aa374e149bc4b5885b86b31ef12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685072"
---
# <span data-ttu-id="8ca50-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8ca50-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="8ca50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ca50-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca50-103">Ottiene i metadati per i moduli dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="8ca50-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="8ca50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ca50-104">SYNTAX</span></span>

### <span data-ttu-id="8ca50-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ca50-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ca50-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ca50-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ca50-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca50-107">DESCRIPTION</span></span>
<span data-ttu-id="8ca50-108">Il cmdlet **Get-AzAutomationModule** ottiene i metadati per i moduli di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8ca50-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="8ca50-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ca50-109">EXAMPLES</span></span>

### <span data-ttu-id="8ca50-110">Esempio 1: ottenere tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="8ca50-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8ca50-111">Questo comando consente di ottenere tutti i moduli nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ca50-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8ca50-112">Esempio 2: ottenere un modulo</span><span class="sxs-lookup"><span data-stu-id="8ca50-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8ca50-113">Questo comando ottiene un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ca50-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8ca50-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ca50-114">PARAMETERS</span></span>

### <span data-ttu-id="8ca50-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ca50-115">-AutomationAccountName</span></span>
<span data-ttu-id="8ca50-116">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="8ca50-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca50-117">-DefaultProfile</span></span>
<span data-ttu-id="8ca50-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8ca50-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ca50-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ca50-119">-Name</span></span>
<span data-ttu-id="8ca50-120">Specifica il nome del modulo per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="8ca50-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca50-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca50-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ca50-122">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="8ca50-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca50-123">CommonParameters</span></span>
<span data-ttu-id="8ca50-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca50-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca50-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca50-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ca50-126">INPUTS</span></span>

### <span data-ttu-id="8ca50-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca50-127">System.String</span></span>

## <span data-ttu-id="8ca50-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ca50-128">OUTPUTS</span></span>

### <span data-ttu-id="8ca50-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="8ca50-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="8ca50-130">Note</span><span class="sxs-lookup"><span data-stu-id="8ca50-130">NOTES</span></span>

## <span data-ttu-id="8ca50-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ca50-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ca50-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8ca50-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="8ca50-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8ca50-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="8ca50-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8ca50-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)

