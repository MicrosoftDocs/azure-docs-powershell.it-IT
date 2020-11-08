---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023892"
---
# <span data-ttu-id="03b49-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="03b49-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="03b49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03b49-102">SYNOPSIS</span></span>

<span data-ttu-id="03b49-103">Crea un Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-103">Creates a runbook.</span></span>

## <span data-ttu-id="03b49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03b49-104">SYNTAX</span></span>

### <span data-ttu-id="03b49-105">ByRunbookName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03b49-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="03b49-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="03b49-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="03b49-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b49-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="03b49-108">Il cmdlet **New-AzureAutomationRunbook** crea un nuovo Runbook di automazione di Microsoft Azure vuoto.</span><span class="sxs-lookup"><span data-stu-id="03b49-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="03b49-109">Specificare un nome per creare un nuovo Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="03b49-110">Puoi anche specificare il percorso di un file di script di Windows PowerShell (con estensione ps1) per importare un Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="03b49-111">Lo script da importare deve contenere una singola definizione del flusso di lavoro di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="03b49-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="03b49-112">Il nome di questo flusso di lavoro di Windows PowerShell diventa il nome di Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="03b49-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03b49-113">EXAMPLES</span></span>

### <span data-ttu-id="03b49-114">Esempio 1: creare un Runbook</span><span class="sxs-lookup"><span data-stu-id="03b49-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="03b49-115">Questo comando crea un nuovo Runbook denominato Runbook02 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="03b49-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="03b49-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03b49-116">PARAMETERS</span></span>

### <span data-ttu-id="03b49-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03b49-117">-AutomationAccountName</span></span>
<span data-ttu-id="03b49-118">Specifica il nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="03b49-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="03b49-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b49-119">-Description</span></span>
<span data-ttu-id="03b49-120">Specifica una descrizione per Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="03b49-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="03b49-121">-Name</span></span>
<span data-ttu-id="03b49-122">Specifica il nome per Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b49-123">-Path</span><span class="sxs-lookup"><span data-stu-id="03b49-123">-Path</span></span>
<span data-ttu-id="03b49-124">Specifica il percorso.</span><span class="sxs-lookup"><span data-stu-id="03b49-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b49-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="03b49-125">-Profile</span></span>
<span data-ttu-id="03b49-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03b49-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="03b49-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="03b49-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="03b49-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="03b49-128">-Tags</span></span>
<span data-ttu-id="03b49-129">Specifica i contrassegni per Runbook.</span><span class="sxs-lookup"><span data-stu-id="03b49-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b49-130">CommonParameters</span></span>
<span data-ttu-id="03b49-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b49-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b49-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b49-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03b49-133">INPUTS</span></span>

## <span data-ttu-id="03b49-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03b49-134">OUTPUTS</span></span>

### <span data-ttu-id="03b49-135">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="03b49-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="03b49-136">Note</span><span class="sxs-lookup"><span data-stu-id="03b49-136">NOTES</span></span>

## <span data-ttu-id="03b49-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03b49-137">RELATED LINKS</span></span>

[<span data-ttu-id="03b49-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="03b49-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="03b49-139">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="03b49-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="03b49-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="03b49-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="03b49-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="03b49-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="03b49-142">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="03b49-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


