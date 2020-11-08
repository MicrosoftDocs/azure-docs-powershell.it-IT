---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030049"
---
# <span data-ttu-id="cae8c-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="cae8c-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="cae8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cae8c-102">SYNOPSIS</span></span>

<span data-ttu-id="cae8c-103">Rimuove un'associazione tra un Runbook e una programmazione.</span><span class="sxs-lookup"><span data-stu-id="cae8c-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="cae8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cae8c-104">SYNTAX</span></span>

### <span data-ttu-id="cae8c-105">ByJobScheduleId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cae8c-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cae8c-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="cae8c-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cae8c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cae8c-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cae8c-108">Il cmdlet **Unregister-AzureAutomationScheduledRunbook** rimuove l'associazione tra un Runbook di automazione di Microsoft Azure e una programmazione, che impedisce l'avvio di runbook quando la programmazione viene attivata.</span><span class="sxs-lookup"><span data-stu-id="cae8c-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="cae8c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cae8c-109">EXAMPLES</span></span>

### <span data-ttu-id="cae8c-110">Esempio 1: rimuovere l'associazione tra un Runbook e una programmazione</span><span class="sxs-lookup"><span data-stu-id="cae8c-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="cae8c-111">Questo comando rimuove l'associazione tra Runbook denominata Runbk01 e la pianificazione denominata Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="cae8c-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="cae8c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cae8c-112">PARAMETERS</span></span>

### <span data-ttu-id="cae8c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cae8c-113">-AutomationAccountName</span></span>
<span data-ttu-id="cae8c-114">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="cae8c-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="cae8c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cae8c-115">-Force</span></span>
<span data-ttu-id="cae8c-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cae8c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cae8c-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="cae8c-117">-JobScheduleId</span></span>
<span data-ttu-id="cae8c-118">Specifica l'ID di un Runbook programmato.</span><span class="sxs-lookup"><span data-stu-id="cae8c-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae8c-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="cae8c-119">-Profile</span></span>
<span data-ttu-id="cae8c-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae8c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cae8c-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cae8c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cae8c-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="cae8c-122">-RunbookName</span></span>
<span data-ttu-id="cae8c-123">Specifica il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="cae8c-123">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae8c-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="cae8c-124">-ScheduleName</span></span>
<span data-ttu-id="cae8c-125">Specifica il nome di una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cae8c-125">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae8c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae8c-126">CommonParameters</span></span>
<span data-ttu-id="cae8c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae8c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae8c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae8c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae8c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cae8c-129">INPUTS</span></span>

## <span data-ttu-id="cae8c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cae8c-130">OUTPUTS</span></span>

## <span data-ttu-id="cae8c-131">Note</span><span class="sxs-lookup"><span data-stu-id="cae8c-131">NOTES</span></span>

## <span data-ttu-id="cae8c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cae8c-132">RELATED LINKS</span></span>

[<span data-ttu-id="cae8c-133">Registro-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="cae8c-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


