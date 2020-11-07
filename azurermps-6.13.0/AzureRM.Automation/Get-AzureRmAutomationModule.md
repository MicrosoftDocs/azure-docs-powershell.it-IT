---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2ed40d0ee0698c8e0ee8d4a1c443db32c843ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685453"
---
# <span data-ttu-id="343ed-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="343ed-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="343ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="343ed-102">SYNOPSIS</span></span>
<span data-ttu-id="343ed-103">Ottiene i metadati per i moduli dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="343ed-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="343ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="343ed-104">SYNTAX</span></span>

### <span data-ttu-id="343ed-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="343ed-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="343ed-106">ByName</span><span class="sxs-lookup"><span data-stu-id="343ed-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="343ed-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="343ed-107">DESCRIPTION</span></span>
<span data-ttu-id="343ed-108">Il cmdlet **Get-AzureRmAutomationModule** ottiene i metadati per i moduli di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="343ed-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="343ed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="343ed-109">EXAMPLES</span></span>

### <span data-ttu-id="343ed-110">Esempio 1: ottenere tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="343ed-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="343ed-111">Questo comando consente di ottenere tutti i moduli nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="343ed-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="343ed-112">Esempio 2: ottenere un modulo</span><span class="sxs-lookup"><span data-stu-id="343ed-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="343ed-113">Questo comando ottiene un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="343ed-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="343ed-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="343ed-114">PARAMETERS</span></span>

### <span data-ttu-id="343ed-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="343ed-115">-AutomationAccountName</span></span>
<span data-ttu-id="343ed-116">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="343ed-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="343ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343ed-117">-DefaultProfile</span></span>
<span data-ttu-id="343ed-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="343ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343ed-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="343ed-119">-Name</span></span>
<span data-ttu-id="343ed-120">Specifica il nome del modulo per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="343ed-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="343ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="343ed-122">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="343ed-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="343ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343ed-123">CommonParameters</span></span>
<span data-ttu-id="343ed-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="343ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343ed-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343ed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343ed-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="343ed-126">INPUTS</span></span>

### <span data-ttu-id="343ed-127">System. String</span><span class="sxs-lookup"><span data-stu-id="343ed-127">System.String</span></span>

## <span data-ttu-id="343ed-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="343ed-128">OUTPUTS</span></span>

### <span data-ttu-id="343ed-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="343ed-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="343ed-130">Note</span><span class="sxs-lookup"><span data-stu-id="343ed-130">NOTES</span></span>

## <span data-ttu-id="343ed-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="343ed-131">RELATED LINKS</span></span>

[<span data-ttu-id="343ed-132">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="343ed-132">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="343ed-133">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="343ed-133">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="343ed-134">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="343ed-134">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


