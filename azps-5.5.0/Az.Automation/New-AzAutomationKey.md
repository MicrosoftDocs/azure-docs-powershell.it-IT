---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201070"
---
# <span data-ttu-id="0076b-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="0076b-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="0076b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0076b-102">SYNOPSIS</span></span>
<span data-ttu-id="0076b-103">Rigenera i codici di registrazione per un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="0076b-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="0076b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0076b-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0076b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0076b-105">DESCRIPTION</span></span>
<span data-ttu-id="0076b-106">Il cmdlet **New-AzAutomationKey** rigenera le chiavi di registrazione per un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0076b-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="0076b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0076b-107">EXAMPLES</span></span>

### <span data-ttu-id="0076b-108">Esempio 1: Rigenerare una chiave per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="0076b-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0076b-109">Questo comando rigenera la chiave primaria per l'account di automazione di Azure denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0076b-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0076b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0076b-110">PARAMETERS</span></span>

### <span data-ttu-id="0076b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0076b-111">-AutomationAccountName</span></span>
<span data-ttu-id="0076b-112">Specifica il nome di un account di automazione per cui questo cmdlet rigenera le chiavi.</span><span class="sxs-lookup"><span data-stu-id="0076b-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0076b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0076b-113">-DefaultProfile</span></span>
<span data-ttu-id="0076b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0076b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0076b-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0076b-115">-KeyType</span></span>
<span data-ttu-id="0076b-116">Specifica il tipo di codice di registrazione dell'agente.</span><span class="sxs-lookup"><span data-stu-id="0076b-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="0076b-117">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="0076b-117">Valid values are:</span></span> 
- <span data-ttu-id="0076b-118">Principale</span><span class="sxs-lookup"><span data-stu-id="0076b-118">Primary</span></span> 
- <span data-ttu-id="0076b-119">Secondary</span><span class="sxs-lookup"><span data-stu-id="0076b-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0076b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0076b-120">-ResourceGroupName</span></span>
<span data-ttu-id="0076b-121">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0076b-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0076b-122">Questo cmdlet rigenera le chiavi per un account di automazione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0076b-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0076b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0076b-123">CommonParameters</span></span>
<span data-ttu-id="0076b-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0076b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0076b-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0076b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0076b-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="0076b-126">INPUTS</span></span>

### <span data-ttu-id="0076b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0076b-127">System.String</span></span>

## <span data-ttu-id="0076b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0076b-128">OUTPUTS</span></span>

### <span data-ttu-id="0076b-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="0076b-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="0076b-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="0076b-130">NOTES</span></span>

## <span data-ttu-id="0076b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0076b-131">RELATED LINKS</span></span>
