---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: f60e254e9addf2e7052b010033d9c81ccc6a0a98
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373435"
---
# <span data-ttu-id="f9fb5-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f9fb5-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="f9fb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fb5-103">Crea una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="f9fb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9fb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fb5-106">Il cmdlet **New-AzAutomationVariable** crea una variabile in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="f9fb5-107">Per crittografare la variabile, specificare il parametro *crittografato* .</span><span class="sxs-lookup"><span data-stu-id="f9fb5-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="f9fb5-108">Non è possibile modificare lo stato crittografato di una variabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="f9fb5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-109">EXAMPLES</span></span>

### <span data-ttu-id="f9fb5-110">Esempio 1: creare una variabile con un valore semplice</span><span class="sxs-lookup"><span data-stu-id="f9fb5-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f9fb5-111">Questo comando crea una variabile denominata StringVariable22 con un valore stringa nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f9fb5-112">Esempio 2: creare una variabile con un valore complesso</span><span class="sxs-lookup"><span data-stu-id="f9fb5-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f9fb5-113">Il primo comando Recupera una macchina virtuale usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="f9fb5-114">Il comando lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f9fb5-115">Il secondo comando crea una variabile denominata ComplexVariable01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f9fb5-116">Questo comando usa un oggetto complesso per il relativo valore, in questo caso la macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="f9fb5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-117">PARAMETERS</span></span>

### <span data-ttu-id="f9fb5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f9fb5-118">-AutomationAccountName</span></span>
<span data-ttu-id="f9fb5-119">Specifica il nome dell'account di automazione in cui archiviare la variabile.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="f9fb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fb5-120">-DefaultProfile</span></span>
<span data-ttu-id="f9fb5-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f9fb5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9fb5-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9fb5-122">-Description</span></span>
<span data-ttu-id="f9fb5-123">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb5-124">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="f9fb5-124">-Encrypted</span></span>
<span data-ttu-id="f9fb5-125">Specifica se questo cmdlet crittografa il valore della variabile per lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9fb5-126">-Name</span></span>
<span data-ttu-id="f9fb5-127">Specifica un nome per la variabile.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="f9fb5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9fb5-128">-ResourceGroupName</span></span>
<span data-ttu-id="f9fb5-129">Specifica il gruppo di risorse per cui questo cmdlet crea una variabile.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="f9fb5-130">-Valore</span><span class="sxs-lookup"><span data-stu-id="f9fb5-130">-Value</span></span>
<span data-ttu-id="f9fb5-131">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fb5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fb5-132">CommonParameters</span></span>
<span data-ttu-id="f9fb5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fb5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fb5-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fb5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fb5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-135">INPUTS</span></span>

### <span data-ttu-id="f9fb5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f9fb5-136">System.String</span></span>

### <span data-ttu-id="f9fb5-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9fb5-137">System.Boolean</span></span>

### <span data-ttu-id="f9fb5-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="f9fb5-138">System.Object</span></span>

## <span data-ttu-id="f9fb5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9fb5-139">OUTPUTS</span></span>

### <span data-ttu-id="f9fb5-140">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="f9fb5-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f9fb5-141">Note</span><span class="sxs-lookup"><span data-stu-id="f9fb5-141">NOTES</span></span>

## <span data-ttu-id="f9fb5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9fb5-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9fb5-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f9fb5-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="f9fb5-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f9fb5-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="f9fb5-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f9fb5-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


