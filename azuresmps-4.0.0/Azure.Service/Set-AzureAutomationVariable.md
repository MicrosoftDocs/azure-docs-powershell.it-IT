---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029530"
---
# <span data-ttu-id="d8a73-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d8a73-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="d8a73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8a73-102">SYNOPSIS</span></span>

<span data-ttu-id="d8a73-103">Modifica una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="d8a73-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="d8a73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8a73-104">SYNTAX</span></span>

### <span data-ttu-id="d8a73-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="d8a73-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8a73-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="d8a73-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8a73-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8a73-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d8a73-108">Il cmdlet **set-AzureAutomationVariable** modifica il valore o la descrizione di una variabile in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d8a73-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d8a73-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8a73-109">EXAMPLES</span></span>

### <span data-ttu-id="d8a73-110">Esempio 1: impostare il valore di una variabile</span><span class="sxs-lookup"><span data-stu-id="d8a73-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="d8a73-111">Questo comando imposta un nuovo valore per la variabile denominata MyStringVariable nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d8a73-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d8a73-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8a73-112">PARAMETERS</span></span>

### <span data-ttu-id="d8a73-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8a73-113">-AutomationAccountName</span></span>
<span data-ttu-id="d8a73-114">Specifica il nome dell'account di automazione con la variabile.</span><span class="sxs-lookup"><span data-stu-id="d8a73-114">Specifies the name of the Automation account with the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a73-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8a73-115">-Description</span></span>
<span data-ttu-id="d8a73-116">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="d8a73-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a73-117">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="d8a73-117">-Encrypted</span></span>
<span data-ttu-id="d8a73-118">Indica se crittografare la variabile.</span><span class="sxs-lookup"><span data-stu-id="d8a73-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a73-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8a73-119">-Name</span></span>
<span data-ttu-id="d8a73-120">Specifica il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="d8a73-120">Specifies the name of the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a73-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="d8a73-121">-Profile</span></span>
<span data-ttu-id="d8a73-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8a73-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8a73-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d8a73-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a73-124">-Valore</span><span class="sxs-lookup"><span data-stu-id="d8a73-124">-Value</span></span>
<span data-ttu-id="d8a73-125">Specifica un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="d8a73-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8a73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a73-126">CommonParameters</span></span>
<span data-ttu-id="d8a73-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a73-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a73-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a73-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8a73-129">INPUTS</span></span>

## <span data-ttu-id="d8a73-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8a73-130">OUTPUTS</span></span>

### <span data-ttu-id="d8a73-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="d8a73-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="d8a73-132">Note</span><span class="sxs-lookup"><span data-stu-id="d8a73-132">NOTES</span></span>

## <span data-ttu-id="d8a73-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8a73-133">RELATED LINKS</span></span>

[<span data-ttu-id="d8a73-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d8a73-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="d8a73-135">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d8a73-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="d8a73-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d8a73-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


