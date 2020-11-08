---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023611"
---
# <span data-ttu-id="0e559-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0e559-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="0e559-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e559-102">SYNOPSIS</span></span>

<span data-ttu-id="0e559-103">Ottiene una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="0e559-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="0e559-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e559-104">SYNTAX</span></span>

### <span data-ttu-id="0e559-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e559-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0e559-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0e559-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e559-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e559-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0e559-108">Il cmdlet **Get-AzureAutomationVariable** ottiene una o più variabili di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0e559-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="0e559-109">Per impostazione predefinita, vengono restituite tutte le variabili.</span><span class="sxs-lookup"><span data-stu-id="0e559-109">By default, all variables are returned.</span></span>
<span data-ttu-id="0e559-110">Per ottenere una variabile specifica, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="0e559-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="0e559-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e559-111">EXAMPLES</span></span>

### <span data-ttu-id="0e559-112">Esempio 1: ottenere una variabile</span><span class="sxs-lookup"><span data-stu-id="0e559-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="0e559-113">Questi comandi ottengono una variabile di automazione denominata variabile e assegnano il relativo valore a una variabile denominata $value.</span><span class="sxs-lookup"><span data-stu-id="0e559-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="0e559-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e559-114">PARAMETERS</span></span>

### <span data-ttu-id="0e559-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e559-115">-AutomationAccountName</span></span>
<span data-ttu-id="0e559-116">Specifica il nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="0e559-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="0e559-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e559-117">-Name</span></span>
<span data-ttu-id="0e559-118">Specifica il nome di una variabile.</span><span class="sxs-lookup"><span data-stu-id="0e559-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e559-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="0e559-119">-Profile</span></span>
<span data-ttu-id="0e559-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e559-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e559-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0e559-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0e559-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e559-122">CommonParameters</span></span>
<span data-ttu-id="0e559-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e559-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e559-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e559-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e559-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e559-125">INPUTS</span></span>

## <span data-ttu-id="0e559-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e559-126">OUTPUTS</span></span>

### <span data-ttu-id="0e559-127">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="0e559-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0e559-128">Note</span><span class="sxs-lookup"><span data-stu-id="0e559-128">NOTES</span></span>

## <span data-ttu-id="0e559-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e559-129">RELATED LINKS</span></span>

[<span data-ttu-id="0e559-130">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0e559-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="0e559-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0e559-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="0e559-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0e559-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


