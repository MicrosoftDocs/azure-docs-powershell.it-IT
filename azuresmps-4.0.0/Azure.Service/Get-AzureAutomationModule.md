---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029830"
---
# <span data-ttu-id="67f3f-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="67f3f-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="67f3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67f3f-102">SYNOPSIS</span></span>

<span data-ttu-id="67f3f-103">Ottenere un modulo di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67f3f-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="67f3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67f3f-104">SYNTAX</span></span>

### <span data-ttu-id="67f3f-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67f3f-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="67f3f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="67f3f-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f3f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67f3f-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="67f3f-108">Il cmdlet **Get-AzureAutomationModule** ottiene uno o più moduli di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67f3f-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="67f3f-109">Per impostazione predefinita, vengono restituiti tutti i moduli.</span><span class="sxs-lookup"><span data-stu-id="67f3f-109">By default, all modules are returned.</span></span>
<span data-ttu-id="67f3f-110">Per ottenere un modulo specifico, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="67f3f-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="67f3f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67f3f-111">EXAMPLES</span></span>

### <span data-ttu-id="67f3f-112">Esempio 1: ottenere tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="67f3f-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="67f3f-113">Questo comando consente di ottenere tutti i moduli nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="67f3f-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="67f3f-114">Esempio 2: ottenere un modulo</span><span class="sxs-lookup"><span data-stu-id="67f3f-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="67f3f-115">Questo comando ottiene un modulo denominato ContosoModule nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="67f3f-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="67f3f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67f3f-116">PARAMETERS</span></span>

### <span data-ttu-id="67f3f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67f3f-117">-AutomationAccountName</span></span>
<span data-ttu-id="67f3f-118">Specifica il nome dell'account di automazione con Runbook da recuperare.</span><span class="sxs-lookup"><span data-stu-id="67f3f-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="67f3f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="67f3f-119">-Name</span></span>
<span data-ttu-id="67f3f-120">Specifica il nome di un modulo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="67f3f-120">Specifies the name of a module to retrieve.</span></span>

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

### <span data-ttu-id="67f3f-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="67f3f-121">-Profile</span></span>
<span data-ttu-id="67f3f-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67f3f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67f3f-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="67f3f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67f3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f3f-124">CommonParameters</span></span>
<span data-ttu-id="67f3f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f3f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f3f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f3f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67f3f-127">INPUTS</span></span>

## <span data-ttu-id="67f3f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67f3f-128">OUTPUTS</span></span>

### <span data-ttu-id="67f3f-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="67f3f-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="67f3f-130">Note</span><span class="sxs-lookup"><span data-stu-id="67f3f-130">NOTES</span></span>

## <span data-ttu-id="67f3f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67f3f-131">RELATED LINKS</span></span>

[<span data-ttu-id="67f3f-132">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="67f3f-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="67f3f-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="67f3f-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="67f3f-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="67f3f-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


