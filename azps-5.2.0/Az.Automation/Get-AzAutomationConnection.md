---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328406"
---
# <span data-ttu-id="f183b-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f183b-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="f183b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f183b-102">SYNOPSIS</span></span>
<span data-ttu-id="f183b-103">Ottiene una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="f183b-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="f183b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f183b-104">SYNTAX</span></span>

### <span data-ttu-id="f183b-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f183b-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f183b-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="f183b-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f183b-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="f183b-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f183b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f183b-108">DESCRIPTION</span></span>
<span data-ttu-id="f183b-109">Il cmdlet **Get-AzAutomationConnection** ottiene una o più connessioni di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f183b-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="f183b-110">Per impostazione predefinita, questo cmdlet recupera tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="f183b-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="f183b-111">Specificare il nome di una connessione per ottenere una connessione specifica.</span><span class="sxs-lookup"><span data-stu-id="f183b-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="f183b-112">Specificare il nome del tipo di connessione per ottenere tutte le connessioni di un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="f183b-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="f183b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f183b-113">EXAMPLES</span></span>

### <span data-ttu-id="f183b-114">Esempio 1: ottenere tutte le connessioni</span><span class="sxs-lookup"><span data-stu-id="f183b-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f183b-115">Questo comando consente di ottenere metadati per tutte le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f183b-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f183b-116">Esempio 2: ottenere tutte le connessioni di un tipo</span><span class="sxs-lookup"><span data-stu-id="f183b-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="f183b-117">Questo comando consente di ottenere metadati per le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f183b-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f183b-118">Questo comando ottiene le connessioni del tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="f183b-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="f183b-119">Esempio 3: ottenere una connessione</span><span class="sxs-lookup"><span data-stu-id="f183b-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="f183b-120">Questo comando consente di ottenere metadati per la connessione denominata ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="f183b-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="f183b-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f183b-121">PARAMETERS</span></span>

### <span data-ttu-id="f183b-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f183b-122">-AutomationAccountName</span></span>
<span data-ttu-id="f183b-123">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="f183b-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="f183b-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="f183b-124">-ConnectionTypeName</span></span>
<span data-ttu-id="f183b-125">Specifica il nome di un tipo di connessione per cui questo cmdlet recupera le connessioni.</span><span class="sxs-lookup"><span data-stu-id="f183b-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="f183b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f183b-126">-DefaultProfile</span></span>
<span data-ttu-id="f183b-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f183b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f183b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f183b-128">-Name</span></span>
<span data-ttu-id="f183b-129">Specifica il nome di una connessione recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f183b-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="f183b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f183b-130">-ResourceGroupName</span></span>
<span data-ttu-id="f183b-131">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="f183b-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="f183b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f183b-132">CommonParameters</span></span>
<span data-ttu-id="f183b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f183b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f183b-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f183b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f183b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f183b-135">INPUTS</span></span>

### <span data-ttu-id="f183b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f183b-136">System.String</span></span>

## <span data-ttu-id="f183b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f183b-137">OUTPUTS</span></span>

### <span data-ttu-id="f183b-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="f183b-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="f183b-139">Note</span><span class="sxs-lookup"><span data-stu-id="f183b-139">NOTES</span></span>

## <span data-ttu-id="f183b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f183b-140">RELATED LINKS</span></span>

[<span data-ttu-id="f183b-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f183b-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="f183b-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="f183b-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


