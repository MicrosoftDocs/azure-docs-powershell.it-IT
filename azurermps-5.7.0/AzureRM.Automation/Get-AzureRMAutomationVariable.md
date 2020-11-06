---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522085"
---
# <span data-ttu-id="555d2-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="555d2-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="555d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="555d2-102">SYNOPSIS</span></span>
<span data-ttu-id="555d2-103">Ottiene una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="555d2-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="555d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="555d2-104">SYNTAX</span></span>

### <span data-ttu-id="555d2-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="555d2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="555d2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="555d2-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="555d2-107">DESCRIPTION</span></span>
<span data-ttu-id="555d2-108">Il cmdlet **Get-AzureRmAutomationVariable** ottiene una o più variabili di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="555d2-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="555d2-109">Per ottenere una variabile specifica, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="555d2-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="555d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="555d2-110">EXAMPLES</span></span>

### <span data-ttu-id="555d2-111">Esempio 1: ottenere una variabile</span><span class="sxs-lookup"><span data-stu-id="555d2-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="555d2-112">Il primo comando ottiene una variabile di automazione denominata Variable06 nell'account denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="555d2-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="555d2-113">Il comando Archivia l'oggetto nella variabile $Variable.</span><span class="sxs-lookup"><span data-stu-id="555d2-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="555d2-114">Il secondo comando usa la notazione standard del punto per fare riferimento alla proprietà **value** di $Variable.</span><span class="sxs-lookup"><span data-stu-id="555d2-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="555d2-115">Il comando Archivia il valore nella variabile $value.</span><span class="sxs-lookup"><span data-stu-id="555d2-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="555d2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="555d2-116">PARAMETERS</span></span>

### <span data-ttu-id="555d2-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="555d2-117">-AutomationAccountName</span></span>
<span data-ttu-id="555d2-118">Specifica il nome dell'account di automazione che contiene le variabili ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="555d2-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="555d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555d2-119">-DefaultProfile</span></span>
<span data-ttu-id="555d2-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="555d2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="555d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="555d2-121">-Name</span></span>
<span data-ttu-id="555d2-122">Specifica il nome di una variabile ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="555d2-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="555d2-124">Specifica il gruppo di risorse per cui questo cmdlet ottiene le variabili.</span><span class="sxs-lookup"><span data-stu-id="555d2-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="555d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555d2-125">CommonParameters</span></span>
<span data-ttu-id="555d2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555d2-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555d2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555d2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="555d2-128">INPUTS</span></span>

### <span data-ttu-id="555d2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="555d2-129">None</span></span>
<span data-ttu-id="555d2-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="555d2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="555d2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="555d2-131">OUTPUTS</span></span>

### <span data-ttu-id="555d2-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="555d2-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="555d2-133">Note</span><span class="sxs-lookup"><span data-stu-id="555d2-133">NOTES</span></span>

## <span data-ttu-id="555d2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="555d2-134">RELATED LINKS</span></span>

[<span data-ttu-id="555d2-135">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="555d2-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="555d2-136">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="555d2-136">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="555d2-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="555d2-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


