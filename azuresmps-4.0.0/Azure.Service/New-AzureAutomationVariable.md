---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023889"
---
# <span data-ttu-id="73c73-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="73c73-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="73c73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73c73-102">SYNOPSIS</span></span>

<span data-ttu-id="73c73-103">Crea una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="73c73-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="73c73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73c73-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73c73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73c73-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="73c73-106">Il cmdlet **New-AzureAutomationVariable** crea una variabile in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="73c73-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="73c73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73c73-107">EXAMPLES</span></span>

### <span data-ttu-id="73c73-108">Esempio 1: creare una nuova variabile con un valore semplice</span><span class="sxs-lookup"><span data-stu-id="73c73-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="73c73-109">Questo comando crea una nuova variabile denominata MyStringVariable con un valore stringa nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="73c73-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="73c73-110">Esempio 2: creare una nuova variabile con un valore complesso</span><span class="sxs-lookup"><span data-stu-id="73c73-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="73c73-111">Questi comandi creano una nuova variabile denominata MyComplexVariable nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="73c73-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="73c73-112">Un oggetto complesso viene usato per il relativo valore, in questo caso un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="73c73-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="73c73-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73c73-113">PARAMETERS</span></span>

### <span data-ttu-id="73c73-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="73c73-114">-AutomationAccountName</span></span>
<span data-ttu-id="73c73-115">Specifica il nome dell'account di automazione in cui verrà archiviata la variabile.</span><span class="sxs-lookup"><span data-stu-id="73c73-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

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

### <span data-ttu-id="73c73-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="73c73-116">-Description</span></span>
<span data-ttu-id="73c73-117">Specifica una descrizione per la variabile.</span><span class="sxs-lookup"><span data-stu-id="73c73-117">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c73-118">-Crittografato</span><span class="sxs-lookup"><span data-stu-id="73c73-118">-Encrypted</span></span>
<span data-ttu-id="73c73-119">Indica se il valore della variabile deve essere archiviato come crittografato.</span><span class="sxs-lookup"><span data-stu-id="73c73-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c73-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73c73-120">-Name</span></span>
<span data-ttu-id="73c73-121">Specifica un nome per la variabile.</span><span class="sxs-lookup"><span data-stu-id="73c73-121">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="73c73-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="73c73-122">-Profile</span></span>
<span data-ttu-id="73c73-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73c73-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73c73-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="73c73-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="73c73-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="73c73-125">-Value</span></span>
<span data-ttu-id="73c73-126">Specifica un valore da archiviare nella variabile.</span><span class="sxs-lookup"><span data-stu-id="73c73-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c73-127">CommonParameters</span></span>
<span data-ttu-id="73c73-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c73-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c73-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c73-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73c73-130">INPUTS</span></span>

## <span data-ttu-id="73c73-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73c73-131">OUTPUTS</span></span>

### <span data-ttu-id="73c73-132">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="73c73-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="73c73-133">Note</span><span class="sxs-lookup"><span data-stu-id="73c73-133">NOTES</span></span>

## <span data-ttu-id="73c73-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73c73-134">RELATED LINKS</span></span>

[<span data-ttu-id="73c73-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="73c73-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="73c73-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="73c73-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="73c73-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="73c73-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


