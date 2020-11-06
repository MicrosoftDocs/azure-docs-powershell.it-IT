---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationConnectionFieldValue.md
ms.openlocfilehash: 84da08588838982353bc8c39354452bec1a17a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519939"
---
# <span data-ttu-id="b787e-101">Set-AzureRmAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="b787e-101">Set-AzureRmAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="b787e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b787e-102">SYNOPSIS</span></span>
<span data-ttu-id="b787e-103">Modifica il valore di un campo in una connessione di automazione.</span><span class="sxs-lookup"><span data-stu-id="b787e-103">Modifies the value of a field in an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b787e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b787e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b787e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b787e-105">DESCRIPTION</span></span>
<span data-ttu-id="b787e-106">Il cmdlet **set-AzureRmAutomationConnectionFieldValue** modifica il valore di un campo in una connessione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b787e-106">The **Set-AzureRmAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="b787e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b787e-107">EXAMPLES</span></span>

### <span data-ttu-id="b787e-108">Esempio 1: modificare un valore di campo in una connessione</span><span class="sxs-lookup"><span data-stu-id="b787e-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzureRmAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="b787e-109">Questo comando cambia l'ID abbonamento per la connessione Azure denominata ContosoConnection nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="b787e-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="b787e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b787e-110">PARAMETERS</span></span>

### <span data-ttu-id="b787e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b787e-111">-AutomationAccountName</span></span>
<span data-ttu-id="b787e-112">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un campo in una connessione.</span><span class="sxs-lookup"><span data-stu-id="b787e-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b787e-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="b787e-113">-ConnectionFieldName</span></span>
<span data-ttu-id="b787e-114">Specifica un nome per il campo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b787e-114">Specifies a name for the field that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b787e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b787e-115">-DefaultProfile</span></span>
<span data-ttu-id="b787e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b787e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b787e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b787e-117">-Name</span></span>
<span data-ttu-id="b787e-118">Specifica un nome per la connessione per cui questo cmdlet modifica un campo.</span><span class="sxs-lookup"><span data-stu-id="b787e-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b787e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b787e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b787e-120">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un campo in una connessione.</span><span class="sxs-lookup"><span data-stu-id="b787e-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b787e-121">-Valore</span><span class="sxs-lookup"><span data-stu-id="b787e-121">-Value</span></span>
<span data-ttu-id="b787e-122">Specifica un valore da modificare nel campo Connection.</span><span class="sxs-lookup"><span data-stu-id="b787e-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b787e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b787e-123">CommonParameters</span></span>
<span data-ttu-id="b787e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b787e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b787e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b787e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b787e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b787e-126">INPUTS</span></span>

### <span data-ttu-id="b787e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b787e-127">None</span></span>
<span data-ttu-id="b787e-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b787e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b787e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b787e-129">OUTPUTS</span></span>

### <span data-ttu-id="b787e-130">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="b787e-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="b787e-131">Note</span><span class="sxs-lookup"><span data-stu-id="b787e-131">NOTES</span></span>

## <span data-ttu-id="b787e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b787e-132">RELATED LINKS</span></span>

[<span data-ttu-id="b787e-133">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b787e-133">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


