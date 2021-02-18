---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201143"
---
# <span data-ttu-id="364b4-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="364b4-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="364b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="364b4-102">SYNOPSIS</span></span>
<span data-ttu-id="364b4-103">Ottiene una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="364b4-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="364b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="364b4-104">SYNTAX</span></span>

### <span data-ttu-id="364b4-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="364b4-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="364b4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="364b4-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="364b4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="364b4-107">DESCRIPTION</span></span>
<span data-ttu-id="364b4-108">Il cmdlet **Get-AzAutomationVariable** ottiene una o più variabili di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="364b4-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="364b4-109">Per ottenere una variabile specifica, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="364b4-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="364b4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="364b4-110">EXAMPLES</span></span>

### <span data-ttu-id="364b4-111">Esempio 1: Ottenere una variabile</span><span class="sxs-lookup"><span data-stu-id="364b4-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="364b4-112">Il primo comando ottiene una variabile di automazione denominata Variabile06 nell'account denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="364b4-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="364b4-113">Il comando archivia l'oggetto nella $Variable variabile.</span><span class="sxs-lookup"><span data-stu-id="364b4-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="364b4-114">Il secondo comando usa la notazione punto standard per fare riferimento alla **proprietà valore** di $Variable.</span><span class="sxs-lookup"><span data-stu-id="364b4-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="364b4-115">Il comando archivia il valore nella $value variabile.</span><span class="sxs-lookup"><span data-stu-id="364b4-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="364b4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="364b4-116">PARAMETERS</span></span>

### <span data-ttu-id="364b4-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="364b4-117">-AutomationAccountName</span></span>
<span data-ttu-id="364b4-118">Specifica il nome dell'account di automazione che contiene le variabili recuperate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="364b4-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="364b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364b4-119">-DefaultProfile</span></span>
<span data-ttu-id="364b4-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="364b4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="364b4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="364b4-121">-Name</span></span>
<span data-ttu-id="364b4-122">Specifica il nome di una variabile recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="364b4-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="364b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="364b4-124">Specifica il gruppo di risorse per cui questo cmdlet ottiene le variabili.</span><span class="sxs-lookup"><span data-stu-id="364b4-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="364b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364b4-125">CommonParameters</span></span>
<span data-ttu-id="364b4-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364b4-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="364b4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364b4-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="364b4-128">INPUTS</span></span>

### <span data-ttu-id="364b4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="364b4-129">System.String</span></span>

## <span data-ttu-id="364b4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="364b4-130">OUTPUTS</span></span>

### <span data-ttu-id="364b4-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="364b4-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="364b4-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="364b4-132">NOTES</span></span>

## <span data-ttu-id="364b4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="364b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="364b4-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="364b4-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="364b4-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="364b4-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="364b4-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="364b4-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


