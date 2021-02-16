---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199671"
---
# <span data-ttu-id="d9849-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d9849-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="d9849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9849-102">SYNOPSIS</span></span>
<span data-ttu-id="d9849-103">Recupera i metadati per i moduli dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="d9849-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="d9849-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9849-104">SYNTAX</span></span>

### <span data-ttu-id="d9849-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9849-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9849-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d9849-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9849-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9849-107">DESCRIPTION</span></span>
<span data-ttu-id="d9849-108">Il cmdlet **Get-AzAutomationModule** recupera i metadati per i moduli dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9849-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="d9849-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9849-109">EXAMPLES</span></span>

### <span data-ttu-id="d9849-110">Esempio 1: Ottenere tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="d9849-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d9849-111">Questo comando recupera tutti i moduli nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d9849-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d9849-112">Esempio 2: Ottenere un modulo</span><span class="sxs-lookup"><span data-stu-id="d9849-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d9849-113">Questo comando ottiene un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d9849-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d9849-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9849-114">PARAMETERS</span></span>

### <span data-ttu-id="d9849-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9849-115">-AutomationAccountName</span></span>
<span data-ttu-id="d9849-116">Specifica il nome dell'account di automazione per cui il cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="d9849-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="d9849-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9849-117">-DefaultProfile</span></span>
<span data-ttu-id="d9849-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d9849-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9849-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d9849-119">-Name</span></span>
<span data-ttu-id="d9849-120">Specifica il nome del modulo per cui il cmdlet riceve i metadati.</span><span class="sxs-lookup"><span data-stu-id="d9849-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9849-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9849-121">-ResourceGroupName</span></span>
<span data-ttu-id="d9849-122">Specifica il nome di un gruppo di risorse per cui il cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="d9849-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="d9849-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9849-123">CommonParameters</span></span>
<span data-ttu-id="d9849-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9849-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9849-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9849-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9849-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9849-126">INPUTS</span></span>

### <span data-ttu-id="d9849-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d9849-127">System.String</span></span>

## <span data-ttu-id="d9849-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9849-128">OUTPUTS</span></span>

### <span data-ttu-id="d9849-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="d9849-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d9849-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9849-130">NOTES</span></span>

## <span data-ttu-id="d9849-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9849-131">RELATED LINKS</span></span>

[<span data-ttu-id="d9849-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d9849-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="d9849-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d9849-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="d9849-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d9849-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


