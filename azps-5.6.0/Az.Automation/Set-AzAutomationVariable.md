---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: ff83049e6afec5b0a6712aef2622bd9cbe0110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004685"
---
# <span data-ttu-id="63cfb-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="63cfb-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="63cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="63cfb-103">Modifica una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="63cfb-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="63cfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63cfb-104">SYNTAX</span></span>

### <span data-ttu-id="63cfb-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="63cfb-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63cfb-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="63cfb-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63cfb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63cfb-107">DESCRIPTION</span></span>
<span data-ttu-id="63cfb-108">Il cmdlet **Set-AzAutomationVariable** modifica il valore o la descrizione di una variabile nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="63cfb-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="63cfb-109">Per crittografare la variabile, specificare *il parametro Encrypted.*</span><span class="sxs-lookup"><span data-stu-id="63cfb-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="63cfb-110">Non è possibile modificare lo stato crittografato di una variabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="63cfb-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="63cfb-111">Se si specifica *Encrypted* per una variabile esistente non crittografata, la variabile non riesce.</span><span class="sxs-lookup"><span data-stu-id="63cfb-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="63cfb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63cfb-112">EXAMPLES</span></span>

### <span data-ttu-id="63cfb-113">Esempio 1: Impostare il valore di una variabile</span><span class="sxs-lookup"><span data-stu-id="63cfb-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="63cfb-114">Questo comando imposta un nuovo valore per la variabile denominata StringVariable22 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="63cfb-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="63cfb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63cfb-115">PARAMETERS</span></span>

### <span data-ttu-id="63cfb-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63cfb-116">-AutomationAccountName</span></span>
<span data-ttu-id="63cfb-117">Specifica il nome dell'account di automazione in cui è archiviata la variabile.</span><span class="sxs-lookup"><span data-stu-id="63cfb-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="63cfb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cfb-118">-DefaultProfile</span></span>
<span data-ttu-id="63cfb-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="63cfb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63cfb-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="63cfb-120">-Description</span></span>
<span data-ttu-id="63cfb-121">Specifica una descrizione della variabile.</span><span class="sxs-lookup"><span data-stu-id="63cfb-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cfb-122">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="63cfb-122">-Encrypted</span></span>
<span data-ttu-id="63cfb-123">Specifica se il cmdlet crittografa il valore della variabile per lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63cfb-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cfb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="63cfb-124">-Name</span></span>
<span data-ttu-id="63cfb-125">Specifica il nome della variabile modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63cfb-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cfb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cfb-126">-ResourceGroupName</span></span>
<span data-ttu-id="63cfb-127">Specifica il gruppo di risorse per cui questo cmdlet modifica una variabile.</span><span class="sxs-lookup"><span data-stu-id="63cfb-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="63cfb-128">-Value</span><span class="sxs-lookup"><span data-stu-id="63cfb-128">-Value</span></span>
<span data-ttu-id="63cfb-129">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="63cfb-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cfb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cfb-130">CommonParameters</span></span>
<span data-ttu-id="63cfb-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63cfb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cfb-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63cfb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cfb-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="63cfb-133">INPUTS</span></span>

### <span data-ttu-id="63cfb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="63cfb-134">System.String</span></span>

### <span data-ttu-id="63cfb-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63cfb-135">System.Boolean</span></span>

### <span data-ttu-id="63cfb-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="63cfb-136">System.Object</span></span>

## <span data-ttu-id="63cfb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63cfb-137">OUTPUTS</span></span>

### <span data-ttu-id="63cfb-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="63cfb-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="63cfb-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="63cfb-139">NOTES</span></span>

## <span data-ttu-id="63cfb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63cfb-140">RELATED LINKS</span></span>

[<span data-ttu-id="63cfb-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="63cfb-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="63cfb-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="63cfb-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="63cfb-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="63cfb-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


