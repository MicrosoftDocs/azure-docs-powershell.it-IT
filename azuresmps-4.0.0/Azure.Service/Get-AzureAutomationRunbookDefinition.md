---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029824"
---
# <span data-ttu-id="a77e6-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="a77e6-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="a77e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a77e6-102">SYNOPSIS</span></span>

<span data-ttu-id="a77e6-103">Ottiene una definizione Runbook.</span><span class="sxs-lookup"><span data-stu-id="a77e6-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="a77e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a77e6-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a77e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a77e6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a77e6-106">Il cmdlet **Get-AzureAutomationRunbookDefinition** ottiene la definizione bozza, la definizione pubblicata o entrambe le definizioni di un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a77e6-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="a77e6-107">Per impostazione predefinita, viene restituita la versione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="a77e6-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="a77e6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a77e6-108">EXAMPLES</span></span>

### <span data-ttu-id="a77e6-109">Esempio 1: ottenere una definizione di Runbook</span><span class="sxs-lookup"><span data-stu-id="a77e6-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="a77e6-110">Questo comando ottiene la definizione Runbook pubblicata di Runbook denominata RunbookDef01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a77e6-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a77e6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a77e6-111">PARAMETERS</span></span>

### <span data-ttu-id="a77e6-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a77e6-112">-AutomationAccountName</span></span>
<span data-ttu-id="a77e6-113">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a77e6-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="a77e6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a77e6-114">-Name</span></span>
<span data-ttu-id="a77e6-115">Specifica il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a77e6-115">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="a77e6-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="a77e6-116">-Profile</span></span>
<span data-ttu-id="a77e6-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a77e6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a77e6-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a77e6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a77e6-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a77e6-119">-Slot</span></span>
<span data-ttu-id="a77e6-120">Specifica lo slot.</span><span class="sxs-lookup"><span data-stu-id="a77e6-120">Specifies the slot.</span></span>
<span data-ttu-id="a77e6-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a77e6-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a77e6-122">Progetto</span><span class="sxs-lookup"><span data-stu-id="a77e6-122">Draft</span></span>
- <span data-ttu-id="a77e6-123">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="a77e6-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a77e6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77e6-124">CommonParameters</span></span>
<span data-ttu-id="a77e6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a77e6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77e6-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a77e6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77e6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a77e6-127">INPUTS</span></span>

## <span data-ttu-id="a77e6-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a77e6-128">OUTPUTS</span></span>

## <span data-ttu-id="a77e6-129">Note</span><span class="sxs-lookup"><span data-stu-id="a77e6-129">NOTES</span></span>

## <span data-ttu-id="a77e6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a77e6-130">RELATED LINKS</span></span>

[<span data-ttu-id="a77e6-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="a77e6-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


