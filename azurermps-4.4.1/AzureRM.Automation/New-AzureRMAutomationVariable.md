---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: c2e03cae02c776b69c424ea3ff685a4118ed94bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518411"
---
# <span data-ttu-id="4491d-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4491d-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="4491d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4491d-102">SYNOPSIS</span></span>
<span data-ttu-id="4491d-103">Crea una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="4491d-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4491d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4491d-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4491d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4491d-105">DESCRIPTION</span></span>
<span data-ttu-id="4491d-106">Il cmdlet **New-AzureRmAutomationVariable** crea una variabile in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4491d-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="4491d-107">Per crittografare la variabile, specificare il parametro *crittografato* .</span><span class="sxs-lookup"><span data-stu-id="4491d-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="4491d-108">Non è possibile modificare lo stato crittografato di una variabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="4491d-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="4491d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4491d-109">EXAMPLES</span></span>

### <span data-ttu-id="4491d-110">Esempio 1: creare una variabile con un valore semplice</span><span class="sxs-lookup"><span data-stu-id="4491d-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4491d-111">Questo comando crea una variabile denominata StringVariable22 con un valore stringa nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4491d-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4491d-112">Esempio 2: creare una variabile con un valore complesso</span><span class="sxs-lookup"><span data-stu-id="4491d-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4491d-113">Il primo comando Recupera una macchina virtuale usando il cmdlet Get-AzureVM.</span><span class="sxs-lookup"><span data-stu-id="4491d-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="4491d-114">Il comando lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4491d-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4491d-115">Il secondo comando crea una variabile denominata ComplexVariable01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4491d-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4491d-116">Questo comando usa un oggetto complesso per il relativo valore, in questo caso la macchina virtuale in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4491d-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="4491d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4491d-117">PARAMETERS</span></span>

### <span data-ttu-id="4491d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4491d-118">-AutomationAccountName</span></span>
<span data-ttu-id="4491d-119">Specifica il nome dell'account di automazione in cui archiviare la variabile.</span><span class="sxs-lookup"><span data-stu-id="4491d-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="4491d-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4491d-120">-Description</span></span>
<span data-ttu-id="4491d-121">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="4491d-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="4491d-122">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="4491d-122">-Encrypted</span></span>
<span data-ttu-id="4491d-123">Specifica se questo cmdlet crittografa il valore della variabile per lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4491d-123">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="4491d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4491d-124">-Name</span></span>
<span data-ttu-id="4491d-125">Specifica un nome per la variabile.</span><span class="sxs-lookup"><span data-stu-id="4491d-125">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="4491d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4491d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4491d-127">Specifica il gruppo di risorse per cui questo cmdlet crea una variabile.</span><span class="sxs-lookup"><span data-stu-id="4491d-127">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="4491d-128">-Valore</span><span class="sxs-lookup"><span data-stu-id="4491d-128">-Value</span></span>
<span data-ttu-id="4491d-129">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="4491d-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="4491d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4491d-130">-DefaultProfile</span></span>
<span data-ttu-id="4491d-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4491d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4491d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4491d-132">CommonParameters</span></span>
<span data-ttu-id="4491d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4491d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4491d-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4491d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4491d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4491d-135">INPUTS</span></span>

## <span data-ttu-id="4491d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4491d-136">OUTPUTS</span></span>

### <span data-ttu-id="4491d-137">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="4491d-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="4491d-138">Note</span><span class="sxs-lookup"><span data-stu-id="4491d-138">NOTES</span></span>

## <span data-ttu-id="4491d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4491d-139">RELATED LINKS</span></span>

[<span data-ttu-id="4491d-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4491d-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="4491d-141">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4491d-141">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="4491d-142">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4491d-142">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


