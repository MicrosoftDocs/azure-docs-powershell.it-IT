---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029943"
---
# <span data-ttu-id="26165-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="26165-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="26165-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26165-102">SYNOPSIS</span></span>

<span data-ttu-id="26165-103">Rimuove un modulo dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="26165-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="26165-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26165-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26165-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26165-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="26165-106">Il cmdlet **Remove-AzureAutomationModule** rimuove un account di automazione da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="26165-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="26165-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26165-107">EXAMPLES</span></span>

### <span data-ttu-id="26165-108">Esempio 1: rimuovere un modulo</span><span class="sxs-lookup"><span data-stu-id="26165-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="26165-109">Questo comando rimuove un modulo denominato ContosoModule dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="26165-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="26165-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26165-110">PARAMETERS</span></span>

### <span data-ttu-id="26165-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="26165-111">-AutomationAccountName</span></span>
<span data-ttu-id="26165-112">Specifica il nome dell'account di automazione con il modulo.</span><span class="sxs-lookup"><span data-stu-id="26165-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="26165-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26165-113">-Force</span></span>
<span data-ttu-id="26165-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="26165-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26165-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="26165-115">-Name</span></span>
<span data-ttu-id="26165-116">Specifica il nome del modulo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26165-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="26165-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="26165-117">-Profile</span></span>
<span data-ttu-id="26165-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26165-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26165-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="26165-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26165-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26165-120">CommonParameters</span></span>
<span data-ttu-id="26165-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26165-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26165-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26165-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26165-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26165-123">INPUTS</span></span>

## <span data-ttu-id="26165-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26165-124">OUTPUTS</span></span>

## <span data-ttu-id="26165-125">Note</span><span class="sxs-lookup"><span data-stu-id="26165-125">NOTES</span></span>

## <span data-ttu-id="26165-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26165-126">RELATED LINKS</span></span>

[<span data-ttu-id="26165-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="26165-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="26165-128">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="26165-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="26165-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="26165-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


