---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029633"
---
# <span data-ttu-id="26104-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="26104-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="26104-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26104-102">SYNOPSIS</span></span>

<span data-ttu-id="26104-103">Rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="26104-103">Removes a runbook.</span></span>

## <span data-ttu-id="26104-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26104-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26104-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26104-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="26104-106">Il cmdlet **Remove-AzureAutomationRunbook** rimuove un Runbook da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="26104-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="26104-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26104-107">EXAMPLES</span></span>

### <span data-ttu-id="26104-108">Esempio 1: rimuovere un Runbook</span><span class="sxs-lookup"><span data-stu-id="26104-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="26104-109">Questo comando rimuove il Runbook denominato MyRunbook nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="26104-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="26104-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26104-110">PARAMETERS</span></span>

### <span data-ttu-id="26104-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="26104-111">-AutomationAccountName</span></span>
<span data-ttu-id="26104-112">Specifica il nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="26104-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="26104-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26104-113">-Force</span></span>
<span data-ttu-id="26104-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="26104-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26104-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="26104-115">-Name</span></span>
<span data-ttu-id="26104-116">Specifica il nome del Runbook da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26104-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26104-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="26104-117">-Profile</span></span>
<span data-ttu-id="26104-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26104-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="26104-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="26104-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26104-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26104-120">-Confirm</span></span>
<span data-ttu-id="26104-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26104-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26104-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26104-122">-WhatIf</span></span>
<span data-ttu-id="26104-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26104-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26104-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26104-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26104-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26104-125">CommonParameters</span></span>
<span data-ttu-id="26104-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26104-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26104-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26104-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26104-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26104-128">INPUTS</span></span>

## <span data-ttu-id="26104-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26104-129">OUTPUTS</span></span>

## <span data-ttu-id="26104-130">Note</span><span class="sxs-lookup"><span data-stu-id="26104-130">NOTES</span></span>

## <span data-ttu-id="26104-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26104-131">RELATED LINKS</span></span>

[<span data-ttu-id="26104-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="26104-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="26104-133">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="26104-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="26104-134">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="26104-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="26104-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="26104-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="26104-136">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="26104-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


