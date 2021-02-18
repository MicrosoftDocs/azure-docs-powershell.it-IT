---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201223"
---
# <span data-ttu-id="43539-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="43539-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="43539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43539-102">SYNOPSIS</span></span>
<span data-ttu-id="43539-103">Ottiene una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="43539-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="43539-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43539-104">SYNTAX</span></span>

### <span data-ttu-id="43539-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43539-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43539-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="43539-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43539-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="43539-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43539-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43539-108">DESCRIPTION</span></span>
<span data-ttu-id="43539-109">Il cmdlet **Get-AzAutomationConnection** ottiene una o più connessioni di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43539-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="43539-110">Per impostazione predefinita, questo cmdlet recupera tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="43539-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="43539-111">Specificare il nome di una connessione per ottenere una connessione specifica.</span><span class="sxs-lookup"><span data-stu-id="43539-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="43539-112">Specificare il nome del tipo di connessione per ottenere tutte le connessioni di un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="43539-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="43539-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43539-113">EXAMPLES</span></span>

### <span data-ttu-id="43539-114">Esempio 1: Ottenere tutte le connessioni</span><span class="sxs-lookup"><span data-stu-id="43539-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="43539-115">Questo comando recupera i metadati per tutte le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43539-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="43539-116">Esempio 2: Ottenere tutte le connessioni di un tipo</span><span class="sxs-lookup"><span data-stu-id="43539-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="43539-117">Questo comando recupera i metadati per le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="43539-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="43539-118">Questo comando recupera le connessioni del tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="43539-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="43539-119">Esempio 3: Ottenere una connessione</span><span class="sxs-lookup"><span data-stu-id="43539-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="43539-120">Questo comando recupera i metadati per la connessione denominata ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="43539-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="43539-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43539-121">PARAMETERS</span></span>

### <span data-ttu-id="43539-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43539-122">-AutomationAccountName</span></span>
<span data-ttu-id="43539-123">Specifica il nome dell'account di automazione per cui il cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="43539-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="43539-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="43539-124">-ConnectionTypeName</span></span>
<span data-ttu-id="43539-125">Specifica il nome di un tipo di connessione per cui il cmdlet recupera le connessioni.</span><span class="sxs-lookup"><span data-stu-id="43539-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43539-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43539-126">-DefaultProfile</span></span>
<span data-ttu-id="43539-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="43539-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43539-128">-Name</span><span class="sxs-lookup"><span data-stu-id="43539-128">-Name</span></span>
<span data-ttu-id="43539-129">Specifica il nome di una connessione che il cmdlet recupera.</span><span class="sxs-lookup"><span data-stu-id="43539-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43539-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43539-130">-ResourceGroupName</span></span>
<span data-ttu-id="43539-131">Specifica il nome di un gruppo di risorse per cui il cmdlet ottiene connessioni.</span><span class="sxs-lookup"><span data-stu-id="43539-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="43539-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43539-132">CommonParameters</span></span>
<span data-ttu-id="43539-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43539-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43539-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43539-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43539-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="43539-135">INPUTS</span></span>

### <span data-ttu-id="43539-136">System.String</span><span class="sxs-lookup"><span data-stu-id="43539-136">System.String</span></span>

## <span data-ttu-id="43539-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43539-137">OUTPUTS</span></span>

### <span data-ttu-id="43539-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="43539-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="43539-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="43539-139">NOTES</span></span>

## <span data-ttu-id="43539-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43539-140">RELATED LINKS</span></span>

[<span data-ttu-id="43539-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="43539-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="43539-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="43539-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


