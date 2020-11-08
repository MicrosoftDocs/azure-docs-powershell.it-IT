---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029631"
---
# <span data-ttu-id="6196c-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6196c-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="6196c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6196c-102">SYNOPSIS</span></span>

<span data-ttu-id="6196c-103">Rimuove una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="6196c-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="6196c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6196c-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6196c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6196c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6196c-106">Il cmdlet **Remove-AzureAutomationVariable** consente di rimuovere una variabile da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6196c-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6196c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6196c-107">EXAMPLES</span></span>

### <span data-ttu-id="6196c-108">Esempio 1: rimuovere una variabile</span><span class="sxs-lookup"><span data-stu-id="6196c-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="6196c-109">Questo comando rimuove una variabile denominata MyStringVariable nell'account di automazione denominata Contoso17 senza richiedere la convalida dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6196c-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="6196c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6196c-110">PARAMETERS</span></span>

### <span data-ttu-id="6196c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6196c-111">-AutomationAccountName</span></span>
<span data-ttu-id="6196c-112">Specifica il nome dell'account di automazione con la variabile.</span><span class="sxs-lookup"><span data-stu-id="6196c-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="6196c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6196c-113">-Force</span></span>
<span data-ttu-id="6196c-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6196c-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6196c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6196c-115">-Name</span></span>
<span data-ttu-id="6196c-116">Specifica il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="6196c-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="6196c-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="6196c-117">-Profile</span></span>
<span data-ttu-id="6196c-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6196c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6196c-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6196c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6196c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6196c-120">CommonParameters</span></span>
<span data-ttu-id="6196c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6196c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6196c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6196c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6196c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6196c-123">INPUTS</span></span>

## <span data-ttu-id="6196c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6196c-124">OUTPUTS</span></span>

## <span data-ttu-id="6196c-125">Note</span><span class="sxs-lookup"><span data-stu-id="6196c-125">NOTES</span></span>

## <span data-ttu-id="6196c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6196c-126">RELATED LINKS</span></span>

[<span data-ttu-id="6196c-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6196c-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="6196c-128">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6196c-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="6196c-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6196c-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


