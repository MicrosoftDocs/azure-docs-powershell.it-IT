---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 96e7be91319713ca17f6ad443596316513d2bfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511363"
---
# <span data-ttu-id="8cf6a-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8cf6a-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="8cf6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf6a-103">Modifica una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cf6a-104">SYNTAX</span></span>

### <span data-ttu-id="8cf6a-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="8cf6a-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cf6a-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="8cf6a-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cf6a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf6a-107">DESCRIPTION</span></span>
<span data-ttu-id="8cf6a-108">Il cmdlet **set-AzureRmAutomationVariable** modifica il valore o la descrizione di una variabile in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="8cf6a-109">Per crittografare la variabile, specificare il parametro *crittografato* .</span><span class="sxs-lookup"><span data-stu-id="8cf6a-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="8cf6a-110">Non è possibile modificare lo stato crittografato di una variabile dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="8cf6a-111">Se si specifica *crittografato* per una variabile esistente non crittografata, non riesce.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="8cf6a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cf6a-112">EXAMPLES</span></span>

### <span data-ttu-id="8cf6a-113">Esempio 1: impostare il valore di una variabile</span><span class="sxs-lookup"><span data-stu-id="8cf6a-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="8cf6a-114">Questo comando imposta un nuovo valore per la variabile denominata StringVariable22 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8cf6a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cf6a-115">PARAMETERS</span></span>

### <span data-ttu-id="8cf6a-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8cf6a-116">-AutomationAccountName</span></span>
<span data-ttu-id="8cf6a-117">Specifica il nome dell'account di automazione in cui è archiviata la variabile.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="8cf6a-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf6a-118">-Description</span></span>
<span data-ttu-id="8cf6a-119">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-119">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="8cf6a-120">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="8cf6a-120">-Encrypted</span></span>
<span data-ttu-id="8cf6a-121">Specifica se il cmdlet crittografa il valore della variabile per lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-121">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="8cf6a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cf6a-122">-Name</span></span>
<span data-ttu-id="8cf6a-123">Specifica il nome della variabile che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-123">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8cf6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cf6a-125">Specifica il gruppo di risorse per cui questo cmdlet modifica una variabile.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-125">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="8cf6a-126">-Valore</span><span class="sxs-lookup"><span data-stu-id="8cf6a-126">-Value</span></span>
<span data-ttu-id="8cf6a-127">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-127">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="8cf6a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf6a-128">-DefaultProfile</span></span>
<span data-ttu-id="8cf6a-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cf6a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf6a-130">CommonParameters</span></span>
<span data-ttu-id="8cf6a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf6a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf6a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf6a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf6a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cf6a-133">INPUTS</span></span>

## <span data-ttu-id="8cf6a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cf6a-134">OUTPUTS</span></span>

### <span data-ttu-id="8cf6a-135">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="8cf6a-135">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="8cf6a-136">Note</span><span class="sxs-lookup"><span data-stu-id="8cf6a-136">NOTES</span></span>

## <span data-ttu-id="8cf6a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cf6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8cf6a-138">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8cf6a-138">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="8cf6a-139">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8cf6a-139">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="8cf6a-140">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8cf6a-140">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


