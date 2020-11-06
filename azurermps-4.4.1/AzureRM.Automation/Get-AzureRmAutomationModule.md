---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517132"
---
# <span data-ttu-id="52a69-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="52a69-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="52a69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52a69-102">SYNOPSIS</span></span>
<span data-ttu-id="52a69-103">Ottiene i metadati per i moduli dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="52a69-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52a69-104">SYNTAX</span></span>

### <span data-ttu-id="52a69-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52a69-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a69-106">ByName</span><span class="sxs-lookup"><span data-stu-id="52a69-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a69-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52a69-107">DESCRIPTION</span></span>
<span data-ttu-id="52a69-108">Il cmdlet **Get-AzureRmAutomationModule** ottiene i metadati per i moduli di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="52a69-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="52a69-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52a69-109">EXAMPLES</span></span>

### <span data-ttu-id="52a69-110">Esempio 1: ottenere tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="52a69-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="52a69-111">Questo comando consente di ottenere tutti i moduli nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="52a69-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="52a69-112">Esempio 2: ottenere un modulo</span><span class="sxs-lookup"><span data-stu-id="52a69-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="52a69-113">Questo comando ottiene un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="52a69-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="52a69-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52a69-114">PARAMETERS</span></span>

### <span data-ttu-id="52a69-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="52a69-115">-AutomationAccountName</span></span>
<span data-ttu-id="52a69-116">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="52a69-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="52a69-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="52a69-117">-Name</span></span>
<span data-ttu-id="52a69-118">Specifica il nome del modulo per cui questo cmdlet ottiene i metadati.</span><span class="sxs-lookup"><span data-stu-id="52a69-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="52a69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a69-119">-ResourceGroupName</span></span>
<span data-ttu-id="52a69-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene i metadati del modulo.</span><span class="sxs-lookup"><span data-stu-id="52a69-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="52a69-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a69-121">-DefaultProfile</span></span>
<span data-ttu-id="52a69-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52a69-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a69-123">CommonParameters</span></span>
<span data-ttu-id="52a69-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a69-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a69-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a69-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52a69-126">INPUTS</span></span>

## <span data-ttu-id="52a69-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52a69-127">OUTPUTS</span></span>

### <span data-ttu-id="52a69-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="52a69-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="52a69-129">Note</span><span class="sxs-lookup"><span data-stu-id="52a69-129">NOTES</span></span>

## <span data-ttu-id="52a69-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52a69-130">RELATED LINKS</span></span>

[<span data-ttu-id="52a69-131">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="52a69-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="52a69-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="52a69-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="52a69-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="52a69-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


