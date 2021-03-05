---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: d11b99352d3a3f75c24e47cabfe06e816958fb82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004734"
---
# <span data-ttu-id="40cc1-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="40cc1-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="40cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="40cc1-103">Modifica il valore di un campo in una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="40cc1-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="40cc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40cc1-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40cc1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="40cc1-105">DESCRIPTION</span></span>
<span data-ttu-id="40cc1-106">Il cmdlet **Set-AzAutomationConnectionFieldValue** modifica il valore di un campo in una connessione nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="40cc1-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="40cc1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40cc1-107">EXAMPLES</span></span>

### <span data-ttu-id="40cc1-108">Esempio 1: Modificare il valore di un campo in una connessione</span><span class="sxs-lookup"><span data-stu-id="40cc1-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="40cc1-109">Questo comando modifica l'ID sottoscrizione per la connessione azure denominata ContosoConnection nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="40cc1-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="40cc1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40cc1-110">PARAMETERS</span></span>

### <span data-ttu-id="40cc1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40cc1-111">-AutomationAccountName</span></span>
<span data-ttu-id="40cc1-112">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un campo in una connessione.</span><span class="sxs-lookup"><span data-stu-id="40cc1-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="40cc1-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="40cc1-113">-ConnectionFieldName</span></span>
<span data-ttu-id="40cc1-114">Specifica un nome per il campo modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40cc1-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cc1-115">-DefaultProfile</span></span>
<span data-ttu-id="40cc1-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="40cc1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40cc1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="40cc1-117">-Name</span></span>
<span data-ttu-id="40cc1-118">Specifica un nome per la connessione per cui il cmdlet modifica un campo.</span><span class="sxs-lookup"><span data-stu-id="40cc1-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cc1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cc1-119">-ResourceGroupName</span></span>
<span data-ttu-id="40cc1-120">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un campo in una connessione.</span><span class="sxs-lookup"><span data-stu-id="40cc1-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="40cc1-121">-Value</span><span class="sxs-lookup"><span data-stu-id="40cc1-121">-Value</span></span>
<span data-ttu-id="40cc1-122">Specifica un valore da modificare nel campo della connessione.</span><span class="sxs-lookup"><span data-stu-id="40cc1-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40cc1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cc1-123">CommonParameters</span></span>
<span data-ttu-id="40cc1-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cc1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cc1-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40cc1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cc1-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="40cc1-126">INPUTS</span></span>

### <span data-ttu-id="40cc1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="40cc1-127">System.String</span></span>

### <span data-ttu-id="40cc1-128">System.Object</span><span class="sxs-lookup"><span data-stu-id="40cc1-128">System.Object</span></span>

## <span data-ttu-id="40cc1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40cc1-129">OUTPUTS</span></span>

### <span data-ttu-id="40cc1-130">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="40cc1-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="40cc1-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="40cc1-131">NOTES</span></span>

## <span data-ttu-id="40cc1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40cc1-132">RELATED LINKS</span></span>

[<span data-ttu-id="40cc1-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="40cc1-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


