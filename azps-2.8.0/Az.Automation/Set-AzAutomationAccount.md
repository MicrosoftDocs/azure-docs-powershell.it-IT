---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: b0bebe0f831cc4041ecdeeeaa3ec8066faeacc8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675700"
---
# <span data-ttu-id="b473c-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b473c-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="b473c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b473c-102">SYNOPSIS</span></span>
<span data-ttu-id="b473c-103">Modifica un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b473c-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="b473c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b473c-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b473c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b473c-105">DESCRIPTION</span></span>
<span data-ttu-id="b473c-106">Il cmdlet **set-AzAutomationAccount** modifica un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b473c-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="b473c-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="b473c-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="b473c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b473c-108">EXAMPLES</span></span>

### <span data-ttu-id="b473c-109">Esempio 1: impostare i tag per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="b473c-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="b473c-110">Il primo comando assegna due coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="b473c-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="b473c-111">Il secondo comando imposta i tag in $Tags per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="b473c-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="b473c-112">Esempio 2: cambiare il piano per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="b473c-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="b473c-113">Questo comando imposta il piano su Basic per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="b473c-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="b473c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b473c-114">PARAMETERS</span></span>

### <span data-ttu-id="b473c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b473c-115">-DefaultProfile</span></span>
<span data-ttu-id="b473c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b473c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b473c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b473c-117">-Name</span></span>
<span data-ttu-id="b473c-118">Specifica il nome dell'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b473c-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473c-119">-Piano</span><span class="sxs-lookup"><span data-stu-id="b473c-119">-Plan</span></span>
<span data-ttu-id="b473c-120">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b473c-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="b473c-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b473c-121">Valid values are:</span></span>
- <span data-ttu-id="b473c-122">Base</span><span class="sxs-lookup"><span data-stu-id="b473c-122">Basic</span></span>
- <span data-ttu-id="b473c-123">Gratuito</span><span class="sxs-lookup"><span data-stu-id="b473c-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b473c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b473c-125">Specifica il nome di un gruppo di risorse che contiene l'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b473c-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b473c-126">-Tags</span></span>
<span data-ttu-id="b473c-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b473c-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b473c-128">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b473c-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b473c-129">CommonParameters</span></span>
<span data-ttu-id="b473c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b473c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b473c-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b473c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b473c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b473c-132">INPUTS</span></span>

### <span data-ttu-id="b473c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b473c-133">System.String</span></span>

### <span data-ttu-id="b473c-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="b473c-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="b473c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b473c-135">OUTPUTS</span></span>

### <span data-ttu-id="b473c-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b473c-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="b473c-137">Note</span><span class="sxs-lookup"><span data-stu-id="b473c-137">NOTES</span></span>

## <span data-ttu-id="b473c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b473c-138">RELATED LINKS</span></span>

[<span data-ttu-id="b473c-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b473c-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="b473c-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b473c-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="b473c-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b473c-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)