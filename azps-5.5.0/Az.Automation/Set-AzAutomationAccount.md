---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205427"
---
# <span data-ttu-id="22352-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22352-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="22352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22352-102">SYNOPSIS</span></span>
<span data-ttu-id="22352-103">Modifica un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="22352-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="22352-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22352-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22352-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22352-105">DESCRIPTION</span></span>
<span data-ttu-id="22352-106">Il cmdlet **Set-AzAutomationAccount** modifica un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="22352-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="22352-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="22352-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="22352-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22352-108">EXAMPLES</span></span>

### <span data-ttu-id="22352-109">Esempio 1: Impostare i tag per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="22352-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="22352-110">Il primo comando assegna due coppie chiave/valore alla $Tags variabile.</span><span class="sxs-lookup"><span data-stu-id="22352-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="22352-111">Il secondo comando imposta i tag in $Tags per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="22352-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="22352-112">Esempio 2: Cambiare il piano per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="22352-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="22352-113">Questo comando modifica il piano in Base per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="22352-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="22352-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22352-114">PARAMETERS</span></span>

### <span data-ttu-id="22352-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22352-115">-DefaultProfile</span></span>
<span data-ttu-id="22352-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="22352-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22352-117">-Name</span><span class="sxs-lookup"><span data-stu-id="22352-117">-Name</span></span>
<span data-ttu-id="22352-118">Specifica il nome dell'account di automazione modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22352-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="22352-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="22352-119">-Plan</span></span>
<span data-ttu-id="22352-120">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="22352-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="22352-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="22352-121">Valid values are:</span></span>
- <span data-ttu-id="22352-122">Di base</span><span class="sxs-lookup"><span data-stu-id="22352-122">Basic</span></span>
- <span data-ttu-id="22352-123">Gratis</span><span class="sxs-lookup"><span data-stu-id="22352-123">Free</span></span>

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

### <span data-ttu-id="22352-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22352-124">-ResourceGroupName</span></span>
<span data-ttu-id="22352-125">Specifica il nome di un gruppo di risorse che contiene l'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22352-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="22352-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="22352-126">-Tags</span></span>
<span data-ttu-id="22352-127">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="22352-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22352-128">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="22352-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22352-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22352-129">CommonParameters</span></span>
<span data-ttu-id="22352-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22352-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22352-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22352-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22352-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="22352-132">INPUTS</span></span>

### <span data-ttu-id="22352-133">System.String</span><span class="sxs-lookup"><span data-stu-id="22352-133">System.String</span></span>

### <span data-ttu-id="22352-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="22352-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="22352-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22352-135">OUTPUTS</span></span>

### <span data-ttu-id="22352-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22352-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="22352-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="22352-137">NOTES</span></span>

## <span data-ttu-id="22352-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22352-138">RELATED LINKS</span></span>

[<span data-ttu-id="22352-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22352-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="22352-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22352-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="22352-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="22352-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
