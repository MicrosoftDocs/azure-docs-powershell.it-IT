---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 462566749ce0c55d4f892cc19e362f62b6fd0fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507655"
---
# <span data-ttu-id="93ff9-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93ff9-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="93ff9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="93ff9-103">Modifica una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="93ff9-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ff9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93ff9-104">SYNTAX</span></span>

### <span data-ttu-id="93ff9-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="93ff9-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93ff9-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="93ff9-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93ff9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93ff9-107">DESCRIPTION</span></span>
<span data-ttu-id="93ff9-108">Il cmdlet **set-AzureRmAutomationVariable** modifica il valore o la descrizione di una variabile in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="93ff9-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="93ff9-109">Per crittografare la variabile, specificare il parametro *crittografato* .</span><span class="sxs-lookup"><span data-stu-id="93ff9-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="93ff9-110">Non è possibile modificare lo stato crittografato di una variabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="93ff9-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="93ff9-111">Se si specifica *crittografato* per una variabile esistente non crittografata, non riesce.</span><span class="sxs-lookup"><span data-stu-id="93ff9-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="93ff9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93ff9-112">EXAMPLES</span></span>

### <span data-ttu-id="93ff9-113">Esempio 1: impostare il valore di una variabile</span><span class="sxs-lookup"><span data-stu-id="93ff9-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="93ff9-114">Questo comando imposta un nuovo valore per la variabile denominata StringVariable22 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="93ff9-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="93ff9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93ff9-115">PARAMETERS</span></span>

### <span data-ttu-id="93ff9-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93ff9-116">-AutomationAccountName</span></span>
<span data-ttu-id="93ff9-117">Specifica il nome dell'account di automazione in cui è archiviata la variabile.</span><span class="sxs-lookup"><span data-stu-id="93ff9-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="93ff9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ff9-118">-DefaultProfile</span></span>
<span data-ttu-id="93ff9-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93ff9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93ff9-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="93ff9-120">-Description</span></span>
<span data-ttu-id="93ff9-121">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="93ff9-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="93ff9-122">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="93ff9-122">-Encrypted</span></span>
<span data-ttu-id="93ff9-123">Specifica se il cmdlet crittografa il valore della variabile per lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93ff9-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="93ff9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="93ff9-124">-Name</span></span>
<span data-ttu-id="93ff9-125">Specifica il nome della variabile che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="93ff9-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="93ff9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ff9-126">-ResourceGroupName</span></span>
<span data-ttu-id="93ff9-127">Specifica il gruppo di risorse per cui questo cmdlet modifica una variabile.</span><span class="sxs-lookup"><span data-stu-id="93ff9-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="93ff9-128">-Valore</span><span class="sxs-lookup"><span data-stu-id="93ff9-128">-Value</span></span>
<span data-ttu-id="93ff9-129">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="93ff9-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="93ff9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ff9-130">CommonParameters</span></span>
<span data-ttu-id="93ff9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ff9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ff9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ff9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ff9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93ff9-133">INPUTS</span></span>

### <span data-ttu-id="93ff9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="93ff9-134">System.String</span></span>

### <span data-ttu-id="93ff9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93ff9-135">System.Boolean</span></span>

### <span data-ttu-id="93ff9-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="93ff9-136">System.Object</span></span>

## <span data-ttu-id="93ff9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93ff9-137">OUTPUTS</span></span>

### <span data-ttu-id="93ff9-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="93ff9-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="93ff9-139">Note</span><span class="sxs-lookup"><span data-stu-id="93ff9-139">NOTES</span></span>

## <span data-ttu-id="93ff9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93ff9-140">RELATED LINKS</span></span>

[<span data-ttu-id="93ff9-141">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93ff9-141">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="93ff9-142">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93ff9-142">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="93ff9-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="93ff9-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


