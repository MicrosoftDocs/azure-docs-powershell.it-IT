---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: bc0fb96ace958761f4d6b12b73ac46b93d9a0143
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684957"
---
# <span data-ttu-id="bae98-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bae98-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="bae98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bae98-102">SYNOPSIS</span></span>
<span data-ttu-id="bae98-103">Modifica una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="bae98-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="bae98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bae98-104">SYNTAX</span></span>

### <span data-ttu-id="bae98-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="bae98-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bae98-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="bae98-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bae98-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bae98-107">DESCRIPTION</span></span>
<span data-ttu-id="bae98-108">Il cmdlet **set-AzAutomationVariable** modifica il valore o la descrizione di una variabile in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bae98-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="bae98-109">Per crittografare la variabile, specificare il parametro *crittografato* .</span><span class="sxs-lookup"><span data-stu-id="bae98-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="bae98-110">Non è possibile modificare lo stato crittografato di una variabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="bae98-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="bae98-111">Se si specifica *crittografato* per una variabile esistente non crittografata, non riesce.</span><span class="sxs-lookup"><span data-stu-id="bae98-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="bae98-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bae98-112">EXAMPLES</span></span>

### <span data-ttu-id="bae98-113">Esempio 1: impostare il valore di una variabile</span><span class="sxs-lookup"><span data-stu-id="bae98-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="bae98-114">Questo comando imposta un nuovo valore per la variabile denominata StringVariable22 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bae98-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="bae98-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bae98-115">PARAMETERS</span></span>

### <span data-ttu-id="bae98-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bae98-116">-AutomationAccountName</span></span>
<span data-ttu-id="bae98-117">Specifica il nome dell'account di automazione in cui è archiviata la variabile.</span><span class="sxs-lookup"><span data-stu-id="bae98-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="bae98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae98-118">-DefaultProfile</span></span>
<span data-ttu-id="bae98-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bae98-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bae98-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="bae98-120">-Description</span></span>
<span data-ttu-id="bae98-121">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="bae98-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="bae98-122">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="bae98-122">-Encrypted</span></span>
<span data-ttu-id="bae98-123">Specifica se il cmdlet crittografa il valore della variabile per lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bae98-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="bae98-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bae98-124">-Name</span></span>
<span data-ttu-id="bae98-125">Specifica il nome della variabile che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="bae98-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bae98-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bae98-126">-ResourceGroupName</span></span>
<span data-ttu-id="bae98-127">Specifica il gruppo di risorse per cui questo cmdlet modifica una variabile.</span><span class="sxs-lookup"><span data-stu-id="bae98-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="bae98-128">-Valore</span><span class="sxs-lookup"><span data-stu-id="bae98-128">-Value</span></span>
<span data-ttu-id="bae98-129">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="bae98-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="bae98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae98-130">CommonParameters</span></span>
<span data-ttu-id="bae98-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bae98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae98-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bae98-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae98-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bae98-133">INPUTS</span></span>

### <span data-ttu-id="bae98-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bae98-134">System.String</span></span>

### <span data-ttu-id="bae98-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bae98-135">System.Boolean</span></span>

### <span data-ttu-id="bae98-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="bae98-136">System.Object</span></span>

## <span data-ttu-id="bae98-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bae98-137">OUTPUTS</span></span>

### <span data-ttu-id="bae98-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="bae98-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="bae98-139">Note</span><span class="sxs-lookup"><span data-stu-id="bae98-139">NOTES</span></span>

## <span data-ttu-id="bae98-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bae98-140">RELATED LINKS</span></span>

[<span data-ttu-id="bae98-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bae98-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="bae98-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bae98-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="bae98-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="bae98-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


