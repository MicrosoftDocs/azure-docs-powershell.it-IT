---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: e83a4c71656feb9dbe766339244e54038fa56c84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519650"
---
# <span data-ttu-id="36d3b-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="36d3b-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="36d3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="36d3b-103">Ottiene una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="36d3b-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36d3b-104">SYNTAX</span></span>

### <span data-ttu-id="36d3b-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36d3b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36d3b-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="36d3b-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36d3b-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="36d3b-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d3b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="36d3b-109">Il cmdlet **Get-AzureRmAutomationConnection** ottiene una o più connessioni di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="36d3b-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="36d3b-110">Per impostazione predefinita, questo cmdlet recupera tutte le connessioni.</span><span class="sxs-lookup"><span data-stu-id="36d3b-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="36d3b-111">Specificare il nome di una connessione per ottenere una connessione specifica.</span><span class="sxs-lookup"><span data-stu-id="36d3b-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="36d3b-112">Specificare il nome del tipo di connessione per ottenere tutte le connessioni di un tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="36d3b-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="36d3b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36d3b-113">EXAMPLES</span></span>

### <span data-ttu-id="36d3b-114">Esempio 1: ottenere tutte le connessioni</span><span class="sxs-lookup"><span data-stu-id="36d3b-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="36d3b-115">Questo comando consente di ottenere metadati per tutte le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36d3b-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="36d3b-116">Esempio 2: ottenere tutte le connessioni di un tipo</span><span class="sxs-lookup"><span data-stu-id="36d3b-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="36d3b-117">Questo comando consente di ottenere metadati per le connessioni nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36d3b-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="36d3b-118">Questo comando ottiene le connessioni del tipo SqlServer.</span><span class="sxs-lookup"><span data-stu-id="36d3b-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="36d3b-119">Esempio 3: ottenere una connessione</span><span class="sxs-lookup"><span data-stu-id="36d3b-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="36d3b-120">Questo comando consente di ottenere metadati per la connessione denominata ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="36d3b-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="36d3b-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36d3b-121">PARAMETERS</span></span>

### <span data-ttu-id="36d3b-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="36d3b-122">-AutomationAccountName</span></span>
<span data-ttu-id="36d3b-123">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="36d3b-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="36d3b-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="36d3b-124">-ConnectionTypeName</span></span>
<span data-ttu-id="36d3b-125">Specifica il nome di un tipo di connessione per cui questo cmdlet recupera le connessioni.</span><span class="sxs-lookup"><span data-stu-id="36d3b-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="36d3b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="36d3b-126">-Name</span></span>
<span data-ttu-id="36d3b-127">Specifica il nome di una connessione recuperata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36d3b-127">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="36d3b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d3b-128">-ResourceGroupName</span></span>
<span data-ttu-id="36d3b-129">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene le connessioni.</span><span class="sxs-lookup"><span data-stu-id="36d3b-129">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="36d3b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d3b-130">-DefaultProfile</span></span>
<span data-ttu-id="36d3b-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36d3b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d3b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d3b-132">CommonParameters</span></span>
<span data-ttu-id="36d3b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36d3b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d3b-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d3b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d3b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36d3b-135">INPUTS</span></span>

## <span data-ttu-id="36d3b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36d3b-136">OUTPUTS</span></span>

### <span data-ttu-id="36d3b-137">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="36d3b-137">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="36d3b-138">Note</span><span class="sxs-lookup"><span data-stu-id="36d3b-138">NOTES</span></span>

## <span data-ttu-id="36d3b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36d3b-139">RELATED LINKS</span></span>

[<span data-ttu-id="36d3b-140">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="36d3b-140">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="36d3b-141">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="36d3b-141">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


