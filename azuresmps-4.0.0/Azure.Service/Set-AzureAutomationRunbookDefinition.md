---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029532"
---
# <span data-ttu-id="34b46-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="34b46-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="34b46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34b46-102">SYNOPSIS</span></span>

<span data-ttu-id="34b46-103">Aggiorna la definizione bozza di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="34b46-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="34b46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34b46-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34b46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34b46-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="34b46-106">Il cmdlet **set-AzureAutomationRunbookDefinition** aggiorna la definizione bozza di un Runbook di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34b46-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="34b46-107">Specifica un file di script di Windows PowerShell (con estensione ps1) che contiene un Runbook che diventa la bozza di Runbook.</span><span class="sxs-lookup"><span data-stu-id="34b46-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="34b46-108">Se una bozza di definizione esiste già, usare il parametro *overwrite* per forzare il cmdlet a sovrascrivere la bozza esistente.</span><span class="sxs-lookup"><span data-stu-id="34b46-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="34b46-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34b46-109">EXAMPLES</span></span>

### <span data-ttu-id="34b46-110">Esempio 1: sovrascrivere una definizione di bozza esistente di un Runbook</span><span class="sxs-lookup"><span data-stu-id="34b46-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="34b46-111">Questo comando sovrascrive la definizione di bozza esistente di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="34b46-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="34b46-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34b46-112">PARAMETERS</span></span>

### <span data-ttu-id="34b46-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34b46-113">-AutomationAccountName</span></span>
<span data-ttu-id="34b46-114">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="34b46-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="34b46-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="34b46-115">-Name</span></span>
<span data-ttu-id="34b46-116">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="34b46-116">Specifies a name.</span></span>

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

### <span data-ttu-id="34b46-117">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="34b46-117">-Overwrite</span></span>
<span data-ttu-id="34b46-118">Indica se sovrascrivere una definizione di bozza esistente.</span><span class="sxs-lookup"><span data-stu-id="34b46-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b46-119">-Path</span><span class="sxs-lookup"><span data-stu-id="34b46-119">-Path</span></span>
<span data-ttu-id="34b46-120">Specifica il percorso di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="34b46-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34b46-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="34b46-121">-Profile</span></span>
<span data-ttu-id="34b46-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34b46-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34b46-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="34b46-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34b46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b46-124">CommonParameters</span></span>
<span data-ttu-id="34b46-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34b46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b46-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b46-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b46-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34b46-127">INPUTS</span></span>

## <span data-ttu-id="34b46-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34b46-128">OUTPUTS</span></span>

### <span data-ttu-id="34b46-129">Microsoft. Azure. Commands. Automation. Model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="34b46-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="34b46-130">Note</span><span class="sxs-lookup"><span data-stu-id="34b46-130">NOTES</span></span>

## <span data-ttu-id="34b46-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34b46-131">RELATED LINKS</span></span>

[<span data-ttu-id="34b46-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="34b46-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


