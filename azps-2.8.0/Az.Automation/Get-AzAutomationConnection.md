---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 267c18ea4abf87936c47629eca523b254b411240
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675826"
---
# <span data-ttu-id="9a9cb-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a9cb-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="9a9cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9cb-103">Ottiene una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="9a9cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a9cb-104">SYNTAX</span></span>

### <span data-ttu-id="9a9cb-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a9cb-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a9cb-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="9a9cb-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a9cb-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9a9cb-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a9cb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a9cb-108">DESCRIPTION</span></span>
<span data-ttu-id="9a9cb-109">Il cmdlet **Get-AzAutomationConnection** ottiene una o più connessioni di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="9a9cb-110">Per impostazione predefinita, questo cmdlet recupera tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="9a9cb-111">Specificare il nome di una connessione per ottenere una connessione specifica.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="9a9cb-112">Specificare il nome del tipo di connessione per ottenere tutte le connessioni di un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="9a9cb-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a9cb-113">EXAMPLES</span></span>

### <span data-ttu-id="9a9cb-114">Esempio 1: ottenere tutte le connessioni</span><span class="sxs-lookup"><span data-stu-id="9a9cb-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9a9cb-115">Questo comando consente di ottenere metadati per tutte le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9a9cb-116">Esempio 2: ottenere tutte le connessioni di un tipo</span><span class="sxs-lookup"><span data-stu-id="9a9cb-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="9a9cb-117">Questo comando consente di ottenere metadati per le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="9a9cb-118">Questo comando ottiene le connessioni del tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="9a9cb-119">Esempio 3: ottenere una connessione</span><span class="sxs-lookup"><span data-stu-id="9a9cb-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="9a9cb-120">Questo comando consente di ottenere metadati per la connessione denominata ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="9a9cb-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a9cb-121">PARAMETERS</span></span>

### <span data-ttu-id="9a9cb-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a9cb-122">-AutomationAccountName</span></span>
<span data-ttu-id="9a9cb-123">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="9a9cb-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9a9cb-124">-ConnectionTypeName</span></span>
<span data-ttu-id="9a9cb-125">Specifica il nome di un tipo di connessione per cui questo cmdlet recupera le connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="9a9cb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a9cb-126">-DefaultProfile</span></span>
<span data-ttu-id="9a9cb-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9a9cb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a9cb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a9cb-128">-Name</span></span>
<span data-ttu-id="9a9cb-129">Specifica il nome di una connessione recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="9a9cb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a9cb-130">-ResourceGroupName</span></span>
<span data-ttu-id="9a9cb-131">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="9a9cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9cb-132">CommonParameters</span></span>
<span data-ttu-id="9a9cb-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a9cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9cb-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a9cb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9cb-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a9cb-135">INPUTS</span></span>

### <span data-ttu-id="9a9cb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9a9cb-136">System.String</span></span>

## <span data-ttu-id="9a9cb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a9cb-137">OUTPUTS</span></span>

### <span data-ttu-id="9a9cb-138">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="9a9cb-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9a9cb-139">Note</span><span class="sxs-lookup"><span data-stu-id="9a9cb-139">NOTES</span></span>

## <span data-ttu-id="9a9cb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a9cb-140">RELATED LINKS</span></span>

[<span data-ttu-id="9a9cb-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a9cb-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="9a9cb-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9a9cb-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


