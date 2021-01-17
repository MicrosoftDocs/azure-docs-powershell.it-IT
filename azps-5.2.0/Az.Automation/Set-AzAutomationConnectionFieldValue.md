---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373110"
---
# <span data-ttu-id="d04ed-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="d04ed-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="d04ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d04ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d04ed-103">Modifica il valore di un campo in una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="d04ed-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="d04ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d04ed-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d04ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d04ed-105">DESCRIPTION</span></span>
<span data-ttu-id="d04ed-106">Il cmdlet **set-AzAutomationConnectionFieldValue** modifica il valore di un campo in una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d04ed-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="d04ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d04ed-107">EXAMPLES</span></span>

### <span data-ttu-id="d04ed-108">Esempio 1: modificare un valore di campo in una connessione</span><span class="sxs-lookup"><span data-stu-id="d04ed-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="d04ed-109">Questo comando cambia l'ID abbonamento per la connessione Azure denominata ContosoConnection nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="d04ed-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="d04ed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d04ed-110">PARAMETERS</span></span>

### <span data-ttu-id="d04ed-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d04ed-111">-AutomationAccountName</span></span>
<span data-ttu-id="d04ed-112">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un campo in una connessione.</span><span class="sxs-lookup"><span data-stu-id="d04ed-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="d04ed-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="d04ed-113">-ConnectionFieldName</span></span>
<span data-ttu-id="d04ed-114">Specifica un nome per il campo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d04ed-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d04ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d04ed-115">-DefaultProfile</span></span>
<span data-ttu-id="d04ed-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d04ed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d04ed-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d04ed-117">-Name</span></span>
<span data-ttu-id="d04ed-118">Specifica un nome per la connessione per cui questo cmdlet modifica un campo.</span><span class="sxs-lookup"><span data-stu-id="d04ed-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="d04ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d04ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="d04ed-120">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un campo in una connessione.</span><span class="sxs-lookup"><span data-stu-id="d04ed-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="d04ed-121">-Valore</span><span class="sxs-lookup"><span data-stu-id="d04ed-121">-Value</span></span>
<span data-ttu-id="d04ed-122">Specifica un valore da modificare nel campo Connection.</span><span class="sxs-lookup"><span data-stu-id="d04ed-122">Specifies a value to modify in the connection field.</span></span>

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

### <span data-ttu-id="d04ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d04ed-123">CommonParameters</span></span>
<span data-ttu-id="d04ed-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d04ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d04ed-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d04ed-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d04ed-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d04ed-126">INPUTS</span></span>

### <span data-ttu-id="d04ed-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d04ed-127">System.String</span></span>

### <span data-ttu-id="d04ed-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="d04ed-128">System.Object</span></span>

## <span data-ttu-id="d04ed-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d04ed-129">OUTPUTS</span></span>

### <span data-ttu-id="d04ed-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="d04ed-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="d04ed-131">Note</span><span class="sxs-lookup"><span data-stu-id="d04ed-131">NOTES</span></span>

## <span data-ttu-id="d04ed-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d04ed-132">RELATED LINKS</span></span>

[<span data-ttu-id="d04ed-133">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d04ed-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


