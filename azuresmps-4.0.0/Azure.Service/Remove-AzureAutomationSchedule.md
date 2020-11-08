---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029632"
---
# <span data-ttu-id="754b5-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="754b5-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="754b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="754b5-102">SYNOPSIS</span></span>

<span data-ttu-id="754b5-103">Elimina una pianificazione di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="754b5-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="754b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="754b5-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="754b5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="754b5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="754b5-106">Il cmdlet **Remove-AzureAutomationSchedule** Elimina una programmazione da Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="754b5-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="754b5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="754b5-107">EXAMPLES</span></span>

### <span data-ttu-id="754b5-108">Esempio 1: rimuovere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="754b5-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="754b5-109">Questo comando rimuove la pianificazione denominata programmazione.</span><span class="sxs-lookup"><span data-stu-id="754b5-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="754b5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="754b5-110">PARAMETERS</span></span>

### <span data-ttu-id="754b5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="754b5-111">-AutomationAccountName</span></span>
<span data-ttu-id="754b5-112">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="754b5-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="754b5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="754b5-113">-Force</span></span>
<span data-ttu-id="754b5-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="754b5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="754b5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="754b5-115">-Name</span></span>
<span data-ttu-id="754b5-116">Specifica il nome della programmazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="754b5-116">Specifies the name of the schedule to remove.</span></span>

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

### <span data-ttu-id="754b5-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="754b5-117">-Profile</span></span>
<span data-ttu-id="754b5-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754b5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="754b5-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="754b5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="754b5-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="754b5-120">-Confirm</span></span>
<span data-ttu-id="754b5-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="754b5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="754b5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="754b5-122">-WhatIf</span></span>
<span data-ttu-id="754b5-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="754b5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="754b5-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="754b5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="754b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754b5-125">CommonParameters</span></span>
<span data-ttu-id="754b5-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="754b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754b5-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="754b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754b5-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="754b5-128">INPUTS</span></span>

## <span data-ttu-id="754b5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="754b5-129">OUTPUTS</span></span>

## <span data-ttu-id="754b5-130">Note</span><span class="sxs-lookup"><span data-stu-id="754b5-130">NOTES</span></span>

## <span data-ttu-id="754b5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="754b5-131">RELATED LINKS</span></span>

[<span data-ttu-id="754b5-132">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="754b5-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="754b5-133">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="754b5-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="754b5-134">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="754b5-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


